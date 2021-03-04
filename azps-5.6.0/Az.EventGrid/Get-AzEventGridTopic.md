---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2af8125f91618cd929a9389d9327532376e92af1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938778"
---
# <span data-ttu-id="75023-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="75023-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="75023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75023-102">SYNOPSIS</span></span>
<span data-ttu-id="75023-103">Lejátsa az Eseményrács témakör részleteit, vagy az aktuális Azure-előfizetés eseményrács-témakörének listáját.</span><span class="sxs-lookup"><span data-stu-id="75023-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="75023-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75023-104">SYNTAX</span></span>

### <span data-ttu-id="75023-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75023-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75023-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75023-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75023-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="75023-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75023-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="75023-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75023-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75023-109">DESCRIPTION</span></span>
<span data-ttu-id="75023-110">A Get-AzEventGridTopic parancsmag vagy egy megadott Eseményrács-témakör adatait, vagy az aktuális Azure-előfizetés eseményrács-témakörének listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="75023-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="75023-111">Ha a témakör neve meg van adni, akkor a rendszer egyetlen eseményrácstémát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="75023-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="75023-112">Ha a témakör neve nem szerepel a listában, a visszaadott témakörlista fog visszakerülni.</span><span class="sxs-lookup"><span data-stu-id="75023-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="75023-113">A listában visszaadott elemek számát a Felső paraméter vezérli.</span><span class="sxs-lookup"><span data-stu-id="75023-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="75023-114">Ha a felső érték nincs megadva vagy nincs $null, a lista az összes témakörelemet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="75023-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="75023-115">Ellenkező esetben a Top a listában visszaadott elemek maximális számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="75023-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="75023-116">Ha további témakörök is elérhetők, a következő hívásban a NextLink értékét kell használni a témakörök következő lapjára való bejedhez.</span><span class="sxs-lookup"><span data-stu-id="75023-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="75023-117">Végül az ODataQuery paramétert használjuk a keresési eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="75023-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="75023-118">A szűrő lekérdezés csak a Name tulajdonságot használó OData-szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="75023-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="75023-119">A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="75023-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="75023-120">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75023-120">EXAMPLES</span></span>

### <span data-ttu-id="75023-121">1. példa</span><span class="sxs-lookup"><span data-stu-id="75023-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="75023-122">A \` MyResourceGroupName erőforráscsoport Eseményrács témakörÉnek \` 1. \` témakörének részleteit \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="75023-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="75023-123">2. példa</span><span class="sxs-lookup"><span data-stu-id="75023-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="75023-124">A \` MyResourceGroupName erőforráscsoport Eseményrács témakörÉnek \` 1. \` témakörének részleteit \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="75023-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="75023-125">3. példa</span><span class="sxs-lookup"><span data-stu-id="75023-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="75023-126">A MyResourceGroupName erőforráscsoport összes eseményrács-témakörének felsorolása \` \` tördelés nélkül.</span><span class="sxs-lookup"><span data-stu-id="75023-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="75023-127">4. példa</span><span class="sxs-lookup"><span data-stu-id="75023-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="75023-128">List the first 10 Event Grid topics (if any) in resource group \` MyResourceGroupName \` that satisfes the $odataFilter query.</span><span class="sxs-lookup"><span data-stu-id="75023-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="75023-129">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="75023-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="75023-130">A témakörök következő oldalának lehívása érdekében a felhasználó várhatóan újra hívja a Get-AzEventGridTopic és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="75023-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="75023-131">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="75023-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="75023-132">5. példa</span><span class="sxs-lookup"><span data-stu-id="75023-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="75023-133">Az előfizetés összes eseményrács-témakörének felsorolása tördelés nélkül.</span><span class="sxs-lookup"><span data-stu-id="75023-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="75023-134">6. példa</span><span class="sxs-lookup"><span data-stu-id="75023-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="75023-135">List the first 10 Event Grid topics (if any) in the subscription that satisfes the $odataFilter query.</span><span class="sxs-lookup"><span data-stu-id="75023-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="75023-136">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="75023-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="75023-137">A témakörök következő oldalának lehívása érdekében a felhasználó várhatóan újra hívja a Get-AzEventGridTopic és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="75023-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="75023-138">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="75023-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="75023-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75023-139">PARAMETERS</span></span>

### <span data-ttu-id="75023-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75023-140">-DefaultProfile</span></span>
<span data-ttu-id="75023-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="75023-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75023-142">-Name</span><span class="sxs-lookup"><span data-stu-id="75023-142">-Name</span></span>
<span data-ttu-id="75023-143">EventGrid-témakör neve.</span><span class="sxs-lookup"><span data-stu-id="75023-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="75023-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="75023-144">-NextLink</span></span>
<span data-ttu-id="75023-145">A következő behozni szükséges erőforrások lapjára mutató hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="75023-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="75023-146">Ezt az értéket az első parancsmag-Get-AzEventGrid akkor lehet beszerezni, ha még több erőforrás áll rendelkezésre a lekérdezhető erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="75023-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="75023-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="75023-147">-ODataQuery</span></span>
<span data-ttu-id="75023-148">A lista eredményeinek szűréséhez használt OData-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="75023-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="75023-149">A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="75023-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="75023-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75023-150">-ResourceGroupName</span></span>
<span data-ttu-id="75023-151">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75023-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="75023-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75023-152">-ResourceId</span></span>
<span data-ttu-id="75023-153">Az Eseményrács témakört képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="75023-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="75023-154">-Top</span><span class="sxs-lookup"><span data-stu-id="75023-154">-Top</span></span>
<span data-ttu-id="75023-155">A lekért erőforrások maximális száma.</span><span class="sxs-lookup"><span data-stu-id="75023-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="75023-156">Az érvényes érték 1 és 100 között lehet.</span><span class="sxs-lookup"><span data-stu-id="75023-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="75023-157">Ha a felső érték meg van adva, és további eredmények is elérhetők, az eredményben egy hivatkozás fog jelenni, amely a következő lekérdezni fogja a NextLinkben lekérdezni fog egy lapot.</span><span class="sxs-lookup"><span data-stu-id="75023-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="75023-158">Ha nincs megadva a felső érték, a teljes erőforráslistát egyszerre adja vissza a visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="75023-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="75023-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75023-159">CommonParameters</span></span>
<span data-ttu-id="75023-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75023-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75023-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75023-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75023-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75023-162">INPUTS</span></span>

### <span data-ttu-id="75023-163">System.String</span><span class="sxs-lookup"><span data-stu-id="75023-163">System.String</span></span>

### <span data-ttu-id="75023-164">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="75023-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="75023-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75023-165">OUTPUTS</span></span>

### <span data-ttu-id="75023-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="75023-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="75023-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="75023-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="75023-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75023-168">NOTES</span></span>

## <span data-ttu-id="75023-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75023-169">RELATED LINKS</span></span>
