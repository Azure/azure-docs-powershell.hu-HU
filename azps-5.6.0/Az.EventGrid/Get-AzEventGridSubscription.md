---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938794"
---
# <span data-ttu-id="cc923-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cc923-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="cc923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc923-102">SYNOPSIS</span></span>
<span data-ttu-id="cc923-103">Lekérte egy esemény-előfizetés részleteit, vagy lekérte az aktuális Azure-előfizetés összes esemény-előfizetésének listáját.</span><span class="sxs-lookup"><span data-stu-id="cc923-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="cc923-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc923-104">SYNTAX</span></span>

### <span data-ttu-id="cc923-105">EventSubscriptionTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc923-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc923-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc923-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc923-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc923-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc923-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc923-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc923-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc923-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc923-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc923-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc923-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc923-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc923-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc923-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc923-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc923-113">DESCRIPTION</span></span>
<span data-ttu-id="cc923-114">A Get-AzEventGridSubscription parancsmag vagy egy megadott Event Grid-előfizetés adatait, vagy az aktuális Azure-előfizetés vagy erőforráscsoport eseményrács-előfizetésének listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cc923-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="cc923-115">Ha meg van biztosítanak egy esemény-előfizetés nevét, a rendszer visszaadja egyetlen Eseményrács-előfizetés adatait.</span><span class="sxs-lookup"><span data-stu-id="cc923-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="cc923-116">Ha az esemény-előfizetés neve nem szerepel, a visszaadott érték az összes esemény-előfizetés listája lesz.</span><span class="sxs-lookup"><span data-stu-id="cc923-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="cc923-117">A listában visszaadott elemek számát a Felső paraméter vezérli.</span><span class="sxs-lookup"><span data-stu-id="cc923-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="cc923-118">Ha a felső érték nincs megadva vagy nincs $null, a lista az összes esemény-előfizetési elemet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cc923-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="cc923-119">Ellenkező esetben a Top a listában visszaadott elemek maximális számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="cc923-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="cc923-120">Ha még több esemény-előfizetés áll rendelkezésre, a NextLink értékét a következő hívásban kell használnia az esemény-előfizetések következő lapjára való feliratkozáshoz.</span><span class="sxs-lookup"><span data-stu-id="cc923-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="cc923-121">Végül az ODataQuery paramétert használjuk a keresési eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="cc923-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="cc923-122">A szűrő lekérdezés csak a Name tulajdonságot használó OData-szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="cc923-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="cc923-123">A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="cc923-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="cc923-124">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc923-124">EXAMPLES</span></span>

### <span data-ttu-id="cc923-125">1. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="cc923-126">Az Esemény-előfizetés \` EventSubscription1 nevű, a \` \` \` \` MyResourceGroupName erőforráscsoportban a Témakör1 témaköréhez létrehozott részleteket \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cc923-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cc923-127">2. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="cc923-128">A MyResourceGroupName erőforráscsoporthoz létrehozott EventSubscription1 esemény-előfizetés adatait tartalmazza, beleértve a teljes végpont URL-címét, ha \` \` \` \` \` \` webhook-alapú esemény-előfizetésről van szükség.</span><span class="sxs-lookup"><span data-stu-id="cc923-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="cc923-129">3. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="cc923-130">A MyResourceGroupName erőforráscsoport Topic1 témaköréhez létrehozott összes esemény-előfizetés listája \` \` \` \` tördelés nélkül.</span><span class="sxs-lookup"><span data-stu-id="cc923-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="cc923-131">4. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="cc923-132">List the first 10 event subscriptions (if any) created for topic \` Topic1 \` in resource group \` MyResourceGroupName \` that satesfes the $odataFilter query.</span><span class="sxs-lookup"><span data-stu-id="cc923-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="cc923-133">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="cc923-134">Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="cc923-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="cc923-135">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="cc923-136">5. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="cc923-137">A \` \` \` MyResourceGroupName erőforráscsoporthoz létrehozott EventSubscription1 esemény-előfizetés adatait \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cc923-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cc923-138">6. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="cc923-139">Az aktuálisan kijelölt Azure-előfizetéshez létrehozott \` EventSubscription1 \` esemény-előfizetés adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cc923-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="cc923-140">7. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="cc923-141">A MyResourceGroupName erőforráscsoport alatt létrehozott összes globális esemény-előfizetés listáját \` \` tördelés nélkül beveszi.</span><span class="sxs-lookup"><span data-stu-id="cc923-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="cc923-142">8. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="cc923-143">Sorolja fel a MyResourceGroupName erőforráscsoportban létrehozott első 5 esemény-előfizetést (ha van ilyen), amely megfelel a $odataFilter \` \` lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="cc923-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="cc923-144">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="cc923-145">Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="cc923-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="cc923-146">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="cc923-147">9. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="cc923-148">A jelenleg kijelölt Azure-előfizetés alatt létrehozott összes globális esemény-előfizetés listáját tördelés nélkül lejátssa.</span><span class="sxs-lookup"><span data-stu-id="cc923-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="cc923-149">10. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="cc923-150">Sorolja fel az aktuálisan kiválasztott Azure-előfizetés alatt létrehozott első 15 globális esemény-előfizetést (ha van ilyen), amely megfelel a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="cc923-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="cc923-151">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="cc923-152">Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="cc923-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="cc923-153">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="cc923-154">11. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="cc923-155">A MyResourceGroupName erőforráscsoportban létrehozott összes regionális esemény-előfizetés listáját a \` \` megadott \` helyen, a westus2 helyen, tördelés nélkül \` adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc923-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="cc923-156">12. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="cc923-157">List the first 15 regional event subscriptions (if any) created under resource group \` MyResourceGroupName \` in the specified location westus2 that \` \` satisfes the $odataFilter query.</span><span class="sxs-lookup"><span data-stu-id="cc923-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="cc923-158">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="cc923-159">Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="cc923-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="cc923-160">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="cc923-161">13. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="cc923-162">Tördelés nélkül megkapja a megadott EventHub névtérhez létrehozott összes esemény-előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="cc923-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="cc923-163">14. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="cc923-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfes the $odataFilter query.</span><span class="sxs-lookup"><span data-stu-id="cc923-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="cc923-165">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="cc923-166">Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="cc923-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="cc923-167">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="cc923-168">15. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="cc923-169">A megadott témakörtípushoz (EventHub névterek) létrehozott összes esemény-előfizetés listáját tördelés nélkül beveszi a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="cc923-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="cc923-170">16. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="cc923-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfes the $odataFilter query.</span><span class="sxs-lookup"><span data-stu-id="cc923-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="cc923-172">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="cc923-173">Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="cc923-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="cc923-174">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="cc923-175">17. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="cc923-176">Tördelés nélkül beveszi az adott erőforráscsoporthoz létrehozott összes esemény-előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="cc923-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="cc923-177">18. példa</span><span class="sxs-lookup"><span data-stu-id="cc923-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="cc923-178">List the first 100 event subscriptions (if any) created for the specific resource group that satesfes the $odataFilter query.</span><span class="sxs-lookup"><span data-stu-id="cc923-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="cc923-179">Ha több találat érhető el, a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="cc923-180">Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink.</span><span class="sxs-lookup"><span data-stu-id="cc923-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="cc923-181">A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.</span><span class="sxs-lookup"><span data-stu-id="cc923-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="cc923-182">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc923-182">PARAMETERS</span></span>

