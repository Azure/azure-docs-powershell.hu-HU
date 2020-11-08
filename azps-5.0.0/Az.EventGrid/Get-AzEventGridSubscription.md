---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185472"
---
# <span data-ttu-id="08242-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="08242-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="08242-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08242-102">SYNOPSIS</span></span>
<span data-ttu-id="08242-103">Beolvassa az esemény előfizetésének részleteit, vagy megkapja az aktuális Azure-előfizetésben az összes esemény-előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="08242-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="08242-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08242-104">SYNTAX</span></span>

### <span data-ttu-id="08242-105">EventSubscriptionTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08242-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08242-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="08242-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08242-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08242-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08242-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08242-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08242-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08242-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08242-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08242-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08242-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08242-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08242-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="08242-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08242-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="08242-113">DESCRIPTION</span></span>
<span data-ttu-id="08242-114">A Get-AzEventGridSubscription parancsmag a megadott esemény rácsra szóló előfizetésének részleteire, illetve az aktuális Azure-előfizetésben vagy az erőforráscsoport-előfizetések listájára kerül.</span><span class="sxs-lookup"><span data-stu-id="08242-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="08242-115">Ha az esemény-előfizetés neve meg van határozva, az egyetlen eseményből álló rácsra szóló előfizetés adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="08242-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="08242-116">Ha az esemény-előfizetés neve nincs megadva, a program az esemény-előfizetések listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="08242-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="08242-117">A listában visszaadott elemek számát a legfelső paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="08242-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="08242-118">Ha a felső érték nincs megadva vagy $null, a lista a minden esemény előfizetési elemét fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="08242-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="08242-119">Egyéb esetben a felső ikon jelzi a listában a visszaadott elemek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="08242-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="08242-120">Ha további esemény-előfizetések is elérhetők, a NextLink lévő értéket a következő hívásban kell használnia az esemény-előfizetések következő lapjának beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="08242-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="08242-121">Végül a ODataQuery paraméter a keresési eredmények szűrésének végrehajtásához használható.</span><span class="sxs-lookup"><span data-stu-id="08242-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="08242-122">A szűrési lekérdezés csak a név tulajdonságot használó OData szintaxist követi.</span><span class="sxs-lookup"><span data-stu-id="08242-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="08242-123">A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="08242-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="08242-124">Példák</span><span class="sxs-lookup"><span data-stu-id="08242-124">EXAMPLES</span></span>

