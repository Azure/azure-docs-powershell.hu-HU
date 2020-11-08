---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183603"
---
# Get-AzEventGridDomainTopic

## Áttekintés
Beolvassa az esemény rácsa, illetve az aktuális Azure-előfizetés adott esemény rácsos tartománya alatti összes esemény rácsos témakörének részletes listáját.

## SZINTAXISA

### DomainTopicNameParameterSet (alapértelmezett)
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdDomainTopicParameterSet
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Get-AzEventGridDomainTopic parancsmag az aktuális Azure-előfizetésben egy adott tartományba tartozó adott esemény rácsa vagy az esemény rácsvonalai területének adatait kapja meg.
Ha a domain-téma neve meg van határozva, az egyetlen esemény rácsvonalai tartománya témakör részleteit adja vissza a függvény.
Ha a domain topic neve nincs megadva, a megadott tartománynév alatti tartományi témakörök listáját adja eredményül. A listában visszaadott elemek számát a legfelső paraméter határozza meg. Ha a felső érték nincs megadva vagy $null, a lista a tartomány összes témakörének elemét fogja tartalmazni. Egyéb esetben a felső ikon jelzi a listában a visszaadott elemek maximális számát.
Ha további tartományi témakörök is elérhetők, a következő hívásban a NextLink értékét kell használni a tartomány témaköreinek következő lapjának beszerzéséhez.
Végül a ODataQuery paraméter a keresési eredmények szűrésének végrehajtásához használható. A szűrési lekérdezés csak a név tulajdonságot használó OData szintaxist követi. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.

## Példák

### Példa 1

Az Event Grid domain témakörének részleteit az \` DomainTopic1 \` \` -tartomány Domain1 \` az erőforráscsoport MyResourceGroupName csoportban találhatja meg \` \` .

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### 2. példa

Az Event Grid domain topic \` DomainTopic1 az \` esemény rácsa \` Domain1 az \` erőforráscsoport \` MyResourceGroupName \` az ResourceId beállítás segítségével.

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### 3. példa

Az esemény rácsa tartomány Domain1 az esemény rácsa csoportban \` \` az \` MyResourceGroupName \` nélkül (az összes eredmény egyetlen lövésben ad eredményül).

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### 4. példa

Az esemény rácsa tartomány \` Domain1 az \` MyResourceGroupName nélküli erőforráscsoport-Kategóriák listájában, \` \` oldalszámozás nélkül (minden eredmény egyetlen lövésben ad eredményül) a ResourceId beállítás használatával

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Példa 5

Felsorolhatja az esemény rácsa tartományi témaköröket (ha vannak ilyenek) az \` erőforráscsoport MyResourceGroupName a tartományi Domain1 csoportban \` \` \` , amely megfelel az $odataFilter Query 10 tartományi témaköreinek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) a domain-témakörök beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridDomainTopic és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Tartománynév
EventGrid-tartomány neve.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
EventGrid a tartomány témájának nevét.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
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
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az esemény rácsa vagy a rács tartománya témakört megadó erőforrás azonosítója.

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
A lista eredményének szűréséhez használt OData lekérdezés. A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### System. Int32

## KIMENETEK

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
