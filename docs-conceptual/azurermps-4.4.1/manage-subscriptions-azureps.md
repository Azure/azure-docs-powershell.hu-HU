---
title: Azure-előfizetések kezelése az Azure PowerShell-lel | Microsoft Docs
description: Azure-előfizetések kezelése az Azure PowerShell-lel
keywords: Azure PowerShell, előfizetés
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 12e304f32f585c1af40d20579cd46999e0a12395
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52827479"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="cb4fb-104">Több Azure-előfizetés kezelése</span><span class="sxs-lookup"><span data-stu-id="cb4fb-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="cb4fb-105">Ha még csak most kezd ismerkedni az Azure-ral, valószínűleg egyetlen előfizetéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="cb4fb-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="cb4fb-106">Ha azonban már egy ideje használja az Azure-t, előfordulhat, hogy már több Azure-előfizetést is létrehozott.</span><span class="sxs-lookup"><span data-stu-id="cb4fb-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="cb4fb-107">Az Azure PowerShellt beállíthatja, hogy egy adott előfizetésen hajtsa végre a parancsokat.</span><span class="sxs-lookup"><span data-stu-id="cb4fb-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="cb4fb-108">Kérje le a fiókban lévő összes előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="cb4fb-108">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="cb4fb-109">Adja meg az alapértelmezett fiókot.</span><span class="sxs-lookup"><span data-stu-id="cb4fb-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="cb4fb-110">Ellenőrizze a módosítást a `Get-AzureRmContext` parancsmag futtatásával.</span><span class="sxs-lookup"><span data-stu-id="cb4fb-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="cb4fb-111">Miután beállította az alapértelmezett előfizetést, az összes Azure PowerShell-parancs az adott előfizetésen fut majd.</span><span class="sxs-lookup"><span data-stu-id="cb4fb-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
