---
title: Azure-előfizetések kezelése az Azure PowerShell-lel
description: Azure-előfizetések kezelése az Azure PowerShell-lel
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 0c4361bbe34df79f5d940d2b14377d0ceef5fcd8
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243276"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="9796f-103">Több Azure-előfizetés kezelése</span><span class="sxs-lookup"><span data-stu-id="9796f-103">Manage multiple Azure subscriptions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="9796f-104">Ha még csak most kezd ismerkedni az Azure-ral, valószínűleg egyetlen előfizetéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="9796f-104">If you're brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="9796f-105">Ha azonban már egy ideje használja az Azure-t, előfordulhat, hogy már több Azure-előfizetést is létrehozott.</span><span class="sxs-lookup"><span data-stu-id="9796f-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="9796f-106">Az Azure PowerShellt beállíthatja, hogy egy adott előfizetésen hajtsa végre a parancsokat.</span><span class="sxs-lookup"><span data-stu-id="9796f-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="9796f-107">Kérje le a fiókban lévő összes előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="9796f-107">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="9796f-108">Adja meg az alapértelmezett fiókot.</span><span class="sxs-lookup"><span data-stu-id="9796f-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="9796f-109">Ellenőrizze a módosítást a `Get-AzureRmContext` parancsmag futtatásával.</span><span class="sxs-lookup"><span data-stu-id="9796f-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="9796f-110">Miután beállította az alapértelmezett előfizetést, az összes Azure PowerShell-parancs az adott előfizetésen fut majd.</span><span class="sxs-lookup"><span data-stu-id="9796f-110">Once you set your default subscription, all Azure PowerShell commands run against this subscription.</span></span>
