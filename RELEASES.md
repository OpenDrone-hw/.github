# OpenDrone release standard

OpenDrone release policy is public product policy. Individual product
repositories remain the source of their designs, revisions, validation
commands, and product-specific scripts.

## Design reports

Every release runs ERC and DRC, including schematic parity and refilled zones.
The reports do not need to be empty. OpenDrone boards intentionally carry some
findings that have been reviewed and accepted.

[`engineering/approved-violations.json`](engineering/approved-violations.json)
records the maximum approved count for each finding type and board. A release
passes when every reported finding is already approved and its count is no
higher than the recorded maximum. Fewer findings pass. A new type or increased
count stops release preparation until a maintainer reviews the report; approval
is never inferred from an earlier board or a similar circuit.

## Preparation chain

Use the validation commands documented in the product repository. Release
preparation must then:

1. Generate ERC and DRC reports and compare them with approved findings.
2. Block missing or invalid 3D models that affect export.
3. Generate and check the fabrication set.
4. Export the board STEP model.
5. Export the schematic PDF.

These are preparation steps, not publication or production authorization.

## Human release decisions

A maintainer selects the release scope and revision, reviews any changed
finding, checks the generated artifacts, and confirms the product documentation
and render set. Tagging, publishing a GitHub release, updating the storefront,
ordering, programming, or operating hardware requires its own explicit action.

Board-specific scripts stay in that board repository. OpenDrone-wide written
standards and approved portfolio configuration stay in this organization
repository.
