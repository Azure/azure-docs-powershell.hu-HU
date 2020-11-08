---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182244"
---
# Get-AzEventGridSubscription

## Áttekintés
Beolvassa az esemény előfizetésének részleteit, vagy megkapja az aktuális Azure-előfizetésben az összes esemény-előfizetés listáját.

## SZINTAXISA

### EventSubscriptionTopicNameParameterSet (alapértelmezett)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A Get-AzEventGridSubscription parancsmag a megadott esemény rácsra szóló előfizetésének részleteire, illetve az aktuális Azure-előfizetésben vagy az erőforráscsoport-előfizetések listájára kerül.
Ha az esemény-előfizetés neve meg van határozva, az egyetlen eseményből álló rácsra szóló előfizetés adatait adja vissza a rendszer.
Ha az esemény-előfizetés neve nincs megadva, a program az esemény-előfizetések listáját adja vissza. A listában visszaadott elemek számát a legfelső paraméter határozza meg. Ha a felső érték nincs megadva vagy $null, a lista a minden esemény előfizetési elemét fogja tartalmazni. Egyéb esetben a felső ikon jelzi a listában a visszaadott elemek maximális számát.
Ha további esemény-előfizetések is elérhetők, a NextLink lévő értéket a következő hívásban kell használnia az esemény-előfizetések következő lapjának beszerzéséhez.
Végül a ODataQuery paraméter a keresési eredmények szűrésének végrehajtásához használható. A szűrési lekérdezés csak a név tulajdonságot használó OData szintaxist követi. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

A \` EventSubscription1 \` \` téma1 \` az erőforráscsoport MyResourceGroupName című témakörben létrehozott esemény- \` előfizetési adatok részleteit kapja meg \` .

### 2. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

A \` \` téma1 az erőforráscsoport MyResourceGroupName, a teljes végpont URL-EventSubscription1 létrehozott esemény-előfizetési adatok részleteit kapja \` \` \` \` meg, ha ez egy webhorogon alapuló esemény előfizetése.

### 3. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Az erőforráscsoportok MyResourceGroupName a témakör téma1 létrehozott összes esemény-előfizetést felsorolhatja \` \` \` \` oldalszámozás nélkül.

### 4. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Felsorolhatja az első 10 esemény előfizetését (ha vannak ilyenek), \` \` amelyeket az erőforráscsoport \` MyResourceGroupName a téma1, \` amely megfelel a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

### Példa 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

A EventSubscription1 MyResourceGroupName létrehozott esemény-előfizetési adatok részleteit kapja \` \` meg \` \` .

### 6. példa
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Az \` \` aktuálisan kijelölt Azure-előfizetéshez létrehozott EventSubscription1-előfizetés részleteit kapja meg.

### 7. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Beolvassa az erőforráscsoport \` MyResourceGroupName nélküli, oldalszámozás nélküli globális esemény-előfizetések listáját \` .

### 8. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Sorolja fel az első 5 esemény előfizetését (ha vannak) az erőforráscsoport \` MyResourceGroupName \` , amely megfelel a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

### Példa 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Beolvassa az aktuálisan kijelölt Azure-előfizetéssel létrehozott globális esemény-előfizetések listáját oldalszámozás nélkül.

### 10. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Felsorolhatja az aktuálisan kijelölt Azure-előfizetésben létrehozott első 15 globális esemény-előfizetést (ha van ilyen), amely megfelel a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

### Példa 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

A \` \` megadott helyen, \` oldalszámozás nélküli westus2-előfizetések listáját kapja meg az erőforráscsoport MyResourceGroupName \` .

### Példa 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Felsoroljuk az első 15 regionális esemény előfizetését (ha vannak ilyenek) az erőforráscsoport \` MyResourceGroupName \` , \` \` amely megfelel a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

### Példa 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

A megadott EventHub-alapú névtérhez létrehozott összes esemény-előfizetés listáját adja meg oldalszámozás nélkül.

### 14 példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

A megadott EventHub-névtérhez létrehozott első 25 esemény-előfizetések (ha vannak) listája, amely megfelel a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

### Példa 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

A megadott EventHub-előfizetések listáját adja meg a megadott helyen, oldalszámozás nélkül.

### 16 példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Felsorolhatja az első 15 esemény előfizetését (ha van ilyen) a megadott EventHub-névterekhez (a megadott helyen), amely megfelel a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

### 17 példa
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Megkeresi az adott erőforráscsoport számára létrehozott összes esemény-előfizetést, oldalszámozás nélkül.

### 18 példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Felsorolhatja az adott erőforráscsoport számára létrehozott első 100-előfizetéseket (ha vannak ilyenek), amelyek megfelelnek a $odataFilter lekérdezésnek. Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null. Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink A hívónak a találatok után leállnia kell. A NextLink $null válik.

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

### -DomainInputObject
EventGrid tartomány objektuma.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tartománynév
EventGrid-tartomány neve.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
EventGrid objektum

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
EventGrid a tartomány témájának nevét.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Az esemény-előfizetés neve

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Adja meg az esemény-előfizetés célhelyének teljes URL-címét.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
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

### -Top
A lista eredményének szűréséhez használt OData lekérdezés. A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
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
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### Microsoft. Azure. Command. EventGrid. models. PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

## KIMENETEK

### Microsoft. Azure. Command. EventGrid. models. PSEventSubscription

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
