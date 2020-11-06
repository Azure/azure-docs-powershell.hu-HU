---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: a09da5122403d971d8b5d1abde79c8a9a95c3ecd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504160"
---
# Remove-AzureRmHDInsightCluster

## Áttekintés
Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmHDInsightCluster** parancsmag az előfizetésből eltávolítja a megadott HDInsight-fürtszolgáltatást.
Ezzel a művelettel a Hadoop elosztott fájlrendszerében (HDFS) tárolt adatok is törlődnek.
A rendszer nem törli a kapcsolódó Azure-tárterületi fiókban tárolt adatait.
A külső metastores tárolt adatot nem törli a program.

## Példák

### Példa 1: Azure HDInsight-fürt törlése
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

Ez a parancs eltávolítja a-Hadoop-001 nevű fürtöt.

## PARAMÉTEREK

### -Fürtnév
A fürt nevét adja meg.

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

### -ResourceGroupName
Az erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Management. HDInsight. models. ClusterGetResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmHDInsightCluster](./Get-AzureRmHDInsightCluster.md)

[Use-AzureRmHDInsightCluster](./Use-AzureRmHDInsightCluster.md)


