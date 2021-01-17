---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347381"
---
# <span data-ttu-id="d633b-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d633b-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="d633b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d633b-102">SYNOPSIS</span></span>
<span data-ttu-id="d633b-103">Házirend-kiértékelési eseményeket hoz létre, amikor erőforrások jönnek létre vagy frissülnek.</span><span class="sxs-lookup"><span data-stu-id="d633b-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="d633b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d633b-104">SYNTAX</span></span>

### <span data-ttu-id="d633b-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d633b-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633b-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="d633b-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633b-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="d633b-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633b-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="d633b-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633b-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="d633b-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633b-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="d633b-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633b-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="d633b-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633b-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="d633b-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d633b-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d633b-113">DESCRIPTION</span></span>
<span data-ttu-id="d633b-114">Házirend-kiértékelési eseményeket hoz létre, amikor erőforrások jönnek létre vagy frissülnek.</span><span class="sxs-lookup"><span data-stu-id="d633b-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="d633b-115">A házirendesemény-rekordok lekérdezhetők különböző hatókörökben a megadott időintervallum alapján (ez az alapértelmezett érték az utolsó nap).</span><span class="sxs-lookup"><span data-stu-id="d633b-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="d633b-116">Az eredmények szűrhetők, csoportosíthatóak és a csoportösszesítők számíthatóak.</span><span class="sxs-lookup"><span data-stu-id="d633b-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="d633b-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d633b-117">EXAMPLES</span></span>

