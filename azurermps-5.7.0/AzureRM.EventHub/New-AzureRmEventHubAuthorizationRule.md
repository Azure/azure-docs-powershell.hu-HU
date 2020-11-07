---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: ae7fe44bf0fd3eccb157cefd6f57dade203d4fb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679735"
---
# New-AzureRmEventHubAuthorizationRule

## Áttekintés
Új esemény-hubok engedélyezési szabályának létrehozása a névtérhez vagy a eventhub.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### NamespaceAuthorizationRuleSet (alapértelmezett)
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EventhubAuthorizationRuleSet
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Az New-AzureRmEventHubAuthorizationRule parancsmag új esemény-hubok engedélyezési szabályt hoz létre.

## Példák

### Példa 1
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat a névtér \` MyNamespaceName \` , az erőforráscsoport \` MyResourceGroupName \` .

### 2. példa
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat az esemény központi \` MyEventHubName a \` MyNamespaceName névtér- \` \` , az erőforráscsoport \` MyResourceGroupName \` .

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventHub
EventHub neve

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Névtér neve

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Jogok
Jogok (például "Figyelj", "Küldés", "kezelés")

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction
További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
System. string []


## KIMENETEK

### Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
