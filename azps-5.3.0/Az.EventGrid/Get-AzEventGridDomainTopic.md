---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376808"
---
# <span data-ttu-id="ecfc4-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ecfc4-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="ecfc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecfc4-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfc4-103">Lejátsa az Eseményrács tartománytémaktémát, vagy az aktuális Azure-előfizetés eseményrács-tartományának összes eseményrács-témakörét.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="ecfc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ecfc4-104">SYNTAX</span></span>

### <span data-ttu-id="ecfc4-105">DomainTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ecfc4-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecfc4-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecfc4-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecfc4-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecfc4-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecfc4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ecfc4-108">DESCRIPTION</span></span>
<span data-ttu-id="ecfc4-109">A Get-AzEventGridDomainTopic parancsmag vagy egy megadott Event Grid tartománytémát, vagy az aktuális Azure-előfizetés egy adott tartományába sorolt Eseményrács tartománytémaktémák listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="ecfc4-110">Ha a tartománytémakör neve meg van téve, a rendszer visszaadja egyetlen Eseményrács tartománytémának a részleteit.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="ecfc4-111">Ha nem adja meg a tartomány témakörnevét, a megadott tartománynév alatti tartománytémakémák listája lesz eredményül adva.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="ecfc4-112">A listában visszaadott elemek számát a Felső paraméter vezérli.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="ecfc4-113">Ha a felső érték nincs megadva vagy nincs $null, a lista az összes tartománytémaktémát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="ecfc4-114">Ellenkező esetben a Top a listában visszaadott elemek maximális számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="ecfc4-115">Ha további tartományi témakörök is elérhetők, a következő hívásban a NextLink értékét kell használnia a tartománytémakémák következő lapjára való behíváshoz.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="ecfc4-116">Végül az ODataQuery paramétert használjuk a keresési eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="ecfc4-117">A szűrő lekérdezés csak a Name tulajdonságot használó OData szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="ecfc4-118">A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="ecfc4-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ecfc4-119">EXAMPLES</span></span>

### <span data-ttu-id="ecfc4-120">1. példa</span><span class="sxs-lookup"><span data-stu-id="ecfc4-120">Example 1</span></span>

<span data-ttu-id="ecfc4-121">A MyResourceGroupName erőforráscsoport Eseményrács tartomány1 eseményrács tartománya tartomány1 csoportjában található \` \` \` DomainTopic1 \` \` eseményrács tartományának adatait \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ecfc4-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="ecfc4-122">Example 2</span></span>

<span data-ttu-id="ecfc4-123">A MyResourceGroupName erőforráscsoport Eseményrács tartomány1 csoportjában található \` DomainTopic1 \` eseményrács tartománytémaktára vonatkozó részleteket a ResourceId lehetőség használatával kapja \` \` \` \` meg.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ecfc4-124">3. példa</span><span class="sxs-lookup"><span data-stu-id="ecfc4-124">Example 3</span></span>

<span data-ttu-id="ecfc4-125">A \` \` \` MyResourceGroupName erőforráscsoport Eseményrács tartomány1 csoportjában, tördelés nélkül sorolja fel az eseményrács összes tartományt (a találatok egy képben \` megjelenik).</span><span class="sxs-lookup"><span data-stu-id="ecfc4-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="ecfc4-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="ecfc4-126">Example 4</span></span>

<span data-ttu-id="ecfc4-127">List all Event Grid domain topics under Event Grid \` domain Domain1 \` in resource group \` MyResourceGroupName \` without pagination (all results are returned in one shot) using ResourceId option</span><span class="sxs-lookup"><span data-stu-id="ecfc4-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="ecfc4-128">5. példa</span><span class="sxs-lookup"><span data-stu-id="ecfc4-128">Example 5</span></span>

<span data-ttu-id="ecfc4-129">A \` \` MyResourceGroupName erőforráscsoport Tartomány1 csoportjában sorolja fel az Eseményrács tartománytémakra vonatkozó témaköröket (ha vannak ilyen), amelyek kielégítik az \` $odataFilter 10 tartománytémát \` egyszerre.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="ecfc4-130">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ecfc4-131">A tartománytémakémák következő oldalának lehívása érdekében a felhasználó várhatóan újra hívja a Get-AzEventGridDomainTopic és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ecfc4-132">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="ecfc4-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecfc4-133">PARAMETERS</span></span>

### <span data-ttu-id="ecfc4-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfc4-134">-DefaultProfile</span></span>
<span data-ttu-id="ecfc4-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfc4-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ecfc4-136">-DomainName</span></span>
<span data-ttu-id="ecfc4-137">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-137">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ecfc4-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ecfc4-138">-Name</span></span>
<span data-ttu-id="ecfc4-139">EventGrid tartomány témakörének neve.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-139">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ecfc4-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ecfc4-140">-NextLink</span></span>
<span data-ttu-id="ecfc4-141">A következő behozni szükséges erőforrások lapjára mutató hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="ecfc4-142">Ezt az értéket az első parancsmag-Get-AzEventGrid akkor lehet beszerezni, ha még több erőforrás áll rendelkezésre a lekérdezhető erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="ecfc4-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ecfc4-143">-ODataQuery</span></span>
<span data-ttu-id="ecfc4-144">A lista eredményeinek szűréséhez használt OData-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ecfc4-145">A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ecfc4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfc4-146">-ResourceGroupName</span></span>
<span data-ttu-id="ecfc4-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-147">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecfc4-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfc4-148">-ResourceId</span></span>
<span data-ttu-id="ecfc4-149">Az Eseményrács vagy a Rács tartománytémát képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="ecfc4-150">-Top</span><span class="sxs-lookup"><span data-stu-id="ecfc4-150">-Top</span></span>
<span data-ttu-id="ecfc4-151">A lista eredményeinek szűréséhez használt OData-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ecfc4-152">A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ecfc4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfc4-153">CommonParameters</span></span>
<span data-ttu-id="ecfc4-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfc4-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecfc4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfc4-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecfc4-156">INPUTS</span></span>

### <span data-ttu-id="ecfc4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="ecfc4-157">System.String</span></span>

### <span data-ttu-id="ecfc4-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ecfc4-158">System.Int32</span></span>

## <span data-ttu-id="ecfc4-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecfc4-159">OUTPUTS</span></span>

### <span data-ttu-id="ecfc4-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ecfc4-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="ecfc4-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="ecfc4-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="ecfc4-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ecfc4-162">NOTES</span></span>

## <span data-ttu-id="ecfc4-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecfc4-163">RELATED LINKS</span></span>
