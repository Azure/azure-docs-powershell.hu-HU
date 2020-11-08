---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184537"
---
# Get-AzEventHubAuthorizationRule

## Áttekintés
Egy engedélyezési szabály részleteit kapja meg, vagy megkapja az engedélyezési szabályok listáját.

## SZINTAXISA

### NamespaceAuthorizationRuleSet (alapértelmezett)
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventhubAuthorizationRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasAuthoRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Get-AzEventHubAuthorizationRule parancsmag egy engedélyezési szabály részleteit vagy egy adott esemény központhoz tartozó összes engedélyezési szabály listáját kapja.
Ha egy engedélyezési szabály neve meg van határozva, az adott egyetlen engedélyezési szabály részleteit adja vissza a függvény.
Ha egy engedélyezési szabály neve nem jelenik meg, akkor a megadott esemény központjának minden engedélyezési szabályát a program visszaadja.
Ha (katasztrófa-helyreállítási) alias név, a rendszer az aliashoz konfigurált névtér engedélyezési szabályának részleteit adja vissza.

## Példák

### 1. példa: AuthorizationRule a névtérhez
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

Az engedélyezési szabály \` MyAuthRuleName a \` névtér \` MyNamespaceName \` .

### 2. példa: AuthorizationRules a névtérhez
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

A névtér MyNamespaceName az összes engedélyezési szabály listáját kapja \` \` .

### 3. példa: AuthorizationRule for EventHub
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

Az \` MyAuthRuleName az \` esemény központi \` MyEventHubName kapja \` , amelyet a névtér \` MyNamespaceName \` .

### 4. példa: AuthorizationRules for EventHub
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

A lista engedélyezési szabályait kapja meg az esemény központi \` MyEventHubName \` , amelyet a névtér \` MyNamespaceName \` .

### 5. példa: AuthorizationRule aliashoz (GeoRecovery-konfiguráció)
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

Az engedélyezési szabály \` MyAuthRuleName a \` névtér \` MyNamespaceName \` .

### 6. példa: AuthorizationRules aliashoz (GeoRecovery-konfiguráció)
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

Beolvassa az összes engedélyezési szabály \` MyAuthRuleName listáját \` a névtér \` MyNamespaceName \` .

## PARAMÉTEREK

### -AliasName
Alias neve

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Eventhub
Eventhub neve

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
AuthorizationRule neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Névtér neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
