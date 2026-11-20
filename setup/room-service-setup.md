---
label: Room Service Setup
icon: hubot
order: 500
---

# Room Service Setup

Room Service combines a central catalog with activation on each Room Booking resource. Configure categories and articles first, then choose which articles and devices should offer the service.

## Requirements

- Access to the Room service and resource-configuration areas in the [HXA.io Portal](https://portal.hxa.io).
- A configured [Room Booking resource](/setup/resource-setup/room-booking-setup/resource-setup.md) with a connected display.
- The appropriate Room Service add-on license assigned to the resource. See [License Assignment](/license/assign-license.md).
- The email recipients intended to receive orders.

## Create categories

1. Open **Room service > Category**.
2. Choose **Add category**.
3. Fill in the required **Name** and **Sorting** fields.
4. Use **Save** and check the entry in the overview.

The category overview lists **Category name** and **Sorting**, with an Options menu for each entry.

## Add catalog items

1. Open **Room service > Item**.
2. Choose **Add item**.
3. Enter **Item**, choose **Category** and **Symbol**, and set **Sorting in the category**.
4. Review **Show price** and the pricing controls offered by the form if you want prices displayed.
5. Use **Save** and check the article in the overview.

The overview includes **Item Name**, **Category**, **Price**, **Symbol**, and **Sorting**. Creating an article in the central catalog is separate from activating it on a resource.

## Activate Room Service on a resource

1. Open **Resources > Options > Edit Resource** for the intended Room Booking resource.
2. Review the assigned license under **Licensing - Add-ons**.
3. Find **Add-On Licenses** and select **Room Service**.
4. Use **Manage Devices** to choose the displays on which the Room Service module should be activated.
5. Enter **E-mail recipient for orders** and, if needed, **E-mail copy recipient for orders**.
6. Review the article table and select the intended entries in **Activate**. The table identifies each article by Item Name, Item category, and Item price.
7. Use the Room Service section's **Save and Update** button.

## Verify the setup

Reopen the resource to check the retained device, recipient, and article configuration. On an enabled display, check that the intended articles are offered. Arrange a test order with the receiving service team to verify delivery and any displayed prices.

<!-- Sources: authenticated portal inspection, 2026-11-20, P05–P07; existing Room Service add-on release notes. Empty category/item forms and an existing resource configuration were inspected. Creation, price controls after enabling Show price, device selection, saving, and order delivery were not tested. -->
