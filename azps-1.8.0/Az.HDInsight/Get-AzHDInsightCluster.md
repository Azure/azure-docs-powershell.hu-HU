---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 8b15a93ee576af683cb2ebfffa621937a2ebba78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836058"
---
# Get-AzHDInsightCluster

## Áttekintés
A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.

## SZINTAXISA

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzHDInsightCluster** parancsmag az Azure HDInsight-szolgáltatási fürtök listáját tartalmazza az aktuális előfizetéshez.
Az *fürtnév* paraméterrel részletes információkat kaphat egy adott fürtről.

## Példák

### Példa 1: az Azure HDInsight-fürtök listázása
```
PS C:\>Get-AzHDInsightCluster
```

Ez a parancs felsorolja az összes Azure HDInsight-fürtöt.

## PARAMÉTEREK

### -Fürtnév
A fürt nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ResourceGroupName
Az erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzHDInsightCluster](./Remove-AzHDInsightCluster.md)

[Use-AzHDInsightCluster](./Use-AzHDInsightCluster.md)


