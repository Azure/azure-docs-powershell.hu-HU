---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
ms.openlocfilehash: 1274b04ed85917a9c1e185bfbef6307eaedecc05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849498"
---
# Get-AzureRmProviderOperation

## Áttekintés
Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az Get-AzureRmProviderOperation az Azure Resource Providers által kitett műveleteket kapja meg.
A műveletek létrehozhatók egyéni szerepkörök az Azure RBAC-ban.
A parancs beírja a kívánt műveleti keresési karakterláncot (esetleges helyettesítő *karakterrel ()), amely meghatározza a megjelenítendő műveletek részleteit. A Get-AzureRmProviderOperation * segítségével minden Azure Resource Provider művelethez hozzáférhet. Használja Get-AzureRmProviderOperation Microsoft. kiszámítás/* a Microsoft összes műveletének beszerzése lehetőséget.

## Példák

### Minden művelet beolvasása minden szolgáltatónál
```
PS C:\> Get-AzureRmProviderOperation *
```

### Műveletek beszerzése egy adott erőforrás-szolgáltatónál
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### A virtuális gépeken végezhető műveletek beolvasása
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
A művelet keresési karakterlánca (esetleges helyettesítő karakterekkel (*)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
Paraméterek: OperationSearchString (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK
