---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: ad4867bc97f35a6e027d0f944d936da1760d1033
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009126"
---
# Get-AzHDInsightMonitoring

## SYNOPSIS
A fürtön telepített telepítés figyelési állapotát kapja meg.

## SZINTAXIS

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzHDInsightMonitoring** parancsmag egy Azure HDInsight-fürt telepítésének figyelési állapotát kapja meg. Ha a figyelés engedélyezve van, akkor a naplóelemzés munkaterület-azonosítóját is visszaadja.

## PÉLDÁK

### 1. példa
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

A figyelés engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz. A naplókat folyamló figyelési munkaterület-azonosító: 1d364e89-bb71-4503-aa3d-a23535aea7bd

### 2. példa
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

A figyelés engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz. A naplókat folyamló figyelési munkaterület-azonosító: 1d364e89-bb71-4503-aa3d-a23535aea7bd

### 3. példa
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

A fürtben le van tiltva a figyelés, mert a ClusterMonitoringEnabled tulajdonság hamis.

### 4. példa
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

A fürtben le van tiltva a figyelés, mert a ClusterMonitoringEnabled tulajdonság hamis.

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

### -Name
Annak a fürtnek a neve, amely a figyelés állapotát jelzi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A fürt erőforráscsoportja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
