---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
ms.openlocfilehash: de297c94be69773d07efedfae42ccc029fc13414
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835277"
---
# Remove-AzMlOpCluster

## Áttekintés
Eltávolít egy operationalization-fürtöt.

## SZINTAXISA

### RemoveByNameAndResourceGroup (alapértelmezett)
```
Remove-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByInputObject
```
Remove-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceId
```
Remove-AzMlOpCluster -ResourceId <String> [-IncludeAllResources] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Eltávolít egy operationalization-fürtöt. Előfordulhat, hogy a fürthöz társított egyes erőforrások nem törlődnek. Az Azure Container szolgáltatás például eltűnik, de a hozzájuk tartozó VMs nem. A tárolási fiók, a tároló-nyilvántartó és az alkalmazás-elemzések nem törlődnek diagnosztikai adatok esetében.

## Példák

### Példa 1
```
PS C:\> Remove-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### 2. példa
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzMlOpCluster
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -IncludeAllResources
Eltávolítja a fürttel létrehozott összes erőforrást.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A operationalization cluster objektum

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A operationalization-fürt neve.

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
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
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
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
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster

### System. String

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
