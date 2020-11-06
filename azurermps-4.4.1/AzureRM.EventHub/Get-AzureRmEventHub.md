---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505040"
---
# Get-AzureRmEventHub

## Áttekintés
Beolvassa az egyetlen esemény központjának részleteit, vagy megkapja az esemény-hubok listáját.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## Leírás
A Get-AzureRmEventHub parancsmag az esemény központjának részleteit vagy az aktuális névtérben lévő összes esemény hubok listáját jeleníti meg.
Ha az esemény-hub neve meg van határozva, akkor az adott esemény egyetlen csomópontjának adatait adja vissza a rendszer.
Ha egy esemény-hub neve nincs megadva, a megadott névtérben lévő összes esemény-hubok listáját adja vissza.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Az esemény központi MyEventHubName részleteit számítja ki \` \` .

### 2. példa
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

A névtér MyNamespaceName az esemény-hubok listáját számítja ki \` \` .

## PARAMÉTEREK

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

### -Name (név)
EventHub neve

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## BEMENETEK

### System. String

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. EventHubAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

