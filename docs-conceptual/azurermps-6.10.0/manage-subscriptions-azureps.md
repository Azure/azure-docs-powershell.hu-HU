---
title: Azure-előfizetések kezelése az Azure PowerShell-lel
description: Azure-előfizetések kezelése az Azure PowerShell-lel
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 3f1c1bab5f9903ee7df813bf1ef043c7107ebe79
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399127"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="c9c15-103">Több Azure-előfizetés kezelése</span><span class="sxs-lookup"><span data-stu-id="c9c15-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="c9c15-104">Ha még csak most kezd ismerkedni az Azure-ral, valószínűleg egyetlen előfizetéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c9c15-104">If you're brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="c9c15-105">Ha azonban már egy ideje használja az Azure-t, előfordulhat, hogy már több Azure-előfizetést is létrehozott.</span><span class="sxs-lookup"><span data-stu-id="c9c15-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="c9c15-106">Az Azure PowerShellt beállíthatja, hogy egy adott előfizetésen hajtsa végre a parancsokat.</span><span class="sxs-lookup"><span data-stu-id="c9c15-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="c9c15-107">Kérje le a fiókban lévő összes előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="c9c15-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. <span data-ttu-id="c9c15-108">Adja meg az alapértelmezett fiókot.</span><span class="sxs-lookup"><span data-stu-id="c9c15-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="c9c15-109">Ellenőrizze a módosítást a `Get-AzureRmContext` parancsmag futtatásával.</span><span class="sxs-lookup"><span data-stu-id="c9c15-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="c9c15-110">Miután beállította az alapértelmezett előfizetést, az összes Azure PowerShell-parancs az adott előfizetésen fut majd.</span><span class="sxs-lookup"><span data-stu-id="c9c15-110">Once you set your default subscription, all Azure PowerShell commands run against this subscription.</span></span>
