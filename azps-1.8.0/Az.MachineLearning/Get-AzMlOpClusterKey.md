---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835310"
---
# Get-AzMlOpClusterKey

## Áttekintés
Beolvassa a operationalization-fürtökhöz társított hozzáférési kulcsokat.

## SZINTAXISA

### GetByNameAndResourceGroup
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A operationalization-fürthöz társított tárolási fiók, tároló-nyilvántartó és más szolgáltatások kulcsai nem jelennek meg a fürt tulajdonságainak beszerzése során. A billentyűk lekérésének konkrét hívását el kell végeznie, mert bizalmas adatok.

## Példák

### Példa 1
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

A operationalization-fürthöz társított szolgáltatások titkos kulcsait számítja ki.

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

### -InputObject
A operationalization cluster objektum

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
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
Parameter Sets: GetByNameAndResourceGroup
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
Parameter Sets: GetByNameAndResourceGroup
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
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster

### System. String

## KIMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationClusterCredentials

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
