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
ms.openlocfilehash: 8869b700e513d6fc07e69de1dbfe852bd2a52df1
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211060"
---
# <a name="manage-multiple-azure-subscriptions"></a>Több Azure-előfizetés kezelése

Ha még csak most kezd ismerkedni az Azure-ral, valószínűleg egyetlen előfizetéssel rendelkezik. Ha azonban már egy ideje használja az Azure-t, előfordulhat, hogy már több Azure-előfizetést is létrehozott. Az Azure PowerShellt beállíthatja, hogy egy adott előfizetésen hajtsa végre a parancsokat.

1. Kérje le a fiókban lévő összes előfizetés listáját.

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

2. Adja meg az alapértelmezett fiókot.

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. Ellenőrizze a módosítást a `Get-AzureRmContext` parancsmag futtatásával.

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

Miután beállította az alapértelmezett előfizetést, az összes Azure PowerShell-parancs az adott előfizetésen fut majd.
