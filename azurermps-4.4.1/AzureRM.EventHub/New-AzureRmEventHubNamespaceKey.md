---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505008"
---
# New-AzureRmEventHubNamespaceKey

## Áttekintés
Új elsődleges vagy másodlagos kulcs létrehozása az engedélyezési szabályhoz a megadott esemény-hubok névtérben.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## Leírás
Az New-AzureRmEventHubNamespaceKey parancsmag újra létrehozta a megadott engedélyezési szabály elsődleges vagy másodlagos kulcsát a megadott esemény-hubok névtérben.

## Példák

### Példa 1
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

Újragenerálja az elsődleges kulcsot az \` MyAuthRuleName az \` esemény-hubok névtér- \` MyNamespaceName, az \` erőforráscsoport- \` MyResourceGroupName \` .

## PARAMÉTEREK

### -AuthorizationRuleName
Engedélyezési szabály neve.

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

### -NamespaceName
Az esemény hubok névterének neve.

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

### -RegenerateKeys
Kulcs a regenerálódni: \` PrimaryKey \` vagy \` SecondaryKey \` .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
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

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. EventHub. models. ListKeysAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

