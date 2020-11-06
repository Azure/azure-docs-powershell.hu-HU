---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501776"
---
# Get-AzureRmMlOpClusterKey

## Áttekintés
Beolvassa a operationalization-fürtökhöz társított hozzáférési kulcsokat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### A operationalization-fürt kulcsai a parancsmag bemeneti paramétereinek beszerzése.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### Beolvashatja a operationalization-fürt kulcsait egy OperationalizationCluster-példányból.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Azure-erőforrás-azonosítóból szerezheti be a operationalization-fürt kulcsait.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## Leírás
A operationalization-fürthöz társított tárolási fiók, tároló-nyilvántartó és más szolgáltatások kulcsai nem jelennek meg a fürt tulajdonságainak beszerzése során. A billentyűk lekérésének konkrét hívását el kell végeznie, mert bizalmas adatok.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

A operationalization-fürthöz társított szolgáltatások titkos kulcsait számítja ki.

## PARAMÉTEREK

### -InputObject
A operationalization cluster objektum

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
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
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## BEMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster
System. String


## KIMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationClusterCredentials


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

