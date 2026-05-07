# Jobber Category & Service Setup Guide

**Source:** PRICING_MANUAL.md (Section 2 — Jobber Pricebook Structure)

Use this guide to create the categories and services in Jobber's *Products & Services* library. Service names below are formatted to copy directly into Jobber's *Service Name* field.

## Setup Order

1. Create all 8 categories first (in the order listed below).
2. Import `jobber_pricebook.csv` to populate services in bulk, OR add each service manually using the names below.
3. After services are created, paste the customer description from `jobber_pricebook.csv` into each service's *Description* field.
4. Paste the internal note into the *Internal Notes* field (not visible to customers).
5. Set the unit type and base price per the CSV.

## Categories & Services

### 1. Driveway & Gravel

- Gravel Driveway Refresh - Standard
- Gravel Spread - Customer-Supplied Material
- Pothole Repair - Per Pothole
- Driveway Grading & Reshaping

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
- Minor Drainage Correction
- Material Spreading - Mulch / Topsoil / Decorative Rock

### 6. Demolition

- Small Demolition - Sheds & Outbuildings
- Fence Removal

### 7. Hourly / Skid Steer

- Skid Steer + Operator - Hourly
- Half Day Skid Steer
- Full Day Skid Steer

### 8. Service Bundles

- Rural Property Cleanup Package
- Driveway Refresh Package
- Fence Line Recovery Package
- Storm Cleanup Package
- Acreage Maintenance - Per Visit
- Acreage Maintenance - 3-Visit Seasonal

## Quick Reference: Total Counts

- **Categories:** 8
- **Services:** 27

## Recommended Jobber Settings

| Setting | Recommendation |
|---|---|
| Default tax rate | Apply per Kansas / KCMO local jurisdiction |
| Default deposit | 25% on quotes over $1,500 |
| Quote expiration | 30 days |
| Invoice terms | Due on completion (Net-15 for repeat customers) |
| Job tags | Driveway, Cleanup, Mowing, Storm, Demolition, Stump, Bundle |
| Custom fields | Acreage, Density, Drive Length (ft), Pile Count, Stump Count |

## Import Notes

- The pricebook CSV uses plain dollar amounts (e.g. `$145.00`). If Jobber's importer expects pure numeric values, run a find/replace to strip the `$` and `,` characters before import.
- Add-ons listed in the CSV are separated with semicolons (`;`). If Jobber expects comma-separated add-ons, replace `;` with `,`.
- Internal Notes contain margin and operational guidance — they should never be exposed to the customer.