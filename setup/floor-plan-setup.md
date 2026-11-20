---
label: Floor Plan Setup
icon: location
order: 600
description: Manage floor-plan metadata and find the resource-link editor in the HXA.io Portal.
---

# Floor Plan Setup

Open **Floor Plans** in the [HXA.io Portal](https://portal.hxa.io). The overview provides **Create new floor plan**, **Search**, **Filter**, and **Columns option**.

The table lists **ID**, **Display Name**, **Floor label**, **Country**, **City**, **Street and building number**, **Floor**, and **Date of last change**.

## Edit floor metadata

1. Find the intended floor plan and open **Options > Edit floor plan**.
2. Review **Display Name**, **Floor label**, **Country**, **City**, **Street and Building Number**, and **Floor**.
3. Use **Save floor plan** for intended changes, or **Back** to return to the overview.

The numeric Floor and the descriptive Floor label are separate fields.

## Open resource-link editing

The Options menu contains a separate **Edit floor plan links** action. Use it for the resource-link workflow rather than the metadata form.

This workflow requires a **Microsoft Entra ID connector**. If the portal displays **Please add a Microsoft Entra ID Connector**, configure that connector before continuing. See [Connector Setup](/setup/connector-setup/connector-setup.md).

## Enable floor plans in resource displays

| Application | Resource setting |
| --- | --- |
| Room Booking | Advanced settings > Dashboard settings > Enable floor plan |
| Room Board | Advanced settings > Enable floor plan; review Table View Configuration as well |

After configuring resource links and display settings, verify that the intended map and resources appear in the application. See also [Sparo User Documentation](/usage/sparo-user-documentation.md).

<!-- Source: portal inspection, 2026-11-20, P12, P04, P05. The link editor, upload workflow, formats, drawing tools, and client rendering could not be inspected because of the missing Entra connector. -->
