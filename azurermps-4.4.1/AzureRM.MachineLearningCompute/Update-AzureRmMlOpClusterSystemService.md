---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504888"
---
# Update-AzureRmMlOpClusterSystemService

## Áttekintés
Elindítja a operationalization-fürt rendszerszolgáltatásainak frissítését.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Rendszerszolgáltatások frissítésének indítása a parancsmag bemeneti paramétereinek segítségével
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### Indítsa el a rendszerszolgáltatások frissítését egy PSOperationalizationCluster példány-definícióból.
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### Indítsa el a rendszerszolgáltatások frissítését egy Azure Resouce-azonosítóból.
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## Leírás
A rendszerszolgáltatásokat a operationalization-fürttől függetlenül is frissítheti. A rendszerszolgáltatások frissítésének indításához használja ezt a parancsmagot. Ha nincs elérhető frissítés, a rendszer továbbra is elindít egy frissítést, és sikeresen visszaadja. Miután a frissítés befejeződött, a jelentések a kezdéskor, a befejezett és a sikeres volt.

## Példák

### Példa 1
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

Elindítja a rendszerszolgáltatások frissítését a megadott fürtön. 

## PARAMÉTEREK

### -InputObject
A operationalization cluster objektum

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A operationalization-fürt neve.

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A operationalization-fürt erőforráscsoport neve.

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Az Azure Resource id a operationalization-fürthöz.

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## BEMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster
### System. String


## KIMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSUpdateSystemServicesResponse


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

