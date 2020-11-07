---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: f2f3c3799ff16cdcc5f1091f8a66cb531cf46cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845625"
---
# <span data-ttu-id="08ff3-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="08ff3-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="08ff3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="08ff3-103">Beolvassa az esemény rácsának adatait, vagy megtekintheti az aktuális Azure-előfizetésben szereplő összes esemény rácsos tartományát.</span><span class="sxs-lookup"><span data-stu-id="08ff3-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="08ff3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08ff3-104">SYNTAX</span></span>

### <span data-ttu-id="08ff3-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08ff3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08ff3-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ff3-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08ff3-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ff3-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08ff3-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ff3-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08ff3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="08ff3-109">DESCRIPTION</span></span>
<span data-ttu-id="08ff3-110">A Get-AzEventGridDomain parancsmag az aktuális Azure-előfizetésből származó adott esemény rácsvonal-tartományának adatait vagy az összes esemény rácsos tartományának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="08ff3-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="08ff3-111">Ha a tartománynév meg van határozva, az egyetlen eseményből álló rács tartomány adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="08ff3-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="08ff3-112">Ha a tartománynév nincs megadva, a program a tartományok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="08ff3-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="08ff3-113">A listában visszaadott elemek számát a legfelső paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="08ff3-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="08ff3-114">Ha a felső érték nincs megadva vagy $null, a lista a tartomány összes, egyszerre visszaadott elemét fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="08ff3-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="08ff3-115">Egyéb esetben a felső ikon jelzi a listában a visszaadott elemek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="08ff3-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="08ff3-116">Ha további tartományok is elérhetők, a következő hívásban a NextLink értékét kell használni a tartomány következő oldalának beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="08ff3-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="08ff3-117">Végül a ODataQuery paraméter a keresési eredmények szűrésének végrehajtásához használható.</span><span class="sxs-lookup"><span data-stu-id="08ff3-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="08ff3-118">A szűrési lekérdezés csak a név tulajdonságot használó OData szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="08ff3-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="08ff3-119">A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="08ff3-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="08ff3-120">Példák</span><span class="sxs-lookup"><span data-stu-id="08ff3-120">EXAMPLES</span></span>

### <span data-ttu-id="08ff3-121">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08ff3-121">Example 1</span></span>

<span data-ttu-id="08ff3-122">Az Event Grid domain Domain1 részleteit \` kapja \` meg az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08ff3-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="08ff3-123">2. példa</span><span class="sxs-lookup"><span data-stu-id="08ff3-123">Example 2</span></span>

<span data-ttu-id="08ff3-124">Az Event Grid domain \` Domain1 az \` erőforráscsoport MyResourceGroupName a \` \` ResourceId beállítás használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="08ff3-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="08ff3-125">3. példa</span><span class="sxs-lookup"><span data-stu-id="08ff3-125">Example 3</span></span>

<span data-ttu-id="08ff3-126">Az összes esemény rácsvonal-tartományának listázása az erőforráscsoport \` MyResourceGroupName \` nélkül (az összes tartomány egy lövésben ad vissza)</span><span class="sxs-lookup"><span data-stu-id="08ff3-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="08ff3-127">4. példa</span><span class="sxs-lookup"><span data-stu-id="08ff3-127">Example 4</span></span>

<span data-ttu-id="08ff3-128">Felsorolhatja azokat az MyResourceGroupName-tartományokat (ha vannak ilyenek) az erőforráscsoport-tartományokban \` \` , amelyek a $odataFilter lekérdezés 10 tartományát egyszerre teljesítik.</span><span class="sxs-lookup"><span data-stu-id="08ff3-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="08ff3-129">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08ff3-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08ff3-130">Annak érdekében, hogy a következő oldal (ok) a tartományokat, a felhasználó várhatóan újra hívja Get-AzEventGridDomain és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08ff3-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08ff3-131">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08ff3-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="08ff3-132">Példa 5</span><span class="sxs-lookup"><span data-stu-id="08ff3-132">Example 5</span></span>

<span data-ttu-id="08ff3-133">Az Azure-előfizetésben lévő összes esemény rácsának listázása oldalszámozás nélkül (az összes tartomány egy lövésben ad vissza)</span><span class="sxs-lookup"><span data-stu-id="08ff3-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="08ff3-134">6. példa</span><span class="sxs-lookup"><span data-stu-id="08ff3-134">Example 6</span></span>

<span data-ttu-id="08ff3-135">Felsorolhatja az Azure-előfizetésben az esemény rácsának tartományait (ha vannak ilyenek), amelyek megfelelnek a $odataFilter lekérdezés 20 tartományának egyszerre.</span><span class="sxs-lookup"><span data-stu-id="08ff3-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="08ff3-136">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08ff3-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08ff3-137">Annak érdekében, hogy a következő oldal (ok) a tartományokat, a felhasználó várhatóan újra hívja Get-AzEventGridDomain és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08ff3-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08ff3-138">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08ff3-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="08ff3-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08ff3-139">PARAMETERS</span></span>

### <span data-ttu-id="08ff3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ff3-140">-DefaultProfile</span></span>
<span data-ttu-id="08ff3-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08ff3-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08ff3-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08ff3-142">-Name</span></span>
<span data-ttu-id="08ff3-143">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="08ff3-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ff3-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="08ff3-144">-NextLink</span></span>
<span data-ttu-id="08ff3-145">A beszerzett források következő lapjának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="08ff3-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="08ff3-146">Ezt az értéket az első Get-AzEventGrid parancsmag-hívással kapjuk meg, ha további források is elérhetők a lekérdezéshez.</span><span class="sxs-lookup"><span data-stu-id="08ff3-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="08ff3-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="08ff3-147">-ODataQuery</span></span>
<span data-ttu-id="08ff3-148">A lista eredményének szűréséhez használt OData lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="08ff3-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="08ff3-149">A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="08ff3-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ff3-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ff3-150">-ResourceGroupName</span></span>
<span data-ttu-id="08ff3-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="08ff3-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ff3-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08ff3-152">-ResourceId</span></span>
<span data-ttu-id="08ff3-153">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="08ff3-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="08ff3-154">-Top</span><span class="sxs-lookup"><span data-stu-id="08ff3-154">-Top</span></span>
<span data-ttu-id="08ff3-155">A beszerezni kívánt források maximális száma.</span><span class="sxs-lookup"><span data-stu-id="08ff3-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="08ff3-156">Az érvényes érték 1 és 100 között van.</span><span class="sxs-lookup"><span data-stu-id="08ff3-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="08ff3-157">Ha a felső érték van megadva, és további találatok is elérhetők, az eredmény a következő oldalra mutató hivatkozást fogja tartalmazni a NextLink.</span><span class="sxs-lookup"><span data-stu-id="08ff3-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="08ff3-158">Ha a felső érték nincs megadva, az erőforrások teljes listája azonnal visszakerül.</span><span class="sxs-lookup"><span data-stu-id="08ff3-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ff3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ff3-159">CommonParameters</span></span>
<span data-ttu-id="08ff3-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08ff3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ff3-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ff3-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ff3-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08ff3-162">INPUTS</span></span>

### <span data-ttu-id="08ff3-163">System. String</span><span class="sxs-lookup"><span data-stu-id="08ff3-163">System.String</span></span>

## <span data-ttu-id="08ff3-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08ff3-164">OUTPUTS</span></span>

### <span data-ttu-id="08ff3-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="08ff3-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="08ff3-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="08ff3-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="08ff3-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08ff3-167">NOTES</span></span>

## <span data-ttu-id="08ff3-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08ff3-168">RELATED LINKS</span></span>
