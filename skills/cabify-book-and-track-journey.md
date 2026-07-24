---
name: Book and track a Cabify journey
description: Estimate, book, and track a ride-hailing journey to completion using the Cabify Ride-Hailing API.
api: openapi/cabify-ride-hailing-openapi.yml
operations: [getEstimation, createJourney, getJourneyState, getJourney, keepSearching, cancelJourney]
---

# Book and track a Cabify journey

Use the Cabify Ride-Hailing API (v4) to price, book, and track a ride.

## Auth
OAuth2 client-credentials. POST client_id/client_secret to
`https://cabify.com/auth/api/authorization` (sandbox: `cabify-sandbox.com`) to get a Bearer token;
send `Authorization: Bearer <token>` on every request. Tokens last ~30 days. See
`authentication/cabify-authentication.yml`.

## Steps
1. **Estimate first (required).** Call `getEstimation` (`POST /api/v4/estimates`) with origin/destination
   stops. You MUST do this before booking — the response returns `product.id` (pass as `product_id`)
   plus pricing and ETA. If the origin is a large venue, the response may include a `hub` with
   meeting points. Estimate no more than 5 minutes before booking.
2. **Book.** Call `createJourney` (`POST /api/v4/journey`) with the `product_id` from the estimate.
   For reservations, set `start_at` (`YYYY-MM-DD HH:MM:SS`, local pickup time), at least 30 minutes
   ahead and up to 60 days out — reuse the same `start_at` you passed to the estimate.
3. **Track.** Poll `getJourneyState` (`GET /api/v4/journey/{id}/state`) for driver, vehicle, and
   waypoints, or (preferred) configure journey-state webhooks. States progress hire → hired →
   arrived → pick up → drop off → terminated. **Stop polling once you receive a terminal state.**
4. **Booking details / price.** Call `getJourney` (`GET /api/v4/journey/{journey_id}`) for stops,
   cost breakdown, and `end_state`.
5. **No driver found?** Call `keepSearching` (`POST /api/v4/journey/{id}/keep_searching`) to re-enter
   `hire` for another 5 minutes without a new estimate.
6. **Cancel.** Call `cancelJourney` (`POST /api/v4/journey/{id}/state`). Free before assignment;
   fees may apply after. Returns 409 if already terminated.

## Rules
- Sandbox pickups must be inside the central-Madrid polygon (see `sandbox/cabify-sandbox.yml`).
- Errors use standard HTTP codes with custom bodies; retry only on 5xx. See `errors/cabify-problem-types.yml`.
- Webhooks are at-least-once — dedupe on `journey_id` + `state`.
