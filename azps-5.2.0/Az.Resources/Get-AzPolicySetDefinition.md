---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356550"
---
# Get-AzPolicySetDefinition

## SYNOPSIS
Házirend-definíciókat kap.

## SZINTAXIS

### NameParameterSet (alapértelmezett)
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupNameParameterSet
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionIdParameterSet
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdParameterSet
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### BuiltinFilterParameterSet
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CustomFilterParameterSet
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzPolicySetDefinition parancsmag** a házirend-definíciók gyűjteményét vagy egy név vagy azonosító által meghatározott házirendkészlet-definíciót kap.

## PÉLDÁK

### 1. példa: Az összes házirendkészlet-definíció lekérte
```
PS C:\> Get-AzPolicySetDefinition
```

Ez a parancs az összes házirendkészlet-definíciót beveszi.

### 2. példa: Házirendkészlet-definíció lekérte az aktuális előfizetésből név szerint
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

Ez a parancs a VMPolicySetDefinition nevű házirendkészlet-definíciót az aktuális alapértelmezett előfizetésből kapja meg.

### 3. példa: Házirendkészlet-definíció lekérte az előfizetésből név szerint
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

Ez a parancs a VMPolicySetDefinition nevű házirend-definíciót a 3bf44b72-c631-427a-b8c8-53e2595398ca azonosítójú előfizetésből kapja meg.

### 4. példa: Az összes egyéni házirendkészlet-definíció lekérte a felügyeleti csoporttól
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

Ez a parancs a Dept42 nevű felügyeleti csoport összes egyéni házirendkészlet-definícióját beveszi.

### 5. példa: Házirendkészlet-definíciók lekérte egy adott kategóriából
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

Ez a parancs az összes házirendkészlet-definíciót a "Virtuális gép" kategóriában kapja meg.

## PARAMETERS

### -ApiVersion
Ha be van állítva, az erőforrás-szolgáltató API-t használja.
Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.

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

### -Builtin
Az eredmények listáját csak a beépített házirendkészlet-definíciókra korlátozza.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Custom
Az eredmények listáját csak egyéni házirendkészlet-definíciókra korlátozza.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Id
A házirendkészlet teljes definícióazonosítója, az előfizetéssel együtt.
pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementGroupName
A lekért házirendkészlet-definíció(k) felügyeleti csoportjának neve.

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
A házirendkészlet definíciójának neve.

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.

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

### -SubscriptionId
A lekért házirendkészlet-definíció(k) előfizetés-azonosítója.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
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

### System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### System.Management.Automation.PSObject

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
