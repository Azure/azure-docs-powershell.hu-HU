---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680566"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## Áttekintés
Beolvassa a Eventubs-névtér engedélyezési szabályának részleteit, vagy megkapja az engedélyezési szabályok listáját.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## Leírás
A Get-AzureRmEventHubNamespaceAuthorizationRule parancsmag a megadott esemény-hubok névtér-engedélyezési szabályának adatait vagy a névtér-engedélyezési szabályok listáját kapja.
Ha az engedélyezési szabály neve meg van határozva, az egyetlen engedélyezési szabály részleteit adja eredményül.
Ha egy engedélyezési szabály neve nincs megadva, a rendszer a névtérben lévő összes engedélyezési szabály listáját adja vissza.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Az \` MyAuthRuleName az \` esemény-hubok névtér- \` MyNamespaceName \` , az erőforráscsoport \` MyResourceGroupName tartalmazó \` engedélyezési szabály értékét számítja ki.

### 2. példa
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

Az esemény hubok névtér-MyNamespaceName az RootManageSharedAccessKey alapértelmezett engedélyezési szabályát számítja \` \` ki \` \` az erőforráscsoport \` MyResourceGroupName \` .

### 3. példa
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Az esemény-hubok névtér-MyNamespaceName minden engedélyezési szabályát visszaállítja \` \` az erőforráscsoport \` MyResourceGroupName \` .

## PARAMÉTEREK

### -AuthorizationRuleName
Az esemény-hubok névtér-engedélyezési szabályának neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

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

## BEMENETEK

### System. String

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

