---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666366"
---
# Get-AzHDInsightOperationsManagementSuite

## Áttekintés
A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.

## SZINTAXISA

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzHDInsightOperationsManagementSuite** PARANCSMAG az OMS telepítésének állapotát egy Azure HDInsight-fürtben kapja meg. Ha a OMS engedélyezve van, akkor a OMS munkaterület azonosítóját is visszaadja a program.

## Példák

### Példa 1
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz. A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd

### 2. példa
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz. A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd

### 3. példa
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.

### 4. példa
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.

## PARAMÉTEREK

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

### -Name (név)
Annak a fürtnek a neve, amely a Operations Management Suite (OMS) állapotát kapja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
A fürt erőforrás csoportja.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightOMS

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