### <span data-ttu-id="cc923-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc923-183">-DefaultProfile</span></span>
<span data-ttu-id="cc923-184">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cc923-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc923-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="cc923-185">-DomainInputObject</span></span>
<span data-ttu-id="cc923-186">EventGrid Domain objektum.</span><span class="sxs-lookup"><span data-stu-id="cc923-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="cc923-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="cc923-187">-DomainName</span></span>
<span data-ttu-id="cc923-188">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="cc923-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="cc923-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="cc923-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="cc923-190">EventGrid domain Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="cc923-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="cc923-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="cc923-191">-DomainTopicName</span></span>
<span data-ttu-id="cc923-192">EventGrid tartomány témakörének neve.</span><span class="sxs-lookup"><span data-stu-id="cc923-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="cc923-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cc923-193">-EventSubscriptionName</span></span>
<span data-ttu-id="cc923-194">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="cc923-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="cc923-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="cc923-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="cc923-196">Tartalmazza az esemény-előfizetés célhelyének teljes végpont URL-címét.</span><span class="sxs-lookup"><span data-stu-id="cc923-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="cc923-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc923-197">-InputObject</span></span>
<span data-ttu-id="cc923-198">EventGrid Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="cc923-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="cc923-199">-Location</span><span class="sxs-lookup"><span data-stu-id="cc923-199">-Location</span></span>
<span data-ttu-id="cc923-200">Hely</span><span class="sxs-lookup"><span data-stu-id="cc923-200">Location</span></span>

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

### <span data-ttu-id="cc923-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="cc923-201">-NextLink</span></span>
<span data-ttu-id="cc923-202">A következő behozni szükséges erőforrások lapjára mutató hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="cc923-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="cc923-203">Ezt az értéket az első parancsmag-Get-AzEventGrid akkor lehet beszerezni, ha még több erőforrás áll rendelkezésre a lekérdezhető erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="cc923-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="cc923-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="cc923-204">-ODataQuery</span></span>
<span data-ttu-id="cc923-205">A lista eredményeinek szűréséhez használt OData-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="cc923-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="cc923-206">A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="cc923-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="cc923-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc923-207">-ResourceGroupName</span></span>
<span data-ttu-id="cc923-208">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc923-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="cc923-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc923-209">-ResourceId</span></span>
<span data-ttu-id="cc923-210">Annak az erőforrásnak az azonosítója, amelyhez esemény-előfizetések létrejöttek.</span><span class="sxs-lookup"><span data-stu-id="cc923-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="cc923-211">-Top</span><span class="sxs-lookup"><span data-stu-id="cc923-211">-Top</span></span>
<span data-ttu-id="cc923-212">A lista eredményeinek szűréséhez használt OData-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="cc923-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="cc923-213">A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.</span><span class="sxs-lookup"><span data-stu-id="cc923-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="cc923-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="cc923-214">-TopicName</span></span>
<span data-ttu-id="cc923-215">EventGrid-témakör neve.</span><span class="sxs-lookup"><span data-stu-id="cc923-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="cc923-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="cc923-216">-TopicTypeName</span></span>
<span data-ttu-id="cc923-217">TopicType name</span><span class="sxs-lookup"><span data-stu-id="cc923-217">TopicType name</span></span>

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

### <span data-ttu-id="cc923-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc923-218">CommonParameters</span></span>
<span data-ttu-id="cc923-219">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc923-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc923-220">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc923-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc923-221">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc923-221">INPUTS</span></span>

### <span data-ttu-id="cc923-222">System.String</span><span class="sxs-lookup"><span data-stu-id="cc923-222">System.String</span></span>

### <span data-ttu-id="cc923-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="cc923-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="cc923-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="cc923-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="cc923-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cc923-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="cc923-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cc923-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cc923-227">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc923-227">OUTPUTS</span></span>

### <span data-ttu-id="cc923-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="cc923-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="cc923-229">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc923-229">NOTES</span></span>

## <span data-ttu-id="cc923-230">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc923-230">RELATED LINKS</span></span>
