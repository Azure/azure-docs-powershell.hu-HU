---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372482"
---
# Start-AzPolicyComplianceScan

## SYNOPSIS
Házirend-megfelelőség felmérését indítja el egy előfizetés vagy erőforráscsoport összes erőforrására.

## SZINTAXIS

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Start-AzPolicyComplianceScan** parancsmag elindítja egy előfizetés vagy erőforráscsoport házirendmegmegelőségi kiértékelését. Az adott hatókörbe tartozó összes erőforrás megfelelőségi állapotát az összes hozzárendelt házirendhez kiértékeli a rendszer.

## PÉLDÁK

### 1. példa: Megfelelőségi vizsgálat kezdése az előfizetés hatókörében
```
PS C:\> Start-AzPolicyComplianceScan
```

Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségértékelését.

### 2. példa: Megfelelőségi vizsgálat kezdése az erőforráscsoport hatókörében
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

Ez a parancs elindítja az aktív előfizetés "myRG" erőforráscsoportja házirend-megfelelőségi kiértékelést.

### 3. példa: Megfelelőségi vizsgálat kezdése és várakozás a háttérben való befejeződésére
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségértékelését. A vizsgálat befejeződik.

## PARAMETERS

### -AsJob
Futtassa a parancsmagot a háttérben.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Igaz érték visszaadva, ha a parancs sikeresen befejeződött.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
