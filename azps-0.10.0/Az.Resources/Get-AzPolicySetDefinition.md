---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 100eb4f58a9fe946c17485b34b9cb8ffaacab6c5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843437"
---
# Get-AzPolicySetDefinition

## Áttekintés
Kapja meg a házirend-definíciókat.

## SZINTAXISA

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
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
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

## Leírás
A **Get-AzPolicySetDefinition** parancsmag a házirend-definíciók, illetve egy név vagy azonosító szerint azonosított speciális házirend-definíció gyűjteményét kapja meg.

## Példák

### Példa 1: az összes házirend-készlet definíciójának beolvasása
```
PS C:\> Get-AzPolicySetDefinition
```

Ez a parancs beilleszti az összes házirend-definíciót.

### 2. példa: a házirend-készlet definíciójának beszerzése a jelenlegi előfizetésből név szerint
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

Ez a parancs az aktuális alapértelmezett előfizetésből a VMPolicySetDefinition nevű házirend-definíciót kapja meg.

### 3. példa: házirend-definíció beszerzése az előfizetésből név szerint
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

Ez a parancs a VMPolicySetDefinition nevű házirend-definíciót kapja meg az 3bf44b72-c631-427a-b8c8-53e2595398ca AZONOSÍTÓJÚ előfizetésből.

### Példa 4: az összes egyéni házirend-készlet definíciójának beolvasása a kezelés csoportból
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

Ez a parancs beilleszti az összes egyéni házirend-definíciót a Dept42 nevű felügyeleti csoportból.

## PARAMÉTEREK

### -ApiVersion
Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.
Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.

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

### -Beépített
Az eredmények listáját csak a beépített házirend-definíciók listájában korlátozhatja.

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
Az eredmények listáját csak az egyéni házirend-készlet definíciói szerint korlátozhatja.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.
például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}

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
A beolvasott házirend-definíció (ok) felügyeleti csoportjának a neve.

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

### -Name (név)
A Policy set definition név.

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
Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.

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
A házirend-készlet definíciójának (ek) előfizetési azonosítója a beszerzéshez.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

## KIMENETEK

### System. Management. Automation. PSObject

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
