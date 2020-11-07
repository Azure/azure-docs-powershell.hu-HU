---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2bae39bb6a3e0c08a86118ce9ed8f9c6fadf82c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666533"
---
# Get-AzEventGridTopic

## Áttekintés
Az aktuális Azure-előfizetésből kinyeri az esemény rácsvonalait ismertető témakör részleteit

## SZINTAXISA

### ResourceGroupNameParameterSet (alapértelmezett)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Get-AzEventGridTopic parancsmag az aktuális Azure-előfizetésből származó adott esemény rácsvonalait ismerteti, vagy az aktuális Azure-előfizetésben lévő összes esemény rácsos témakörének listáját.
Ha a téma neve meg van határozva, az egyetlen esemény rácsa témakör részleteit adja vissza a program.
Ha a téma neve nincs megadva, a program a témakörök listáját adja vissza. A listában visszaadott elemek számát a legfelső paraméter határozza meg. Ha a felső érték nincs megadva vagy $null, a lista a témák összes elemét fogja tartalmazni. Egyéb esetben a felső ikon jelzi a listában a visszaadott elemek maximális számát.
Ha továbbra is elérhetők további témakörök, a következő hívásban a NextLink értékét kell használni a témakörök következő oldalának beszerzéséhez.
Végül a ODataQuery paraméter a keresési eredmények szűrésének végrehajtásához használható. A szűrési lekérdezés csak a név tulajdonságot használó OData szintaxist követi. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .

### 2. példa
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .

### 3. példa
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Az erőforráscsoport MyResourceGroupName nélkül listázhatja az összes esemény rácsát \` \` .

### 4. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Itt felsorolhatja az erőforráscsoport MyResourceGroupName az első 10 esemény rácshoz kapcsolódó témaköröket (ha vannak ilyenek), \` \` amelyek megfelelnek a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. A következő oldal (ok) beszerzése érdekében a felhasználó várhatóan újrahívja az Get-AzEventGridTopict, és az eredményt használja. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

### Példa 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Az előfizetésben szereplő összes esemény rácsos témakörének listázása oldalszámozás nélkül.

### 6. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Itt felsorolhatja az előfizetésben az első 10 esemény rácshoz kapcsolódó témaköröket (ha vannak ilyenek), amelyek megfelelnek a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. A következő oldal (ok) beszerzése érdekében a felhasználó várhatóan újrahívja az Get-AzEventGridTopict, és az eredményt használja. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

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

### -Name (név)
EventGrid a téma neve

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
A beszerzett források következő lapjának hivatkozása. Ezt az értéket az első Get-AzEventGrid parancsmag-hívással kapjuk meg, ha további források is elérhetők a lekérdezéshez.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
A lista eredményének szűréséhez használt OData lekérdezés. A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
A beszerezni kívánt források maximális száma. Az érvényes érték 1 és 100 között van. Ha a felső érték van megadva, és további találatok is elérhetők, az eredmény a következő oldalra mutató hivatkozást fogja tartalmazni a NextLink. Ha a felső érték nincs megadva, az erőforrások teljes listája azonnal visszakerül.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

## KIMENETEK

### Microsoft. Azure. Command. EventGrid. models. PSTopic

### Microsoft. Azure. Command. EventGrid. models. PSTopicListInstance

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