### <span data-ttu-id="d633b-118">1. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét</span><span class="sxs-lookup"><span data-stu-id="d633b-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="d633b-119">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d633b-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="d633b-120">2. példa: Házirendesemények lekérte a megadott előfizetési hatókört</span><span class="sxs-lookup"><span data-stu-id="d633b-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="d633b-121">Házirendesemény-rekordokat hoz létre az utolsó napon a megadott előfizetésben található összes erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d633b-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="d633b-122">3. példa: Házirendesemények levezetése a felügyeleti csoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="d633b-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="d633b-123">A megadott felügyeleti csoport összes erőforrása számára az utolsó napon létrehozott házirend-eseményrekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="d633b-124">4. példa: Házirendesemények lekértése az aktuális előfizetés erőforráscsoport-hatókörében</span><span class="sxs-lookup"><span data-stu-id="d633b-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d633b-125">A megadott erőforráscsoport összes erőforrásához (az aktuális munkamenet kontextusában az előfizetéshez) az utolsó napon létrehozott házirend-eseményrekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d633b-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="d633b-126">5. példa: Házirendesemények lekértése az erőforráscsoport hatókörében a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d633b-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d633b-127">A megadott erőforráscsoport összes erőforrásához (a megadott előfizetésben) az utolsó napon létrehozott házirend-eseményrekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="d633b-128">6. példa: Házirendesemények lekérte egy erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="d633b-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="d633b-129">A megadott erőforrás utolsó napján létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="d633b-130">7. példa: Házirend-definíció házirendesemények lekértése az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d633b-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d633b-131">A megadott házirendkészlet-definíció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d633b-132">8. példa: Házirend-definíció házirendesemények lekértése a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d633b-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d633b-133">A megadott házirendkészlet-definíció által (a megadott előfizetésben létező) összes erőforráshoz (a bérlő aktuális munkamenet kontextusában) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d633b-134">9. példa: Házirendesemények lekérte egy házirenddefinícióhoz az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d633b-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d633b-135">A megadott házirenddefiníció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d633b-136">10. példa: Házirendesemények lekértése egy házirenddefinícióhoz a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d633b-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d633b-137">A megadott házirenddefiníció által (a megadott előfizetésben létező) összes erőforráshoz (a bérlő aktuális munkamenet kontextusában) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d633b-138">11. példa: Házirend-hozzárendelés házirend-eseményeinek lekértése az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d633b-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d633b-139">A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d633b-140">12. példa: Házirend-események lekérte egy házirend-hozzárendeléshez a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d633b-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d633b-141">A megadott házirend-hozzárendelés által (a megadott előfizetésben létező) összes erőforráshoz (a bérlő aktuális munkamenet kontextusában) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d633b-142">13. példa: Házirend-hozzárendelés házirend-eseményeinek lekérte az aktuális előfizetés megadott erőforráscsoportját</span><span class="sxs-lookup"><span data-stu-id="d633b-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d633b-143">A megadott házirend-hozzárendelés által (az előfizetés aktuális munkamenet kontextusában az erőforráscsoportban megtalálható) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="d633b-144">14. példa: Házirendesemények lekérdezése az aktuális előfizetési hatókörben az OrderBy, a Top és a Select lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="d633b-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="d633b-145">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d633b-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d633b-146">A parancs időbélyeg és házirend-hozzárendelés nevének tulajdonságai alapján rendeli el az eredményeket, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="d633b-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="d633b-147">Azt is kijelöli, hogy az egyes rekordoszlopok csak egy részkészletét sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d633b-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="d633b-148">15. példa: Házirendesemények lekérdezése az aktuális előfizetési hatókörben a From and To lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="d633b-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="d633b-149">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához megadott dátumtartományon belül létrehozott házirendesemény-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="d633b-150">16. példa: Házirendesemények lekérdezése az aktuális előfizetési hatókörben, a Lekérdezésszűrés lehetőséggel</span><span class="sxs-lookup"><span data-stu-id="d633b-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="d633b-151">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d633b-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="d633b-152">A parancs korlátozza a szűrés által visszaadott eredményeket a házirenddefiníciós művelet (beleértve az elutasítási vagy naplózási műveleteket) és az erőforrás helye alapján (a keletus helyet nem foglalja magában).</span><span class="sxs-lookup"><span data-stu-id="d633b-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="d633b-153">17. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét, és sorszám összesítésének alkalmazása</span><span class="sxs-lookup"><span data-stu-id="d633b-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="d633b-154">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordok számát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d633b-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="d633b-155">A parancs csak a házirend eseményrekordjainak számát adja vissza, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="d633b-156">18. példa: Házirendesemények lekértése az aktuális előfizetési hatókörben, csoportosítás alkalmazása összesítéssel</span><span class="sxs-lookup"><span data-stu-id="d633b-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="d633b-157">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d633b-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d633b-158">A parancs korlátozza a házirenddefiníciós művelet alapján végzett szűrés által visszaadott eredményeket (csak naplózási és elutasítási eseményeket tartalmaz).</span><span class="sxs-lookup"><span data-stu-id="d633b-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="d633b-159">Az eredményeket a házirend-hozzárendelés, a házirend-definíció, a házirenddefiníciós művelet és az erőforrás-azonosító alapján csoportosítja, és kiszámítja az egyes csoportok rekordjainak számát, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="d633b-160">Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="d633b-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="d633b-161">19. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét, és csoportosítás alkalmazása összesítés nélkül</span><span class="sxs-lookup"><span data-stu-id="d633b-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="d633b-162">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d633b-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d633b-163">A parancs korlátozza a házirenddefiníciós művelet alapján végzett szűrés által visszaadott eredményeket (csak naplózási és elutasítási eseményeket tartalmaz).</span><span class="sxs-lookup"><span data-stu-id="d633b-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="d633b-164">Az eredményeket az erőforrás-azonosító alapján csoportosulja. Ez a szolgáltatás létrehozza az előfizetés azon erőforrásainak listáját, amelyek legalább egy naplózási vagy elutasítási házirendhez létrehoznak egy házirendeseményt.</span><span class="sxs-lookup"><span data-stu-id="d633b-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="d633b-165">20. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét, és az Alkalmaz beállítással több csoportosítást adott meg</span><span class="sxs-lookup"><span data-stu-id="d633b-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="d633b-166">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d633b-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d633b-167">A parancs korlátozza a szűrés által visszaadott eredményeket a házirend-definíciós művelet alapján (csak elutasítási eseményeket tartalmaz).</span><span class="sxs-lookup"><span data-stu-id="d633b-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="d633b-168">Az eredményeket először a házirend-hozzárendelés, a házirend-definíció és az erőforrás-azonosító alapján csoportosulja. Ezután a csoportosítás eredményét az erőforrás-azonosító kivételével ugyanazokkal a tulajdonságokkal csoportosítja, és kiszámítja az egyes csoportok rekordjainak számát, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d633b-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="d633b-169">Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="d633b-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="d633b-170">Ez a legfelső 5 elutasító házirendet hozza létre, amelyekben a legtöbb elutasított erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="d633b-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="d633b-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d633b-171">PARAMETERS</span></span>

### <span data-ttu-id="d633b-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="d633b-172">-Apply</span></span>
<span data-ttu-id="d633b-173">Kifejezés alkalmazása aggregációkhoz OData-notation használatával.</span><span class="sxs-lookup"><span data-stu-id="d633b-173">Apply expression for aggregations using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d633b-174">-DefaultProfile</span></span>
<span data-ttu-id="d633b-175">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d633b-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d633b-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="d633b-176">-Filter</span></span>
<span data-ttu-id="d633b-177">Filter expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="d633b-177">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-178">-From</span><span class="sxs-lookup"><span data-stu-id="d633b-178">-From</span></span>
<span data-ttu-id="d633b-179">ISO 8601 formázott időbélyeg, amely a lekérdezési időköz kezdő idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d633b-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="d633b-180">Ha nincs megadva, az alapértelmezett érték a "To" paraméter értéke mínusz 1 nap.</span><span class="sxs-lookup"><span data-stu-id="d633b-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d633b-181">-ManagementGroupName</span></span>
<span data-ttu-id="d633b-182">Felügyeleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d633b-182">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d633b-183">-OrderBy</span></span>
<span data-ttu-id="d633b-184">Ordering expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="d633b-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="d633b-185">Egy vagy több vesszővel elválasztott oszlopnév opcionális "desc" (alapértelmezett) vagy "asc" értékekkel.</span><span class="sxs-lookup"><span data-stu-id="d633b-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d633b-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="d633b-187">Házirend-hozzárendelés neve.</span><span class="sxs-lookup"><span data-stu-id="d633b-187">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d633b-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="d633b-189">Házirenddefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="d633b-189">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d633b-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="d633b-191">Házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="d633b-191">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d633b-192">-ResourceGroupName</span></span>
<span data-ttu-id="d633b-193">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d633b-193">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d633b-194">-ResourceId</span></span>
<span data-ttu-id="d633b-195">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d633b-195">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-196">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="d633b-196">-Select</span></span>
<span data-ttu-id="d633b-197">Select expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="d633b-197">Select expression using OData notation.</span></span>
<span data-ttu-id="d633b-198">Egy vagy több vesszővel elválasztott oszlopnév.</span><span class="sxs-lookup"><span data-stu-id="d633b-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="d633b-199">Az egyes rekordokat csak a kért oszlopokra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="d633b-199">Limits the columns on each record to just those requested.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d633b-200">-SubscriptionId</span></span>
<span data-ttu-id="d633b-201">Előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d633b-201">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-202">-To</span><span class="sxs-lookup"><span data-stu-id="d633b-202">-To</span></span>
<span data-ttu-id="d633b-203">ISO 8601 formázott időbélyeg, amely megadja a lekérdezési időköz záró idejét.</span><span class="sxs-lookup"><span data-stu-id="d633b-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="d633b-204">Ha nincs megadva, a kérések alapértelmezett ideje.</span><span class="sxs-lookup"><span data-stu-id="d633b-204">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-205">-Top</span><span class="sxs-lookup"><span data-stu-id="d633b-205">-Top</span></span>
<span data-ttu-id="d633b-206">A vissza nem térhet rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="d633b-206">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d633b-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d633b-207">CommonParameters</span></span>
<span data-ttu-id="d633b-208">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d633b-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d633b-209">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d633b-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d633b-210">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d633b-210">INPUTS</span></span>

### <span data-ttu-id="d633b-211">System.String</span><span class="sxs-lookup"><span data-stu-id="d633b-211">System.String</span></span>

## <span data-ttu-id="d633b-212">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d633b-212">OUTPUTS</span></span>

### <span data-ttu-id="d633b-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d633b-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="d633b-214">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d633b-214">NOTES</span></span>

## <span data-ttu-id="d633b-215">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d633b-215">RELATED LINKS</span></span>
