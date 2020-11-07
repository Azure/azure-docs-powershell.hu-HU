---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673107"
---
# Remove-AzureRmMlOpCluster

## Áttekintés
Eltávolít egy operationalization-fürtöt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Operationalization-fürt eltávolítása a parancsmag bemeneti paramétereivel
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### Operationalization-fürt eltávolítása OperationalizationCluster-példányból
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### Operationalization-fürt eltávolítása Azure Resouce-azonosítóból.
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## Leírás
Eltávolít egy operationalization-fürtöt. Előfordulhat, hogy a fürthöz társított egyes erőforrások nem törlődnek. Az Azure Container szolgáltatás például eltűnik, de a hozzájuk tartozó VMs nem. A tárolási fiók, a tároló-nyilvántartó és az alkalmazás-elemzések nem törlődnek diagnosztikai adatok esetében.

## Példák

### Példa 1
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### 2. példa
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## PARAMÉTEREK

### -InputObject
A operationalization cluster objektum

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
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
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
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
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
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
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
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

### System. Void


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

