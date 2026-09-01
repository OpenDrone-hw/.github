# OpenDrone release standard

OpenDrone release policy is public product policy. Incutec supplies the
hardware-management software that executes it; individual product repositories
remain the source of their designs, revisions, and product-specific scripts.

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

From the Incutec workspace root, run the hardware-agnostic release manager with
the OpenDrone approval data and the board's explicit approval key:

```sh
python3 scripts/hardware/release/kicad_release.py \
  OpenDrone/hardware/<repo>/hardware/<board>.kicad_pcb \
  --approved-violations OpenDrone/_org-github/engineering/approved-violations.json \
  --approval-key <repo>/hardware/<board>
```

The preparation chain:

1. Generates ERC and DRC reports and compares them with approved findings.
2. Blocks missing or invalid 3D models that affect export.
3. Generates and checks the fabrication set.
4. Exports the board STEP model.
5. Exports the schematic PDF.

These are preparation steps, not publication or production authorization.

## Human release decisions

A maintainer selects the release scope and revision, reviews any changed
finding, checks the generated artifacts, and confirms the product documentation
and render set. Tagging, publishing a GitHub release, updating the storefront,
ordering, programming, or operating hardware requires its own explicit action.

Board-specific scripts stay in that board repository. OpenDrone-wide written
standards and approved portfolio configuration stay in this organization
repository. Reusable implementations stay with Incutec.
