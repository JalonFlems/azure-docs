---
title: Troubleshooting Elastic
description: This article provides information about troubleshooting Elastic integration with Azure
ms.topic: conceptual
ms.date: 01/06/2023
author: flang-msft
ms.author: franlanglois
---

# Troubleshooting Elastic integration with Azure

This document contains information about troubleshooting your solutions that use Elastic.

## Unable to create an Elastic resource

Elastic integration with Azure can only be set up by users who have *Owner* or *Contributor* access on the Azure subscription. [Confirm that you have the appropriate access](/azure/role-based-access-control/check-access).

## Logs not being emitted to Elastic

- Only resources listed in [Azure Monitor resource log categories](../../azure-monitor/essentials/resource-logs-categories.md) emit logs to Elastic. To verify whether the resource is emitting logs to Elastic:
    1. Navigate to [Azure diagnostic setting](../../azure-monitor/essentials/diagnostic-settings.md) for the resource. 
    1. Verify that there's a diagnostic setting option available.

    :::image type="content" source="media/troubleshoot/check-diagnostic-setting.png" alt-text="Verify diagnostic setting":::

- Resource doesn't support sending logs. Only resource types with monitoring log categories can be configured to send logs. For more information, see [supported categories](/azure/azure-monitor/essentials/resource-logs-categories).

- Limit of five diagnostic settings reached. Each Azure resource can have a maximum of five diagnostic settings. For more information, see [diagnostic settings](/azure/azure-monitor/essentials/diagnostic-settings?tabs=portal)

- Export of Metrics data is not supported currently by the partner solutions under Azure Monitor diagnostic settings. 


## Purchase errors

* Purchase fails because a valid credit card isn't connected to the Azure subscription or a payment method isn't associated with the subscription.

  Use a different Azure subscription. Or, add or update the credit card or payment method for the subscription. For more information, see [updating the credit and payment method](/azure/cost-management-billing/manage/change-credit-card).

* The EA subscription doesn't allow Marketplace purchases.

  Use a different subscription. Or, check if your EA subscription is enabled for Marketplace purchase. For more information, see [Enable Marketplace purchases](/azure/cost-management-billing/manage/ea-azure-marketplace#enabling-azure-marketplace-purchases).


## Get support

To contact support about the Elastic integration with Azure, select the **New Support request** in the left pane. Select **Open an Elastic Support ticket**.

:::image type="content" source="media/troubleshoot/open-ticket.png" alt-text="Open support ticket":::

In the Elastic site, open a support request.

:::image type="content" source="media/troubleshoot/elastic-support.png" alt-text="Open Elastic support":::

## Next steps

Learn about [managing your instance](manage.md) of Elastic.
