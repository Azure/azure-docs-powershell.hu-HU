---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347382"
---
# Get-AzPolicyMetadata

## SYNOPSIS
Házirend metaadat-erőforrásainak lekérte

## SZINTAXIS

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzPolicyRemediation** parancsmag begyűjte az összes házirend metaadat-erőforrását vagy egy adott házirend metaadat-erőforrását.

## PÉLDÁK

### 1. példa: Az összes házirend metaadat-erőforrásának lekérte
```powershell
PS C:\> Get-AzPolicyMetadata
```

Ez a parancs az összes házirend metaadat-erőforrását beveszi

### 2. példa: 10 házirend metaadat-erőforrásának gyűjteménye
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Ez a parancs 10 házirend metaadat-erőforrásból álló gyűjteményt kap

### 3. példa: Egyetlen házirend metaadat-erőforrásának lekértése "ACF1348" néven
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Ez a parancs egyetlen házirend metaadat-erőforrást kap "ACF1348" néven

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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
Erőforrás neve.

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

### -Top
A vissza nem térhet házirend metaadat-erőforrásainak maximális száma.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
