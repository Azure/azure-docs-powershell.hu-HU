---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207342"
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
