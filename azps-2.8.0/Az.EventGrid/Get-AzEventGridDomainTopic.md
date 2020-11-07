---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: b12369fb0a4140bea1693fd9074a601cd73fa9cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666541"
---
# <span data-ttu-id="02080-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="02080-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="02080-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02080-102">SYNOPSIS</span></span>
<span data-ttu-id="02080-103">Beolvassa az esemény rácsa, illetve az aktuális Azure-előfizetés adott esemény rácsos tartománya alatti összes esemény rácsos témakörének részletes listáját.</span><span class="sxs-lookup"><span data-stu-id="02080-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="02080-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02080-104">SYNTAX</span></span>

### <span data-ttu-id="02080-105">DomainTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02080-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02080-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="02080-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02080-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="02080-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02080-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02080-108">DESCRIPTION</span></span>
<span data-ttu-id="02080-109">A Get-AzEventGridDomainTopic parancsmag az aktuális Azure-előfizetésben egy adott tartományba tartozó adott esemény rácsa vagy az esemény rácsvonalai területének adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="02080-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="02080-110">Ha a domain-téma neve meg van határozva, az egyetlen esemény rácsvonalai tartománya témakör részleteit adja vissza a függvény.</span><span class="sxs-lookup"><span data-stu-id="02080-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="02080-111">Ha a domain topic neve nincs megadva, a megadott tartománynév alatti tartományi témakörök listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="02080-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="02080-112">A listában visszaadott elemek számát a legfelső paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="02080-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="02080-113">Ha a felső érték nincs megadva vagy $null, a lista a tartomány összes témakörének elemét fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="02080-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="02080-114">Egyéb esetben a felső ikon jelzi a listában a visszaadott elemek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="02080-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="02080-115">Ha további tartományi témakörök is elérhetők, a következő hívásban a NextLink értékét kell használni a tartomány témaköreinek következő lapjának beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="02080-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="02080-116">Végül a ODataQuery paraméter a keresési eredmények szűrésének végrehajtásához használható.</span><span class="sxs-lookup"><span data-stu-id="02080-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="02080-117">A szűrési lekérdezés csak a név tulajdonságot használó OData szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="02080-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="02080-118">A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="02080-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="02080-119">Példák</span><span class="sxs-lookup"><span data-stu-id="02080-119">EXAMPLES</span></span>

### <span data-ttu-id="02080-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="02080-120">Example 1</span></span>

<span data-ttu-id="02080-121">Az Event Grid domain témakörének részleteit az \` DomainTopic1 \` \` -tartomány Domain1 \` az erőforráscsoport MyResourceGroupName csoportban találhatja meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="02080-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="02080-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="02080-122">Example 2</span></span>

<span data-ttu-id="02080-123">Az Event Grid domain topic \` DomainTopic1 az \` esemény rácsa \` Domain1 az \` erőforráscsoport \` MyResourceGroupName \` az ResourceId beállítás segítségével.</span><span class="sxs-lookup"><span data-stu-id="02080-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="02080-124">3. példa</span><span class="sxs-lookup"><span data-stu-id="02080-124">Example 3</span></span>

<span data-ttu-id="02080-125">Az esemény rácsa tartomány Domain1 az esemény rácsa csoportban \` \` az \` MyResourceGroupName \` nélkül (az összes eredmény egyetlen lövésben ad eredményül).</span><span class="sxs-lookup"><span data-stu-id="02080-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="02080-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="02080-126">Example 4</span></span>

<span data-ttu-id="02080-127">Az esemény rácsa tartomány \` Domain1 az \` MyResourceGroupName nélküli erőforráscsoport-Kategóriák listájában, \` \` oldalszámozás nélkül (minden eredmény egyetlen lövésben ad eredményül) a ResourceId beállítás használatával</span><span class="sxs-lookup"><span data-stu-id="02080-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="02080-128">Példa 5</span><span class="sxs-lookup"><span data-stu-id="02080-128">Example 5</span></span>

<span data-ttu-id="02080-129">Felsorolhatja az esemény rácsa tartományi témaköröket (ha vannak ilyenek) az \` erőforráscsoport MyResourceGroupName a tartományi Domain1 csoportban \` \` \` , amely megfelel az $odataFilter Query 10 tartományi témaköreinek.</span><span class="sxs-lookup"><span data-stu-id="02080-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="02080-130">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="02080-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="02080-131">Annak érdekében, hogy a következő oldal (ok) a domain-témakörök beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridDomainTopic és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="02080-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="02080-132">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="02080-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="02080-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02080-133">PARAMETERS</span></span>

### <span data-ttu-id="02080-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02080-134">-DefaultProfile</span></span>
<span data-ttu-id="02080-135">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02080-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02080-136">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="02080-136">-DomainName</span></span>
<span data-ttu-id="02080-137">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="02080-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02080-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02080-138">-Name</span></span>
<span data-ttu-id="02080-139">EventGrid a tartomány témájának nevét.</span><span class="sxs-lookup"><span data-stu-id="02080-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02080-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="02080-140">-NextLink</span></span>
<span data-ttu-id="02080-141">A beszerzett források következő lapjának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="02080-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="02080-142">Ezt az értéket az első Get-AzEventGrid parancsmag-hívással kapjuk meg, ha további források is elérhetők a lekérdezéshez.</span><span class="sxs-lookup"><span data-stu-id="02080-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02080-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="02080-143">-ODataQuery</span></span>
<span data-ttu-id="02080-144">A lista eredményének szűréséhez használt OData lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="02080-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="02080-145">A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="02080-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02080-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02080-146">-ResourceGroupName</span></span>
<span data-ttu-id="02080-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02080-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02080-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02080-148">-ResourceId</span></span>
<span data-ttu-id="02080-149">Az esemény rácsa vagy a rács tartománya témakört megadó erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="02080-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="02080-150">-Top</span><span class="sxs-lookup"><span data-stu-id="02080-150">-Top</span></span>
<span data-ttu-id="02080-151">A lista eredményének szűréséhez használt OData lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="02080-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="02080-152">A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="02080-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02080-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02080-153">CommonParameters</span></span>
<span data-ttu-id="02080-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02080-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02080-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02080-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02080-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02080-156">INPUTS</span></span>

### <span data-ttu-id="02080-157">System. String</span><span class="sxs-lookup"><span data-stu-id="02080-157">System.String</span></span>

### <span data-ttu-id="02080-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="02080-158">System.Int32</span></span>

## <span data-ttu-id="02080-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02080-159">OUTPUTS</span></span>

### <span data-ttu-id="02080-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="02080-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="02080-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="02080-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="02080-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02080-162">NOTES</span></span>

## <span data-ttu-id="02080-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02080-163">RELATED LINKS</span></span>
