---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496860"
---
# Get-AzureRmServiceBusNamespaceAuthorizationRule

## Áttekintés
Egy adott névtérhez tartozó meghatározott engedélyezési szabály leírását kapja meg. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmServiceBusNamespaceAuthorizationRule** parancsmag az adott névtérben a megadott engedélyezési szabály leírását kapja.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

Adott névtérhez megadott engedélyezési szabály leírását adja meg.

## PARAMÉTEREK

### -ResourceGroup
Az erőforráscsoport neve.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
ServiceBus-névtér AuthorizationRule neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
ServiceBus-névtér neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### -ResourceGroup
 System. String
 

### -NamespaceName
 System. String
 

### -AuthorizationRuleName
 System. String

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]
ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 típusa: Microsoft. ServiceBus/AuthorizationRules név: AuthoRule1 hely: Címkék: Rights: {figyelj, küldés}

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

