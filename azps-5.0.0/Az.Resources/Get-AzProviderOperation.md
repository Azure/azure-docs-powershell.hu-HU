---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301136"
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

### Példa 1: a minden szolgáltató minden műveletének beolvasása
```powershell
PS C:\> Get-AzProviderOperation *
```

### 2. példa: műveletek beszerzése egy adott erőforrás-szolgáltatónál
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### 3. példa: a virtuális gépeken végezhető műveletek beolvasása
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK
