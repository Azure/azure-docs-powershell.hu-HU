---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: d41c340b5c7276ddd6546bcf44e83f38dbc8b240
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846085"
---
# <span data-ttu-id="2364a-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="2364a-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="2364a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2364a-102">SYNOPSIS</span></span>
<span data-ttu-id="2364a-103">Az aktuális Azure-előfizetésből kinyeri az esemény rácsvonalait ismertető témakör részleteit</span><span class="sxs-lookup"><span data-stu-id="2364a-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="2364a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2364a-104">SYNTAX</span></span>

### <span data-ttu-id="2364a-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2364a-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2364a-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2364a-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2364a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2364a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2364a-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="2364a-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2364a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2364a-109">DESCRIPTION</span></span>
<span data-ttu-id="2364a-110">A Get-AzEventGridTopic parancsmag az aktuális Azure-előfizetésből származó adott esemény rácsvonalait ismerteti, vagy az aktuális Azure-előfizetésben lévő összes esemény rácsos témakörének listáját.</span><span class="sxs-lookup"><span data-stu-id="2364a-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="2364a-111">Ha a téma neve meg van határozva, az egyetlen esemény rácsa témakör részleteit adja vissza a program.</span><span class="sxs-lookup"><span data-stu-id="2364a-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="2364a-112">Ha a téma neve nincs megadva, a program a témakörök listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="2364a-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="2364a-113">A listában visszaadott elemek számát a legfelső paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2364a-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="2364a-114">Ha a felső érték nincs megadva vagy $null, a lista a témák összes elemét fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2364a-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="2364a-115">Egyéb esetben a felső ikon jelzi a listában a visszaadott elemek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="2364a-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="2364a-116">Ha továbbra is elérhetők további témakörök, a következő hívásban a NextLink értékét kell használni a témakörök következő oldalának beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="2364a-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="2364a-117">Végül a ODataQuery paraméter a keresési eredmények szűrésének végrehajtásához használható.</span><span class="sxs-lookup"><span data-stu-id="2364a-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="2364a-118">A szűrési lekérdezés csak a név tulajdonságot használó OData szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="2364a-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="2364a-119">A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="2364a-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="2364a-120">Példák</span><span class="sxs-lookup"><span data-stu-id="2364a-120">EXAMPLES</span></span>

### <span data-ttu-id="2364a-121">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2364a-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="2364a-122">Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="2364a-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2364a-123">2. példa</span><span class="sxs-lookup"><span data-stu-id="2364a-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="2364a-124">Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="2364a-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2364a-125">3. példa</span><span class="sxs-lookup"><span data-stu-id="2364a-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="2364a-126">Az erőforráscsoport MyResourceGroupName nélkül listázhatja az összes esemény rácsát \` \` .</span><span class="sxs-lookup"><span data-stu-id="2364a-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="2364a-127">4. példa</span><span class="sxs-lookup"><span data-stu-id="2364a-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="2364a-128">Itt felsorolhatja az erőforráscsoport MyResourceGroupName az első 10 esemény rácshoz kapcsolódó témaköröket (ha vannak ilyenek), \` \` amelyek megfelelnek a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="2364a-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="2364a-129">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="2364a-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="2364a-130">A következő oldal (ok) beszerzése érdekében a felhasználó várhatóan újrahívja az Get-AzEventGridTopict, és az eredményt használja. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="2364a-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="2364a-131">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="2364a-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="2364a-132">Példa 5</span><span class="sxs-lookup"><span data-stu-id="2364a-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="2364a-133">Az előfizetésben szereplő összes esemény rácsos témakörének listázása oldalszámozás nélkül.</span><span class="sxs-lookup"><span data-stu-id="2364a-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="2364a-134">6. példa</span><span class="sxs-lookup"><span data-stu-id="2364a-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="2364a-135">Itt felsorolhatja az előfizetésben az első 10 esemény rácshoz kapcsolódó témaköröket (ha vannak ilyenek), amelyek megfelelnek a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="2364a-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="2364a-136">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="2364a-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="2364a-137">A következő oldal (ok) beszerzése érdekében a felhasználó várhatóan újrahívja az Get-AzEventGridTopict, és az eredményt használja. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="2364a-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="2364a-138">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="2364a-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="2364a-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2364a-139">PARAMETERS</span></span>

### <span data-ttu-id="2364a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2364a-140">-DefaultProfile</span></span>
<span data-ttu-id="2364a-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2364a-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2364a-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2364a-142">-Name</span></span>
<span data-ttu-id="2364a-143">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="2364a-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="2364a-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="2364a-144">-NextLink</span></span>
<span data-ttu-id="2364a-145">A beszerzett források következő lapjának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="2364a-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="2364a-146">Ezt az értéket az első Get-AzEventGrid parancsmag-hívással kapjuk meg, ha további források is elérhetők a lekérdezéshez.</span><span class="sxs-lookup"><span data-stu-id="2364a-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="2364a-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="2364a-147">-ODataQuery</span></span>
<span data-ttu-id="2364a-148">A lista eredményének szűréséhez használt OData lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="2364a-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="2364a-149">A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="2364a-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="2364a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2364a-150">-ResourceGroupName</span></span>
<span data-ttu-id="2364a-151">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2364a-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="2364a-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2364a-152">-ResourceId</span></span>
<span data-ttu-id="2364a-153">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2364a-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="2364a-154">-Top</span><span class="sxs-lookup"><span data-stu-id="2364a-154">-Top</span></span>
<span data-ttu-id="2364a-155">A beszerezni kívánt források maximális száma.</span><span class="sxs-lookup"><span data-stu-id="2364a-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="2364a-156">Az érvényes érték 1 és 100 között van.</span><span class="sxs-lookup"><span data-stu-id="2364a-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="2364a-157">Ha a felső érték van megadva, és további találatok is elérhetők, az eredmény a következő oldalra mutató hivatkozást fogja tartalmazni a NextLink.</span><span class="sxs-lookup"><span data-stu-id="2364a-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="2364a-158">Ha a felső érték nincs megadva, az erőforrások teljes listája azonnal visszakerül.</span><span class="sxs-lookup"><span data-stu-id="2364a-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="2364a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2364a-159">CommonParameters</span></span>
<span data-ttu-id="2364a-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2364a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2364a-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2364a-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2364a-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2364a-162">INPUTS</span></span>

### <span data-ttu-id="2364a-163">System. String</span><span class="sxs-lookup"><span data-stu-id="2364a-163">System.String</span></span>

### <span data-ttu-id="2364a-164">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2364a-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2364a-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2364a-165">OUTPUTS</span></span>

### <span data-ttu-id="2364a-166">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2364a-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="2364a-167">Microsoft. Azure. Command. EventGrid. models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="2364a-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="2364a-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2364a-168">NOTES</span></span>

## <span data-ttu-id="2364a-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2364a-169">RELATED LINKS</span></span>
