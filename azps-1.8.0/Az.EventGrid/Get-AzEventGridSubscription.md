---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670880"
---
# Get-AzEventGridSubscription

## Áttekintés
Beolvassa az esemény előfizetésének részleteit, vagy megkapja az aktuális Azure-előfizetésben az összes esemény-előfizetés listáját.

## SZINTAXISA

### EventSubscriptionTopicNameParameterSet (alapértelmezett)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A Get-AzEventGridSubscription parancsmag a megadott esemény rácsra szóló előfizetésének részleteire, illetve az aktuális Azure-előfizetésben vagy az erőforráscsoport-előfizetések listájára kerül.
Ha az esemény-előfizetés neve meg van határozva, az egyetlen eseményből álló rácsra szóló előfizetés adatait adja vissza a rendszer.
Ha az esemény-előfizetés neve nincs megadva, a program az esemény-előfizetések listáját adja vissza.

## Példák

### Példa 1
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

A \` EventSubscription1 \` \` téma1 \` az erőforráscsoport MyResourceGroupName című témakörben létrehozott esemény- \` előfizetési adatok részleteit kapja meg \` .

### 2. példa
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

A \` \` téma1 az erőforráscsoport MyResourceGroupName, a teljes végpont URL-EventSubscription1 létrehozott esemény-előfizetési adatok részleteit kapja \` \` \` \` meg, ha ez egy webhorogon alapuló esemény előfizetése.

### 3. példa
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Ebben a témakörben megtalálhatja az \` erőforráscsoport-MyResourceGroupName létrehozott téma1-előfizetések listáját \` \` \` .

### 4. példa
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

A EventSubscription1 MyResourceGroupName létrehozott esemény-előfizetési adatok részleteit kapja \` \` meg \` \` .

### Példa 5
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Az \` \` aktuálisan kijelölt Azure-előfizetéshez létrehozott EventSubscription1-előfizetés részleteit kapja meg.

### 6. példa
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Megkapja az erőforráscsoport MyResourceGroupName létrehozott összes globális esemény-előfizetés listáját \` \` .

### 7. példa
```
PS C:\> Get-AzEventGridSubscription
```

Az aktuálisan kijelölt Azure-előfizetésből létrehozott összes globális esemény-előfizetés listáját kapja meg.

### 8. példa
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

A megadott hely westus2 az erőforráscsoport MyResourceGroupName létrehozott összes regionális esemény-előfizetésből álló listát kapja \` \` meg \` \` .

### Példa 9
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

A megadott EventHub-névtérhez létrehozott összes esemény-előfizetés listáját kapja meg.

### 10. példa
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

A megadott helyen lévő adott témakörhöz (EventHub-névterekhez) létrehozott összes esemény-előfizetés listáját adja meg.

### Példa 11
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Az adott erőforráscsoport számára létrehozott összes esemény-előfizetés listáját kapja.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -EventSubscriptionName
Az esemény-előfizetés neve

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Adja meg az esemény-előfizetés célhelyének teljes URL-címét.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid-téma objektuma

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Hely
Helyre

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetéseket létrehozták.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
EventGrid a téma neve

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType neve

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. EventGrid. models. PSTopic

## KIMENETEK

### Microsoft. Azure. Command. EventGrid. models. PSEventSubscription

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
