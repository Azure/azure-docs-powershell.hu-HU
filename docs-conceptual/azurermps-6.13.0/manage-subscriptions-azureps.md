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
# <a name="manage-multiple-azure-subscriptions"></a>Több Azure-előfizetés kezelése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Ha még csak most kezd ismerkedni az Azure-ral, valószínűleg egyetlen előfizetéssel rendelkezik. Ha azonban már egy ideje használja az Azure-t, előfordulhat, hogy már több Azure-előfizetést is létrehozott. Az Azure PowerShellt beállíthatja, hogy egy adott előfizetésen hajtsa végre a parancsokat.

1. Kérje le a fiókban lévő összes előfizetés listáját.

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

2. Adja meg az alapértelmezett fiókot.

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. Ellenőrizze a módosítást a `Get-AzureRmContext` parancsmag futtatásával.

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

Miután beállította az alapértelmezett előfizetést, az összes Azure PowerShell-parancs az adott előfizetésen fut majd.
