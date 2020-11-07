---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679718"
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
A parancs a művelet keresési karakterláncát adja meg, amely a megjelenített műveletek részleteit határozza meg.

A Get-AzureRmProviderOperation * segítségével minden Azure Resource Provider művelethez hozzáférhet.

Használja Get-AzureRmProviderOperation Microsoft. számítási/* lehetőséget a Microsoft összes műveletének beszerzéséhez. az erőforrás-szolgáltató kiszámítása.

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
Type: IAzureContextContainer
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
Type: String
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

### Karakterlánc
A ' OperationSearchString ' paraméter a "string" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK
