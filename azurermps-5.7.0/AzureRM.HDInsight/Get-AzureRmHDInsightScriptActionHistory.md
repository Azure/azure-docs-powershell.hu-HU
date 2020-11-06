---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: b2e302f9490cb5671728a46105ad574b54270c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492278"
---
# Get-AzureRmHDInsightScriptActionHistory

## Áttekintés
Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmHDInsightScriptActionHistory parancsmag beolvassa** az Azure HDInsight-fürtök parancsfájl-műveletek előzményeit, és a fordított időrendi sorrendben felsorolja azt, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.

## Példák

### Példa 1: egy fürt parancsfájl-végrehajtási műveleteinek előzményeit kapja meg.
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

Ez a parancs a Hadoop-001-alapú fürthöz tartozó parancsfájl-műveletek előzményeit kapja meg.

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

### -ScriptExecutionId
A futtatott parancsfájl műveleti AZONOSÍTÓját adja meg.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionDetail]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

