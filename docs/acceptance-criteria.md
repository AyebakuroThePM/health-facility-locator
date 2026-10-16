# Acceptance Criteria — Health Facility Locator

## 1. Document Information

| Item | Details |
|---|---|
| Project | Health Facility Locator with Google Maps Integration |
| Document Type | Acceptance Criteria |
| Project Manager | Oruwori Ayebakuro |
| Version | 1.0 |
| Status | Draft — Pending Review |

## 2. Purpose

This document defines the conditions that must be met before the Health Facility Locator feature can be accepted. It provides a shared basis for developer reviews, functional testing, defect resolution, and final handover.

## 3. Acceptance Criteria

### AC-01: Map Display

- The map loads successfully when valid configuration and network access are available.
- Available facilities appear as identifiable markers.
- The map displays an appropriate error message if the mapping service fails.

**Verification:** Demonstrate the map with a valid configuration and sample facility records.

### AC-02: Location Search

- Users can search using an agreed address or place-name input.
- Search results correspond to the selected location.
- Invalid or unsuccessful searches produce clear feedback.

**Verification:** Test valid, invalid, and unmatched search inputs.

### AC-03: Current Location

- Users are asked for permission before the feature accesses their current location.
- When permission is granted, the feature uses the available location appropriately.
- When permission is denied or unavailable, manual location search remains usable.

**Verification:** Test both granted and denied location-permission scenarios.

### AC-04: Facility Categories

- Users can filter results by hospitals, clinics, laboratories, and pharmacies.
- Results reflect the selected category.
- Users can change or clear their selection.

**Verification:** Test each category against a dataset containing known facility types.

### AC-05: Service Filters

- Users can filter facilities by configured services such as immunization, radiology, and laboratory testing.
- Facilities without a matching service are excluded from filtered results.
- Missing service information is not presented as a confirmed service offering.

**Verification:** Test filters using sample records with matching, non-matching, and missing service information.

### AC-06: Facility Details

- Selecting a facility displays its available name, address, category, and service information.
- Contact information appears when available.
- Missing information is handled clearly without breaking the interface.

**Verification:** Select sample facilities with complete and incomplete records.

### AC-07: Results and Distance

- Matching facilities appear in a results list alongside the map.
- Selecting a result identifies the corresponding facility on the map.
- Distance is displayed only when it can be calculated reliably from valid location data.

**Verification:** Compare the results list with the map markers and test records with valid and missing coordinates.

### AC-08: Directions

- Users can open Google Maps directions for a selected facility.
- The destination uses valid coordinates or an appropriate address.
- Facilities without usable destination information provide clear feedback.

**Verification:** Open directions for a sample facility and inspect the destination.

### AC-09: Responsive Interface

- The feature remains usable at agreed desktop and mobile viewport sizes.
- Search controls, filters, map, and results remain accessible.
- Content and controls do not overlap in ways that prevent normal use.

**Verification:** Test the agreed viewport sizes using browser developer tools or supported devices.

### AC-10: Error Handling

- Empty searches display a helpful message.
- Denied location permission does not prevent manual search.
- Network or mapping API errors are handled gracefully.
- Loading indicators and error messages are understandable.

**Verification:** Simulate the agreed error scenarios and record the results.

### AC-11: Security and Privacy

- No real API keys, passwords, or other secrets are committed to the public repository.
- API keys are restricted appropriately for their intended use.
- Location access requires permission where applicable.
- Unnecessary collection or storage of location information is avoided.

**Verification:** Review the repository, configuration, application behaviour, and relevant implementation documentation.

### AC-12: Documentation and Handover

- The source code is committed to the designated repository.
- Setup and execution instructions are documented.
- Required environment variables are described without exposing real secret values.
- Required Google Maps services and configuration steps are documented.
- Test results and known limitations are provided.
- Outstanding defects are recorded and agreed upon before final approval.

**Verification:** Follow the setup instructions and review the handover materials.

## 4. Defect Classification

| Severity | Description | Acceptance approach |
|---|---|---|
| Critical | Security exposure or a failure that makes the feature unusable | Must be resolved before acceptance |
| High | A core requirement such as search, filtering, or directions does not work | Must be resolved before acceptance |
| Medium | A non-critical function or interaction is defective | Resolve or obtain explicit approval for a documented exception |
| Low | Minor cosmetic issue with no material impact on usability | Record and agree on resolution timing |

## 5. Final Acceptance Conditions

The feature may be recommended for acceptance when:

1. All agreed functional acceptance criteria have been demonstrated.
2. Required tests have been completed and their results documented.
3. Critical and high-severity defects have been resolved.
4. Any outstanding lower-severity defects have been documented and explicitly agreed upon.
5. The code review is complete and approved changes have been merged into the designated branch.
6. Documentation and required configuration instructions have been handed over.
7. Any scope changes have been approved and reflected in the final deliverables.

## 6. Acceptance Record

**Review date:** To be completed.

**Review outcome:** Pending testing.

**Outstanding defects:** To be recorded during testing.

**Project Manager decision:** Pending evidence review.

**Final status:** Not yet accepted.
