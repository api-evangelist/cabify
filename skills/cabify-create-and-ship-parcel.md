---
name: Create and ship a Cabify parcel
description: Estimate, create, ship, and track a last-mile delivery using the Cabify Logistics API.
api: openapi/cabify-logistics-openapi.yml
operations: [shippingTypesAvailable, EstimateShipParcels, addParcels, shipParcels, statusParcel, timelineParcel, cancelParcels]
---

# Create and ship a Cabify parcel

Use the Cabify Logistics API (v1) to create and track a parcel delivery.

## Auth
OAuth2 client-credentials Bearer token (same issuance as Ride-Hailing; production host
`https://logistics.api.cabify.com`, sandbox `https://logistics.api.cabify-sandbox.com`). See
`authentication/cabify-authentication.yml`.

## Steps
1. **Check coverage / shipping types.** Call `shippingTypesAvailable`
   (`GET /v1/shipping_types/available`) for your pickup location to get valid shipping types.
2. **Estimate (optional).** Call `EstimateShipParcels` (`POST /v3/parcels/estimate`) for price,
   pickup time, and delivery time for a shipping type.
3. **Create parcels.** Call `addParcels` (`POST /v1/parcels`) with `pickup_info` and `dropoff_info`
   (each via `loc`, `addr`, or `hub_external_id`). Creating a parcel does NOT schedule pickup.
4. **Ship.** Call `shipParcels` (`POST /v1/parcels/ship`) with the chosen shipping type to schedule
   the pickup.
5. **Track.** Call `statusParcel` (`GET /v1/parcels/{parcel_id}/status`) for current state, and
   `timelineParcel` (`GET /v1/parcels/{parcel_id}/timeline`) for the ordered state history (last 30
   days). Or subscribe to webhooks via `subscribeWebhook` (`POST /v1/webhooks`).
6. **Cancel.** Call `cancelParcels` (`POST /v1/parcels/deliver/cancel`) — allowed only in
   `qualifiedforpickup`, `onroutetopickup`, `pickingup`; not after pickup. May incur costs.

## Rules
- Delivery-lifecycle failures surface as `failure_reason`, `pickup_failed.reason`, and
  `delivery_attempt.fail_reason` (e.g. `payment_method_declined`). See `errors/cabify-operation-errors.yml`.
- Money is ISO 4217 minor units (€6.30 → 630).
- Webhook delivery is at-least-once; deduplicate events.
