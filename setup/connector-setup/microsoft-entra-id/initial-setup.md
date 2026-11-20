# Microsoft Entra ID Connector: Initial Setup

The **Microsoft Entra ID (Microsoft 365 Azure Active Directory)** connector supports directory integration for HXA Sparo. The floor-plan resource-link editor also requires an Entra ID connector.

## Open the setup panel

1. Sign in to the [HXA.io Portal](https://portal.hxa.io).
2. Open **Connectors > Create connector**.
3. Locate **Microsoft Entra ID (Microsoft 365 Azure Active Directory)**.
4. Use **Connect** on that tile.

The next panel provides a single account-type option: **Application Account**. It also contains **Connect** and **Back**.

When configuring the connection, select **Application Account** and use the panel's **Connect** button to continue with Microsoft authentication and authorization. Review the permissions requested for the intended tenant before approving them. **Back** returns to connector selection without submitting the setup.

## Review the connector and continue setup

After completing authorization, locate the connector in **Connectors** and review its Type, Application, Registered from, and Status.

| Next task | Documentation |
| --- | --- |
| Import users and assign HXA Sparo licenses | [User Setup](/setup/user-setup.md), [License Assignment](/license/assign-license.md) |
| Find group creation and directory import | [Groups](/setup/user-setup.md#groups) |
| Open floor-plan resource links | [Floor Plan Setup](/setup/floor-plan-setup.md) |
| Investigate connection errors | [Event Logs](/maintenance/event-logs.md) |

The resource-calendar connector and the Entra ID connector serve different setup tasks. For Room Booking and Room Board calendar access through Microsoft 365, see [Microsoft 365 Resources Setup](/setup/connector-setup/microsoft-365/initial-setup.md).
