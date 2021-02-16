---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: a2e0bc21546dad414ee8782acd0a1505ed1e5489
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399124"
---
# New-AzOperationalInsightsWorkspace

## SYNOPSIS
Munkaterületet hoz létre, vagy visszaállít egy helyreállíthatóan törölt munkaterületet.

## SZINTAXIS

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzOperationalInsightsWorkspace** parancsmag munkaterületet hoz létre a megadott erőforráscsoportban és helyen. Vagy visszaállíthatja a helyreállíthatóan törölt munkaterületet.

## PÉLDÁK

### 1. példa: Munkaterület létrehozása név szerint
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

Ez a parancs létrehoz egy MyWorkspace nevű szabványos termékváltozat-munkaterületet a ContosoResourceGroup nevű erőforráscsoportban.

### 2. példa: Munkaterület létrehozása és csatolása meglévő fiókhoz
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

Az első parancs a Get-AzOperationalInsightsLinkTargets parancsmag segítségével begyakorlja a Operational Insights-fiók hivatkozási céljait, majd tárolja őket a $OILinkTargets változóban.
A második parancs átadja az $OILinkTargets-ban az első fiókhivatkozási célhelyet a **New-AzOperationalInsightsWorkspace** parancsmagnak a folyamatoperációs operátor használatával.
A parancs létrehoz egy MyWorkspace nevű szabványos termékváltozat-munkaterületet, amely a webhely első Operational Insights-$OILinkTargets.

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

### -Force
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Azt a helyet adja meg, ahol létre kell hoznia a munkaterületet, például Kelet-Egyesült Államok vagy Nyugat-Európa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
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

### -PublicNetworkAccessForIngestion
A munkaterületen való hozzáféréshez szükséges hálózati hozzáférés típusa. Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNetworkAccessForQuery
A munkaterületi lekérdezés eléréséhez használható hálózati hozzáférés típusa. Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
A munkaterület ebben az erőforráscsoportban jön létre.

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

### -RetentionInDays
A munkaterület adatmegőrzési időszaka napokban. 730 nap az összes többi skus maximálisan engedélyezett

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Termékváltozat
A munkaterület szolgáltatási rétegét határozza meg. Ha többet meg kell tudni arról, hogy melyik értéket kell használni, https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers ellenőrizze.
Érvényes értékek:
- ingyenes
- pergb2018
- pernode
- prémium
- különálló
- normál

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
A munkaterület erőforráscímkéi.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Hashtable

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## MEGJEGYZÉSEK

Megjelent egy új árazási modell. Ha Ön felhőszolgáltató, ez azt jelenti, hogy a termékváltozathoz "önálló" eszközt kell használnia. A színfalak mögött a termékváltozat gbonként 2018-ra változik. További információért olvassa el az alábbi információkat: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure Operational Insights-parancsmagok](./Az.OperationalInsights.md)



