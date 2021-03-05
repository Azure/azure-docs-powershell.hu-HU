---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009093"
---
# Get-AzHDInsightProperty

## SYNOPSIS
Beszerzheti a HDInsight szolgáltatás tulajdonságait, például az elérhető helyeket és a kapacitást.

## SZINTAXIS

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzHDInsightProperty** parancsmag az Azure HDInsight-re jellemző tulajdonságokat kap, például az elérhető helyek listáját, a HDInsight-fürtverziókat és az elérhető számítási kapacitást.

## PÉLDÁK

### 1. példa: Azure HDInsight-fürt tulajdonságainak lekérte
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

Ez a parancs hdinsight-szolgáltatásból kap tulajdonságokat az US 2.2-től keletre.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Location
Azt a helyet adja meg, ahol lekéri a HDInsight-tulajdonságokat.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs
## KIMENETEK

### Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities
## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