### <span data-ttu-id="08242-125">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08242-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="08242-126">A \` EventSubscription1 \` \` téma1 \` az erőforráscsoport MyResourceGroupName című témakörben létrehozott esemény- \` előfizetési adatok részleteit kapja meg \` .</span><span class="sxs-lookup"><span data-stu-id="08242-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08242-127">2. példa</span><span class="sxs-lookup"><span data-stu-id="08242-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="08242-128">A \` \` téma1 az erőforráscsoport MyResourceGroupName, a teljes végpont URL-EventSubscription1 létrehozott esemény-előfizetési adatok részleteit kapja \` \` \` \` meg, ha ez egy webhorogon alapuló esemény előfizetése.</span><span class="sxs-lookup"><span data-stu-id="08242-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="08242-129">3. példa</span><span class="sxs-lookup"><span data-stu-id="08242-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="08242-130">Az erőforráscsoportok MyResourceGroupName a témakör téma1 létrehozott összes esemény-előfizetést felsorolhatja \` \` \` \` oldalszámozás nélkül.</span><span class="sxs-lookup"><span data-stu-id="08242-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="08242-131">4. példa</span><span class="sxs-lookup"><span data-stu-id="08242-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="08242-132">Felsorolhatja az első 10 esemény előfizetését (ha vannak ilyenek), \` \` amelyeket az erőforráscsoport \` MyResourceGroupName a téma1, \` amely megfelel a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="08242-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="08242-133">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08242-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08242-134">Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08242-135">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08242-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="08242-136">Példa 5</span><span class="sxs-lookup"><span data-stu-id="08242-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="08242-137">A EventSubscription1 MyResourceGroupName létrehozott esemény-előfizetési adatok részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="08242-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08242-138">6. példa</span><span class="sxs-lookup"><span data-stu-id="08242-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="08242-139">Az \` \` aktuálisan kijelölt Azure-előfizetéshez létrehozott EventSubscription1-előfizetés részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="08242-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="08242-140">7. példa</span><span class="sxs-lookup"><span data-stu-id="08242-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="08242-141">Beolvassa az erőforráscsoport \` MyResourceGroupName nélküli, oldalszámozás nélküli globális esemény-előfizetések listáját \` .</span><span class="sxs-lookup"><span data-stu-id="08242-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="08242-142">8. példa</span><span class="sxs-lookup"><span data-stu-id="08242-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="08242-143">Sorolja fel az első 5 esemény előfizetését (ha vannak) az erőforráscsoport \` MyResourceGroupName \` , amely megfelel a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="08242-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="08242-144">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08242-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08242-145">Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08242-146">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08242-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="08242-147">Példa 9</span><span class="sxs-lookup"><span data-stu-id="08242-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="08242-148">Beolvassa az aktuálisan kijelölt Azure-előfizetéssel létrehozott globális esemény-előfizetések listáját oldalszámozás nélkül.</span><span class="sxs-lookup"><span data-stu-id="08242-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="08242-149">10. példa</span><span class="sxs-lookup"><span data-stu-id="08242-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="08242-150">Felsorolhatja az aktuálisan kijelölt Azure-előfizetésben létrehozott első 15 globális esemény-előfizetést (ha van ilyen), amely megfelel a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="08242-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="08242-151">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08242-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08242-152">Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08242-153">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08242-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="08242-154">Példa 11</span><span class="sxs-lookup"><span data-stu-id="08242-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="08242-155">A \` \` megadott helyen, \` oldalszámozás nélküli westus2-előfizetések listáját kapja meg az erőforráscsoport MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08242-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="08242-156">Példa 12</span><span class="sxs-lookup"><span data-stu-id="08242-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="08242-157">Felsoroljuk az első 15 regionális esemény előfizetését (ha vannak ilyenek) az erőforráscsoport \` MyResourceGroupName \` , \` \` amely megfelel a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="08242-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="08242-158">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08242-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08242-159">Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08242-160">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08242-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="08242-161">Példa 13</span><span class="sxs-lookup"><span data-stu-id="08242-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="08242-162">A megadott EventHub-alapú névtérhez létrehozott összes esemény-előfizetés listáját adja meg oldalszámozás nélkül.</span><span class="sxs-lookup"><span data-stu-id="08242-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="08242-163">14 példa</span><span class="sxs-lookup"><span data-stu-id="08242-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="08242-164">A megadott EventHub-névtérhez létrehozott első 25 esemény-előfizetések (ha vannak) listája, amely megfelel a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="08242-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="08242-165">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08242-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08242-166">Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08242-167">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08242-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="08242-168">Példa 15</span><span class="sxs-lookup"><span data-stu-id="08242-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="08242-169">A megadott EventHub-előfizetések listáját adja meg a megadott helyen, oldalszámozás nélkül.</span><span class="sxs-lookup"><span data-stu-id="08242-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="08242-170">16 példa</span><span class="sxs-lookup"><span data-stu-id="08242-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="08242-171">Felsorolhatja az első 15 esemény előfizetését (ha van ilyen) a megadott EventHub-névterekhez (a megadott helyen), amely megfelel a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="08242-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="08242-172">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08242-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08242-173">Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08242-174">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08242-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="08242-175">17 példa</span><span class="sxs-lookup"><span data-stu-id="08242-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="08242-176">Megkeresi az adott erőforráscsoport számára létrehozott összes esemény-előfizetést, oldalszámozás nélkül.</span><span class="sxs-lookup"><span data-stu-id="08242-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="08242-177">18 példa</span><span class="sxs-lookup"><span data-stu-id="08242-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="08242-178">Felsorolhatja az adott erőforráscsoport számára létrehozott első 100-előfizetéseket (ha vannak ilyenek), amelyek megfelelnek a $odataFilter lekérdezésnek.</span><span class="sxs-lookup"><span data-stu-id="08242-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="08242-179">Ha további találatok is elérhetők, akkor a $result. A NextLink nem lesz $null.</span><span class="sxs-lookup"><span data-stu-id="08242-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="08242-180">Annak érdekében, hogy a következő oldal (ok) az esemény-előfizetések beszerzése, a felhasználó várhatóan újra felhívhatja Get-AzEventGridSubscription és használja az eredményt. Az előző hívásból nyert NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="08242-181">A hívónak a találatok után leállnia kell. A NextLink $null válik.</span><span class="sxs-lookup"><span data-stu-id="08242-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="08242-182">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08242-182">PARAMETERS</span></span>

