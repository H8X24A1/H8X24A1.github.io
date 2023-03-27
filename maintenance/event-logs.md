---
label: Event Logs
icon: history
order: 1000
---
## Introduction

The Event Log on HXA.io is an essential tool for administrators seeking to monitor and manage the performance of their connectors. It provides detailed information about the status and health of each connector, helping administrators identify and resolve potential issues. This article will explore the types of error messages found in the Event Log and offer guidance on how to address common connector problems such as reachability, connection, and authentication failures.

## What is the Event Log on HXA.io?

The Event Log is a central repository that records critical information about events and activities occurring within the HXA.io platform. It serves as a valuable resource for troubleshooting and diagnosing issues related to connectors, which are responsible for facilitating communication between HXA.io and external systems. By reviewing the Event Log, administrators can gain insights into the operational status of their connectors and take appropriate action to resolve issues as they arise.

## Types of Error Messages in the Event Log

The Event Log contains various types of error messages, some of which are specific to connectors. Here are the most common connector-related error messages:

+++
# Connector Not Reachable:
This error indicates that the connector is not accessible due to a network issue, server downtime, or other connectivity problems. The message may also provide additional information about the cause of the issue.
+++

+++
# Connection Not Allowed:
This error occurs when a connector is unable to establish a connection with the external system, often due to security or firewall settings. The error message will typically include details about the specific connection issue.
+++

+++
# Authentication Not Successful:
This error arises when the connector fails to authenticate with the external system, usually because of incorrect or expired credentials. The error message will provide information about the authentication failure and suggest potential solutions.
+++
## Troubleshooting Connector Issues

To resolve connector issues identified in the Event Log, follow these steps:

# Verify Connectivity:
Check the connector's configuration settings to ensure they are accurate and up-to-date. Verify that the external system is online and reachable, and that the connector's IP address is whitelisted in the external system's firewall, if applicable.

# Review Security Settings:
Examine the security settings of the external system and ensure that the connector is granted the necessary permissions to establish a connection. Update any outdated settings, if required.

# Check Credentials:
Confirm that the connector's authentication credentials (e.g., username, password, API key, or access token) are correct and have not expired. Update the credentials if necessary and reattempt the connection.

# Consult Documentation:
Refer to the connector's documentation for specific troubleshooting steps, as certain issues may be unique to the particular connector.

# Contact Support:
If the issue persists, reach out to HXA.io's support team for assistance. Provide a detailed description of the problem, including relevant error messages from the Event Log and any steps you have already taken to address the issue.

## Conclusion

The Event Log on HXA.io is a valuable resource for monitoring and troubleshooting connector issues. By regularly reviewing the log and addressing error messages related to reachability, connection, and authentication, administrators can ensure the optimal performance of their connectors and maintain seamless communication between HXA.io and external systems.