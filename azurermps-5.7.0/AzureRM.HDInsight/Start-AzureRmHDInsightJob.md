---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504571"
---
# Start-AzureRmHDInsightJob

## Áttekintés
Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Start-AzureRMHDInsightJob** parancsmag egy meghatározott Azure HDInsight-feladatot indít egy adott fürtön.
Ez lehet egy MapReduce-feladat, egy adatfolyam-MapReduce feladat, egy kaptár vagy egy sertés-feladat.

## Példák

### Példa 1: feladat indítása a megadott fürtön
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

Ez a parancs elindítja a feladatot a Hadoop-001 nevű fürtben.

## PARAMÉTEREK

### -Fürtnév
A fürt nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -HttpCredential
A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobDefinition
Itt adhatja meg az Azure HDInsight-fürtben való indulási feladatot.

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### AzureHDInsightJobDefinition
A ' JobDefinition ' paraméter az "AzureHDInsightJobDefinition" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmHDInsightJob](./Get-AzureRmHDInsightJob.md)

[Új – AzureRmHDInsightHiveJobDefinition](./New-AzureRmHDInsightHiveJobDefinition.md)

[Stop-AzureRmHDInsightJob](./Stop-AzureRmHDInsightJob.md)

[Várjon-AzureRmHDInsightJob](./Wait-AzureRmHDInsightJob.md)


