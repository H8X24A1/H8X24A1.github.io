## Introduction

The Event Log on HXA.io is an essential tool for administrators seeking to monitor and manage the performance of their connectors. It provides detailed information about the status and health of each connector, helping administrators identify and resolve potential issues. This article will explore the types of error messages found in the Event Log and offer guidance on how to address common connector problems such as reachability, connection, and authentication failures.

## Open the event log

In the [HXA.io Portal](https://portal.hxa.io), choose **Settings > Event log**. The page is labeled **Event log | Overview** and **Event display for error analysis**. It provides **Search**, **Filter**, **Columns option**, and sortable table headings.

| Column | Information |
| --- | --- |
| ID | Event identifier |
| Method | Method recorded for the operation |
| Path | Recorded request or operation path |
| Connector ID | Related connector identifier, where recorded |
| Status | Status recorded for the operation |
| Date | Event timestamp displayed by the portal |

## Filter events

Open **Filter** to specify **ID**, **Method**, **Path**, **Connector ID**, and **Status**. Method is a selection field.

For dates, choose **Static date** or **Date Range**, then fill in **Date** and, for a range, **End**. The dialog shows **DD/MM/YYYY**. Use **Apply** for the selected filters or **Reset** to clear them.

Identify a resource's connector under **Resources > Edit Resource > Connector**, then match that ID in the event log. You can also find it in the [Connectors overview](/setup/connector-setup/connector-setup.md).

### What is the Event Log on HXA.io?

The Event Log is a central repository that records critical information about events and activities occurring within the HXA.io platform. It serves as a valuable resource for troubleshooting and diagnosing issues related to connectors, which are responsible for facilitating communication between HXA.io and external systems. By reviewing the Event Log, administrators can gain insights into the operational status of their connectors and take appropriate action to resolve issues as they arise.

## Troubleshooting categories

The following headings describe common classes of connector problems. They are explanatory categories, not a complete list of exact portal messages or status codes. Use the Method, Path, Status, and Connector ID actually recorded for the event when investigating an issue.

+++ Connector Not Reachable:
This error indicates that the connector is not accessible due to a network issue, server downtime, or other connectivity problems. The message may also provide additional information about the cause of the issue.
+++

+++ Connection Not Allowed:
This error occurs when a connector is unable to establish a connection with the external system, often due to security or firewall settings. The error message will typically include details about the specific connection issue.
+++

+++ Authentication Not Successful:
This error arises when the connector fails to authenticate with the external system, usually because of incorrect or expired credentials. The error message will provide information about the authentication failure and suggest potential solutions.
+++
## Troubleshooting Connector Issues

To resolve connector issues identified in the Event Log, follow these steps:

### Verify Connectivity:
Check the connector's configuration settings to ensure they are accurate and up-to-date. Verify that the external system is online and reachable, and that the connector's IP address is whitelisted in the external system's firewall, if applicable.

### Review Security Settings:
Examine the security settings of the external system and ensure that the connector is granted the necessary permissions to establish a connection. Update any outdated settings, if required.

### Check Credentials:
Confirm that the connector's authentication credentials (e.g., username, password, API key, or access token) are correct and have not expired. Update the credentials if necessary and reattempt the connection.

### Consult Documentation:
Refer to the connector's documentation for specific troubleshooting steps, as certain issues may be unique to the particular connector.

### Contact Support:
If the issue persists, reach out to HXA.io's support team for assistance. Provide a detailed description of the problem, including relevant error messages from the Event Log and any steps you have already taken to address the issue.

## Conclusion

The Event Log on HXA.io is a valuable resource for monitoring and troubleshooting connector issues. By regularly reviewing the log and addressing error messages related to reachability, connection, and authentication, administrators can ensure the optimal performance of their connectors and maintain seamless communication between HXA.io and external systems.
