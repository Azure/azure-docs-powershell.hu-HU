---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503940"
---
# Set-AzureRmServiceBusQueueAuthorizationRule

## Áttekintés
Frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz várólistájában.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmServiceBusQueueAuthorizationRule** parancsmag frissíti a megadott Service Bus-várólista megadott engedélyezési szabályának leírását.

## Példák

### Példa 1
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

A várólista engedélyezési szabályának elérési jogát hozzáadja a **kezeléshez** `SBAuthoRule1` `SB-Queue_exampl1` .

## PARAMÉTEREK

### -AuthorizationRuleName
Az engedélyezési szabály neve. Kötelező, ha **-AuthruleObj** nincs megadva.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuthRuleObj
A szolgáltatás busz várólista-engedélyezési szabály objektuma.

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
A szolgáltatás Buszjának névtér neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -QueueName
A szolgáltatás Buszjának várólista neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Az erőforráscsoport neve.

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
A jogok; például @ ("Figyelj", "Küldés", "kezelés"). Kötelező, ha a "AuthruleObj" nincs megadva.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### -ResourceGroup
 System. String

### -NamespaceName
 System. String

### -QueueName
 System. String

### -AuthRuleObj
 Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes

## KIMENETEK

### Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

