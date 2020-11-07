---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 741a888287ba7fcb4a9b54c1281a6a27be5fbb0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679740"
---
# Get-AzureRmEventGridTopicKey

## Áttekintés
Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### TopicNameParameterSet (alapértelmezett)
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicInputObjectParameterSet
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .

### 2. példa
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -InputObject
EventGrid-téma objektuma

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
EventGrid a téma neve

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az esemény rács témakörét megadó erőforrás-azonosító.

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

