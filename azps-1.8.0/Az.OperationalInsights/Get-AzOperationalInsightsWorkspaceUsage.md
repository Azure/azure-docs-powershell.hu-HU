---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 04a62f4929e89dd4bff4d088d84325b0bdbb140b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671932"
---
# Get-AzOperationalInsightsWorkspaceUsage

## Áttekintés
A munkaterület használati adatainak beolvasása

## SZINTAXISA

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzOperationalInsightsWorkspaceUsage** parancsmag kikeresi a munkaterület használati adatait.
Ez a cikk bemutatja, hogy mennyi adatot elemeztek a munkaterület egy bizonyos időszakra.

## Példák

### Példa 1: használati érték beszerzése munkaterületi név szerint
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

Ez a parancs a megadott erőforráscsoport MyWorkspace nevű munkaterülete használati adatait kapja meg.

### 2. példa: használati adatainak beszerzése a csővezeték használatával
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

Ez a parancs a MyWorkSpace nevű munkaterületet az Get-AzOperationalInsightsWorkspace parancsmag segítségével kapja meg, majd átadja a munkaterületet az aktuális parancsmagnak.
A parancs kinyeri az adott munkaterület használati adatait.

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
A munkaterület nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. OperationalInsights. models. PSUsageMetric

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure hadműveleti parancsmagok](/powershell/module/az.operationalinsights)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


