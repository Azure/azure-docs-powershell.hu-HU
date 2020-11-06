---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502727"
---
# Get-AzureRmEventHubNamespace

## Áttekintés
Beolvassa az esemény-hubok névterének részleteit, vagy az aktuális Azure-előfizetésből az összes esemény-hubok névterének listáját kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## Leírás
A Get-AzureRmEventHubNamespace parancsmag az aktuális Azure-előfizetésben lévő adott esemény-hubok névterének részleteit vagy az összes esemény hubok névterét tartalmazza.
Ha a névtér neve meg van határozva, az egyetlen esemény-hubok névtér részleteit adja vissza a rendszer.
Ha a névtér neve nincs megadva, a program a névterek listáját adja vissza.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Az esemény-hubok névtér-MyNamespaceName részleteit kapja \` \` meg az erőforráscsoport \` MyResourceGroupName \` .

## PARAMÉTEREK

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
EventHub-névtér neve

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## BEMENETEK

### System. String

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. NamespaceAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

