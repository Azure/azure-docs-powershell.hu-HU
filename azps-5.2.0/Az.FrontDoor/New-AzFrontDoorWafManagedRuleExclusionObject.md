---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369150"
---
# New-AzFrontDoorWafManagedRuleExclusionObject

## SYNOPSIS
Felügyelt szabálykizárási objektum létrehozása a waf felügyelt szabálykészletek, -csoportok és -szabályok számára.

## SZINTAXIS

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Felügyelt szabálykizárási objektum létrehozása a waf felügyelt szabálykészletek, -csoportok és -szabályok számára.

## PÉLDÁK

### 1. példa
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

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

### -Operátor
Operátor, amely a választó egyeztetésekor használható, az EqualsAny azt jelenti, hogy nincs kiválasztó (a megadott típusú összes egyező változó)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Választó
Selector pattern to match using the operator (if the operator is not EqualsAny)

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

### -Variable
Változó egyeztetése Lehetséges értékek: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestNamePostArgNames.
A QueryStringArgNames például kivételt ad a választónak a megadott operátorral egyező GET paraméterekből.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
