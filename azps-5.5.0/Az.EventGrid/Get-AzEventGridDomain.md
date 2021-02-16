---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153194"
---
# <span data-ttu-id="9033a-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="9033a-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="9033a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9033a-102">SYNOPSIS</span></span>
<span data-ttu-id="9033a-103">Lekérte egy Eseményrács tartomány adatait, vagy lekérte az aktuális Azure-előfizetés összes Eseményrács tartományának listáját.</span><span class="sxs-lookup"><span data-stu-id="9033a-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="9033a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9033a-104">SYNTAX</span></span>

### <span data-ttu-id="9033a-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9033a-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9033a-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9033a-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9033a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9033a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9033a-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="9033a-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9033a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9033a-109">DESCRIPTION</span></span>
<span data-ttu-id="9033a-110">A Get-AzEventGridDomain parancsmag vagy egy megadott Event Grid tartomány adatait, vagy az aktuális Azure-előfizetés összes Eseményrács tartományának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="9033a-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="9033a-111">Ha meg van biztosítanak egy tartománynevet, egyetlen Event Grid tartomány adatait ad vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="9033a-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="9033a-112">Ha a tartománynév nem szerepel a listában, a visszaadott tartománylistát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9033a-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="9033a-113">A listában visszaadott elemek számát a Felső paraméter vezérli.</span><span class="sxs-lookup"><span data-stu-id="9033a-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="9033a-114">Ha a felső érték nincs megadva vagy nincs $null, akkor a lista az összes visszaadott tartományelemet egyszerre fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9033a-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="9033a-115">Ellenkező esetben a Top a listában visszaadott elemek maximális számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="9033a-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="9033a-116">Ha további tartományok is elérhetők, a következő hívásban a NextLink értékét kell használnia a következő tartománylap lehívására.</span><span class="sxs-lookup"><span data-stu-id="9033a-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="9033a-117">Végül az ODataQuery paramétert használjuk a keresési eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="9033a-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="9033a-118">A szűrő lekérdezés csak a Name tulajdonságot használó OData szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="9033a-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="9033a-119">A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="9033a-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="9033a-120">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9033a-120">EXAMPLES</span></span>

### <span data-ttu-id="9033a-121">1. példa</span><span class="sxs-lookup"><span data-stu-id="9033a-121">Example 1</span></span>

<span data-ttu-id="9033a-122">A \` \` \` MyResourceGroupName erőforráscsoport Eseményrács tartomány1 tartományának adatait \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9033a-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="9033a-123">2. példa</span><span class="sxs-lookup"><span data-stu-id="9033a-123">Example 2</span></span>

<span data-ttu-id="9033a-124">A \` \` \` MyResourceGroupName erőforráscsoport Eseményrács tartomány1 tartományának adatait a ResourceId lehetőség használatával \` kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9033a-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="9033a-125">3. példa</span><span class="sxs-lookup"><span data-stu-id="9033a-125">Example 3</span></span>

<span data-ttu-id="9033a-126">List all Event Grid domains in resource group \` MyResourceGroupName \` without pagination (all domains are returned in one shot)</span><span class="sxs-lookup"><span data-stu-id="9033a-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="9033a-127">4. példa</span><span class="sxs-lookup"><span data-stu-id="9033a-127">Example 4</span></span>

<span data-ttu-id="9033a-128">Sorolja fel a MyResourceGroupName erőforráscsoport eseményrács tartományát (ha van ilyen), amely megfelel a $odataFilter \` \` 10 tartománynak.</span><span class="sxs-lookup"><span data-stu-id="9033a-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="9033a-129">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="9033a-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="9033a-130">A tartományok következő oldalának lehívása érdekében a felhasználó várhatóan újra Get-AzEventGridDomain és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="9033a-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="9033a-131">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="9033a-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="9033a-132">5. példa</span><span class="sxs-lookup"><span data-stu-id="9033a-132">Example 5</span></span>

<span data-ttu-id="9033a-133">Az Azure-előfizetés összes Eseményrács tartományának felsorolása tördelés nélkül (minden tartományt egy képben ad vissza)</span><span class="sxs-lookup"><span data-stu-id="9033a-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="9033a-134">6. példa</span><span class="sxs-lookup"><span data-stu-id="9033a-134">Example 6</span></span>

<span data-ttu-id="9033a-135">Az Azure-előfizetésben sorolja fel azokat az Eseményrács tartományokat (ha vannak), amelyek $odataFilter 20 tartományt.</span><span class="sxs-lookup"><span data-stu-id="9033a-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="9033a-136">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="9033a-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="9033a-137">A tartományok következő oldalának lehívása érdekében a felhasználó várhatóan újra hívja az Get-AzEventGridDomain és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="9033a-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="9033a-138">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="9033a-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="9033a-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9033a-139">PARAMETERS</span></span>

### <span data-ttu-id="9033a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9033a-140">-DefaultProfile</span></span>
<span data-ttu-id="9033a-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9033a-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9033a-142">-Name</span><span class="sxs-lookup"><span data-stu-id="9033a-142">-Name</span></span>
<span data-ttu-id="9033a-143">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="9033a-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9033a-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="9033a-144">-NextLink</span></span>
<span data-ttu-id="9033a-145">A következő behozni szükséges erőforrások lapjára mutató hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="9033a-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="9033a-146">Ezt az értéket az első parancsmag-Get-AzEventGrid akkor lehet beszerezni, ha még több erőforrás áll rendelkezésre a lekérdezhető erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="9033a-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="9033a-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9033a-147">-ODataQuery</span></span>
<span data-ttu-id="9033a-148">A lista eredményeinek szűréséhez használt OData-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="9033a-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="9033a-149">A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="9033a-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9033a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9033a-150">-ResourceGroupName</span></span>
<span data-ttu-id="9033a-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9033a-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9033a-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9033a-152">-ResourceId</span></span>
<span data-ttu-id="9033a-153">Az Eseményrács tartományt képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9033a-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="9033a-154">-Top</span><span class="sxs-lookup"><span data-stu-id="9033a-154">-Top</span></span>
<span data-ttu-id="9033a-155">A lekért erőforrások maximális száma.</span><span class="sxs-lookup"><span data-stu-id="9033a-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="9033a-156">Az érvényes érték 1 és 100 között lehet.</span><span class="sxs-lookup"><span data-stu-id="9033a-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="9033a-157">Ha a felső érték meg van adva, és további eredmények is elérhetők, az eredményben egy hivatkozás fog jelenni, amely a következő lekérdezni fogja a NextLinkben lekérdezni fogja a következő lapot.</span><span class="sxs-lookup"><span data-stu-id="9033a-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="9033a-158">Ha nincs megadva a felső érték, a teljes erőforráslistát egyszerre adja vissza a visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="9033a-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9033a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9033a-159">CommonParameters</span></span>
<span data-ttu-id="9033a-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9033a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9033a-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9033a-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9033a-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9033a-162">INPUTS</span></span>

### <span data-ttu-id="9033a-163">System.String</span><span class="sxs-lookup"><span data-stu-id="9033a-163">System.String</span></span>

## <span data-ttu-id="9033a-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9033a-164">OUTPUTS</span></span>

### <span data-ttu-id="9033a-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="9033a-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="9033a-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="9033a-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="9033a-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9033a-167">NOTES</span></span>

## <span data-ttu-id="9033a-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9033a-168">RELATED LINKS</span></span>
