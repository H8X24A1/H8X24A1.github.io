---
title: Exchange Hybrid - HXA.io DOCS
label: Exchange Hybrid
icon: server
order: 1000
---

# Exchange Hybrid

A hybrid deployment allows organizations to extend the feature-rich experience and administrative authority they have with their existing on-premises Microsoft Exchange organization to the cloud. A hybrid exchange deployment provides the seamless look and feel of a single Exchange organization between an on-premises Exchange organization and Exchange Online. In addition, a hybrid deployment can serve as an intermediate step to moving to an Exchange Online organization.

1. Prepare the on-premises Exchange environment: Before you can configure Exchange Hybrid, you need to ensure that your on-premises Exchange environment is up to date and configured correctly. This includes verifying that all Exchange servers are running a supported version of Exchange Server and that the Active Directory schema is up to date.

2. Configure Exchange Hybrid in the Exchange Admin Center: Exchange Hybrid is configured through the Exchange Admin Center (EAC) in Office 365. You will need to log in to the EAC with your Office 365 tenant administrator account and navigate to the Hybrid tab to begin the configuration process.

3. Configure hybrid connectivity: The first step in configuring Exchange Hybrid is to establish hybrid connectivity between your on-premises Exchange environment and Exchange Online. This involves creating a hybrid deployment object in the EAC and configuring the hybrid configuration wizard.

4. Configure mail flow: Once hybrid connectivity is established, you need to configure mail flow between the on-premises Exchange environment and Exchange Online. This involves configuring send and receive connectors in both environments and configuring mail flow rules to ensure that messages are routed correctly.

5. Configure directory synchronization: To ensure that user accounts and other directory objects are synchronized between your on-premises environment and Exchange Online, you need to configure directory synchronization. This involves setting up Azure Active Directory Connect and configuring directory synchronization between your on-premises Active Directory and Azure Active Directory.

6. Migrate mailboxes: Once all of the above steps are complete, you can begin migrating mailboxes from your on-premises Exchange environment to Exchange Online. This can be done using a variety of migration methods, including cutover migration, staged migration, or hybrid migration.

7. Monitor and manage the hybrid environment: After the migration is complete, you will need to monitor and manage the hybrid environment to ensure that it continues to function properly. This includes monitoring mail flow, managing user accounts, and troubleshooting any issues that may arise.

Overall, configuring Exchange Hybrid requires careful planning and attention to detail, as well as a solid understanding of both the on-premises Exchange environment and Exchange Online. Microsoft provides detailed documentation and tools to help organizations configure Exchange Hybrid, but it's still important to have a clear understanding of the process and the requirements involved.

### Sources

[!ref target="blank" text="Exchange Hybrid"](https://docs.microsoft.com/en-us/exchange/exchange-hybrid)


