---
external help file: Microsoft.Azure.Commands.ResourceGraph.dll-Help.xml
Module Name: AzureRM.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resourcegraph/search-azurermgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
ms.openlocfilehash: 900722c15d1c7a6560ba1f498b9dd0d3981f899a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500143"
---
# Search-AzureRmGraph

## Áttekintés
Lekérdezi az Azure Resource Manager által kezelt erőforrásokat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Search-AzureRmGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
További információ a lekérdezési szintaxisról: https://aka.ms/resource-graph/learntoquery

## Példák

### Példa 1
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

Egyszerű erőforrások lekérdezése: az erőforrásmezők egy alcsoportját kéri.

### 2. példa
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

Komplex lekérdezés a mezők kijelöléséről, szűréséről és összegzéséről.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Query
Erőforrás-grafikon lekérdezése

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Előfizetés
Előfizetés (ek) a lekérdezés futtatásához.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip (kihagyás)
Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Első
A visszaadni kívánt objektumok maximális száma. Engedélyezett értékek: 1-5000.
Az alapértelmezett érték a 100.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction
További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### System. Management. Automation. PSObject

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
