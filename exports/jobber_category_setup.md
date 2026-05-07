# Jobber Category & Service Setup Guide

**Source:** PRICING_MANUAL.md (Section 2 — Jobber Pricebook Structure)

Use this guide to create the categories and services in Jobber's *Products & Services* library. Service names below are formatted to copy directly into Jobber's *Service Name* field.

## Setup Order

1. Create all categories first (in the order listed below).
2. Create the recommended custom fields (see below).
3. Create the recommended tags (see below).
4. Import `jobber_pricebook.csv` to populate services in bulk, OR add each service manually using the names below.
5. After services are created, paste the customer description from `jobber_pricebook.csv` into each service's *Description* field.
6. Paste the internal note into the *Internal Notes* field (not visible to customers).
7. Set the unit type and base price per the CSV. Base Price and Minimum Charge are numeric-only (no $ or commas) for clean import.

## Categories & Services

### 1. Driveway & Gravel

- Gravel Driveway Refresh - Standard
- Gravel Spread - Customer-Supplied Material
- Pothole Repair - Per Pothole
- Driveway Grading & Reshaping
- Driveway Culvert Repair

### 2. Property Cleanup

- Brush Pile Removal - Standard
- General Property Cleanup
- Storm Cleanup - Emergency Response

### 3. Vegetation Management

- Acreage Mowing - Tall Grass / Pasture
- Heavy Brush Cutting - Per Hour
- Fence Line Cleanup

### 4. Tree & Stump

- Stump Grinding - Standard
- Small Tree Removal

### 5. Grading & Dirt Work

- Light Grading
- Dirt Work - Excavation & Fill

### 6. Specialty / Project Services

- Minor Drainage Correction

### 7. Demolition

- Small Demolition - Sheds & Outbuildings
- Fence Removal

### 8. Hourly / Skid Steer

- Skid Steer + Operator - Hourly
- Half Day Skid Steer
- Full Day Skid Steer

### 9. Service Bundles

- Rural Property Cleanup Package
- Driveway Refresh Package
- Fence Line Recovery Package
- Storm Cleanup Package
- Acreage Maintenance - Per Visit
- Acreage Maintenance - 3-Visit Seasonal

## Quick Reference: Total Counts

- **Categories:** 9
- **Services:** 27

## Recommended Custom Fields

| Custom Field | Type | Options | Purpose |
|---|---|---|---|
| Access Difficulty | Dropdown | Easy / Medium / Hard / Severe | Drives the difficulty modifier on internal pricing. |
| Ground Conditions | Dropdown | Dry / Soft / Saturated / Frozen | Drives reschedule risk and equipment selection. |
| Estimated Tons | Number |  | Driveway and material work. |
| Estimated Dump Loads | Number |  | Brush, demo, cleanup pricing. |
| Travel Zone | Dropdown | 0-25 / 25-40 / 40-60 / 60+ mi | Drives mobilization fee. |
| Attachment Needed | Dropdown | Bucket / Grapple / Brush Cutter / Harley Rake / Stump Grinder / Auger / Forks | Schedules the right attachment for the job. |
| Utility Locate Required | Yes / No |  | Triggers Kansas One-Call. |
| Photos Uploaded | Yes / No |  | Drives quote confidence. |
| Customer Priority | Dropdown | Standard / Same Week / Emergency | Drives surcharge logic. |
| Quote Confidence | Dropdown | High / Medium / Low | High = remote quote OK; Medium = photos required; Low = site visit. |

**Quote Confidence reference:**
- **High** — remote quote acceptable with basic info (length, acreage, count)
- **Medium** — photos required before sending firm quote
- **Low** — on-site walk-through required

## Recommended Tags

Use tags for filtering, reporting, and identifying high-margin or recurring work:

`Driveway`, `Potholes`, `Cleanup`, `Storm`, `Brush`, `Fence Line`, `Acreage`, `Stump`, `Tree`, `Drainage`, `Demolition`, `Recurring`, `High Margin`, `Emergency`, `Bundle`, `Rural`, `Residential`, `Material Delivery`, `Recurring Maintenance`

**Tag usage notes:**
- `High Margin` — apply to pothole repair, stump grinding, brush pile removal (rural burn), storm cleanup
- `Recurring` and `Recurring Maintenance` — apply to acreage mowing seasonal plans, annual driveway refresh
- `Emergency` — pair with Customer Priority = Emergency to drive surcharge logic
- `Bundle` — apply to all packaged services for quick filtering
- `Material Delivery` — apply when material pass-through is included

## Recommended Jobber Settings

| Setting | Recommendation |
|---|---|
| Default tax rate | Apply per Kansas / KCMO local jurisdiction |
| Default deposit | 25% on quotes over $1,500 |
| Quote expiration | 30 days |
| Invoice terms | Due on completion (Net-15 for repeat customers) |
| Quote template footer | "Free quotes · Owner-operated · Tracked Bobcat equipment · Insured" |

## Import Notes (CSV Compatibility)

- **Numeric-only** Base Price and Minimum Charge fields (e.g. `145.00`, `850.00`) — no $ symbols or commas.
- Add-ons listed in the CSV are separated with semicolons (`;`). If Jobber expects comma-separated add-ons, replace `;` with `,`.
- Internal Notes contain margin and operational guidance — they should never be exposed to the customer.
- Material Spreading is **not** included as a stand-alone customer-facing service; it is bundled inside Driveway Refresh, Light Grading, and other applicable services.
- Minor Drainage Correction is filed under **Specialty / Project Services** and is intentionally de-emphasized in residential-facing marketing.
- Driveway Culvert Repair was added in Revision 2 — it lives under **Driveway & Gravel**.