### <span data-ttu-id="08242-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08242-183">-DefaultProfile</span></span>
<span data-ttu-id="08242-184">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08242-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08242-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="08242-185">-DomainInputObject</span></span>
<span data-ttu-id="08242-186">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="08242-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="08242-187">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="08242-187">-DomainName</span></span>
<span data-ttu-id="08242-188">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="08242-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="08242-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="08242-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="08242-190">EventGrid objektum</span><span class="sxs-lookup"><span data-stu-id="08242-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="08242-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="08242-191">-DomainTopicName</span></span>
<span data-ttu-id="08242-192">EventGrid a tartomány témájának nevét.</span><span class="sxs-lookup"><span data-stu-id="08242-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="08242-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="08242-193">-EventSubscriptionName</span></span>
<span data-ttu-id="08242-194">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="08242-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="08242-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="08242-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="08242-196">Adja meg az esemény-előfizetés célhelyének teljes URL-címét.</span><span class="sxs-lookup"><span data-stu-id="08242-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="08242-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08242-197">-InputObject</span></span>
<span data-ttu-id="08242-198">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="08242-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="08242-199">-Hely</span><span class="sxs-lookup"><span data-stu-id="08242-199">-Location</span></span>
<span data-ttu-id="08242-200">Helyre</span><span class="sxs-lookup"><span data-stu-id="08242-200">Location</span></span>

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

### <span data-ttu-id="08242-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="08242-201">-NextLink</span></span>
<span data-ttu-id="08242-202">A beszerzett források következő lapjának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="08242-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="08242-203">Ezt az értéket az első Get-AzEventGrid parancsmag-hívással kapjuk meg, ha további források is elérhetők a lekérdezéshez.</span><span class="sxs-lookup"><span data-stu-id="08242-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="08242-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="08242-204">-ODataQuery</span></span>
<span data-ttu-id="08242-205">A lista eredményének szűréséhez használt OData lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="08242-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="08242-206">A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="08242-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="08242-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08242-207">-ResourceGroupName</span></span>
<span data-ttu-id="08242-208">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="08242-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="08242-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08242-209">-ResourceId</span></span>
<span data-ttu-id="08242-210">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetéseket létrehozták.</span><span class="sxs-lookup"><span data-stu-id="08242-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="08242-211">-Top</span><span class="sxs-lookup"><span data-stu-id="08242-211">-Top</span></span>
<span data-ttu-id="08242-212">A lista eredményének szűréséhez használt OData lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="08242-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="08242-213">A szűrés jelenleg csak a Name (név) tulajdonságon engedélyezett. A támogatott műveletek közé tartoznak az alábbiak: az EQ (egyenlő), a ne (nem egyenlő) és a és nem.</span><span class="sxs-lookup"><span data-stu-id="08242-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="08242-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="08242-214">-TopicName</span></span>
<span data-ttu-id="08242-215">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="08242-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="08242-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="08242-216">-TopicTypeName</span></span>
<span data-ttu-id="08242-217">TopicType neve</span><span class="sxs-lookup"><span data-stu-id="08242-217">TopicType name</span></span>

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

### <span data-ttu-id="08242-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08242-218">CommonParameters</span></span>
<span data-ttu-id="08242-219">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08242-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08242-220">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="08242-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08242-221">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08242-221">INPUTS</span></span>

### <span data-ttu-id="08242-222">System. String</span><span class="sxs-lookup"><span data-stu-id="08242-222">System.String</span></span>

### <span data-ttu-id="08242-223">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="08242-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="08242-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="08242-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="08242-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="08242-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="08242-226">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="08242-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="08242-227">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08242-227">OUTPUTS</span></span>

### <span data-ttu-id="08242-228">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="08242-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="08242-229">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08242-229">NOTES</span></span>

## <span data-ttu-id="08242-230">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08242-230">RELATED LINKS</span></span>