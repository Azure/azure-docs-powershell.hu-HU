---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843429"
---
# Get-AzProviderOperation

## Áttekintés
Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.

## SZINTAXISA

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az Get-AzProviderOperation az Azure Resource Providers által kitett műveleteket kapja meg.
A műveletek létrehozhatók egyéni szerepkörök az Azure RBAC-ban.
A parancs beírja a kívánt műveleti keresési karakterláncot (esetleges helyettesítő *karakterrel ()), amely meghatározza a megjelenítendő műveletek részleteit. A Get-AzProviderOperation * segítségével minden Azure Resource Provider művelethez hozzáférhet. Használja Get-AzProviderOperation Microsoft. kiszámítás/* a Microsoft összes műveletének beszerzése lehetőséget.

## Példák

### Minden művelet beolvasása minden szolgáltatónál
```
PS C:\> Get-AzProviderOperation *
```

### Műveletek beszerzése egy adott erőforrás-szolgáltatónál
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### A virtuális gépeken végezhető műveletek beolvasása
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
Paraméterek: OperationSearchString (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation

## MEGJEGYZI
Kulcsszavak: Azure, az, kar, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK
