---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491171"
---
# Get-AzureRmContext

## Áttekintés
Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.

## SZINTAXISA

```
Get-AzureRmContext [<CommonParameters>]
```

## Leírás
A Get-AzureRmContext parancsmag az Azure Resource Manager-kérések hitelesítéséhez használt jelenlegi metaadatot kapja meg.

Ez a parancsmag az Active Directory-fiókot, az Active Directory-bérlőt, az Azure-előfizetést és a célzott Azure-környezetet kapja meg.
Az Azure Resource Manager-parancsmagok alapértelmezés szerint ezeket a beállításokat használják az Azure Resource Manager-kérések készítésekor.

## Példák

### Példa 1: a jelenlegi környezet beszerzése
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Ebben a példában egy Azure-előfizetéssel jelentkezik be a fiókba a AzureRmAccount használatával, és az aktuális munkamenet kontextusát a Get-AzureRmContext.

## PARAMÉTEREK

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSAzureContext
Ez a parancsmag az Azure Resource Manager-parancsmagok által használt fiókot, bérlőt és előfizetést számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRMContext]()

