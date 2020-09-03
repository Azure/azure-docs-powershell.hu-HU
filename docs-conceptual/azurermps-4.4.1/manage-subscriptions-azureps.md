---
title: Azure-előfizetések kezelése az Azure PowerShell-lel | Microsoft Docs
description: Azure-előfizetések kezelése az Azure PowerShell-lel
keywords: Azure PowerShell, előfizetés
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: d2674e37a211d1c1896a13e234cda95beea4479a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243990"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="bc969-104">Több Azure-előfizetés kezelése</span><span class="sxs-lookup"><span data-stu-id="bc969-104">Manage multiple Azure subscriptions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="bc969-105">Ha még csak most kezd ismerkedni az Azure-ral, valószínűleg egyetlen előfizetéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="bc969-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="bc969-106">Ha azonban már egy ideje használja az Azure-t, előfordulhat, hogy már több Azure-előfizetést is létrehozott.</span><span class="sxs-lookup"><span data-stu-id="bc969-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="bc969-107">Az Azure PowerShellt beállíthatja, hogy egy adott előfizetésen hajtsa végre a parancsokat.</span><span class="sxs-lookup"><span data-stu-id="bc969-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="bc969-108">Kérje le a fiókban lévő összes előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="bc969-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
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

2. <span data-ttu-id="bc969-109">Adja meg az alapértelmezett fiókot.</span><span class="sxs-lookup"><span data-stu-id="bc969-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="bc969-110">Ellenőrizze a módosítást a `Get-AzureRmContext` parancsmag futtatásával.</span><span class="sxs-lookup"><span data-stu-id="bc969-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
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

<span data-ttu-id="bc969-111">Miután beállította az alapértelmezett előfizetést, az összes Azure PowerShell-parancs az adott előfizetésen fut majd.</span><span class="sxs-lookup"><span data-stu-id="bc969-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
