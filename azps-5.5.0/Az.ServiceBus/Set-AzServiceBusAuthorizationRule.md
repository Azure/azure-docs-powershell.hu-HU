---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165083"
---
# Set-AzServiceBusAuthorizationRule

## SYNOPSIS
Frissíti a szolgáltatási-busz névterének vagy várólistájának vagy témájának engedélyezési szabályának megadott leírását.

## SZINTAXIS

### NamespaceAuthorizationRuleSet (alapértelmezett)
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### QueueAuthorizationRuleSet
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### TopicAuthorizationRuleSet
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AuthoRuleInputObjectSet
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzServiceBusAuthorizationRule** parancsmag frissíti a megadott engedélyezési szabály leírását a szolgáltatásbusz névterében vagy várólistáján vagy témakörében.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

Eltávolítja a **Manage** billentyűt a névtér engedélyezési szabályának `AuthoRule1` hozzáférési `SB-Example1` jogaiból.

### 2. példa
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

Eltávolítja a **Kezelés** elérést a várólistán lévő engedélyezési `AuthoRule1` szabály hozzáférési jogosultságaiból. `SBQueue`

### 3. példa
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

Eltávolítja a **Kezelés** elérést a témakörben található engedélyezési `AuthoRule1` szabály hozzáférési jogosultságaiból. `SBTopic`

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

### -InputObject
ServiceBus AuthorizationRule objektum

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
AuthorizationRule Name

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Namespace Name

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Queue
Várólistán lévő név

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve

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

### -Rights
Jogok, például @("Hallgatás","Küldés","Kezelés")

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Topic
Témakör neve

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes

### System.String[]

## KIMENETEK

### Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
