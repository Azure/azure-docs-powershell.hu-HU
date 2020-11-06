---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491164"
---
# Get-AzureRmTenant

## Áttekintés
Az aktuális felhasználótól kapott bérlői fiókokat kapja.

## SZINTAXISA

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## Leírás
A Get-AzureRmTenant parancsmag az aktuális felhasználóhoz tartozó bérlői fiókokat kapja meg.

## Példák

### Példa 1: az összes bérlő beszerzése
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

Ebben a példában bemutatjuk, hogy miként szerezheti be az Azure-fiókok összes hivatalos bérlőjét.

### 2. példa: adott bérlő beszerzése
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

Ebben a példában bemutatjuk, hogyan lehet egy Azure-fiók meghatalmazott bérlői fiókját beszerezni.

## PARAMÉTEREK

### -Bérlői azonosító megkeresése
Annak a bérlőnek az AZONOSÍTÓját adja meg, akinek a parancsmagja van.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSAzureTenant
Ez a parancsmag a bérlői azonosítót és a kapcsolódó tartomány adatait számítja ki az aktuális fiókhoz engedélyezett bérlői fiókhoz.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

