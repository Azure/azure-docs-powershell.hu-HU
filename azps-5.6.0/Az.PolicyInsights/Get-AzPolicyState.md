---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937498"
---
# <span data-ttu-id="80a1a-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="80a1a-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="80a1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="80a1a-103">Házirend-megfelelőségi államokat biztosít az erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="80a1a-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="80a1a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80a1a-104">SYNTAX</span></span>

### <span data-ttu-id="80a1a-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80a1a-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a1a-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="80a1a-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a1a-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="80a1a-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a1a-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="80a1a-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a1a-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="80a1a-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a1a-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="80a1a-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a1a-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="80a1a-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a1a-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="80a1a-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80a1a-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80a1a-113">DESCRIPTION</span></span>
<span data-ttu-id="80a1a-114">Házirend-megfelelőségi államokat biztosít az erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="80a1a-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="80a1a-115">A házirendállapot-rekordok lekérdezhetők különböző hatókörökben.</span><span class="sxs-lookup"><span data-stu-id="80a1a-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="80a1a-116">A megadott időintervallum alapján (alapértelmezés szerint az utolsó nap) lekérdezhető a legújabb házirendállapotok vagy az összes házirendállapot-áttűnés.</span><span class="sxs-lookup"><span data-stu-id="80a1a-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="80a1a-117">Az eredmények szűrhetők, csoportosíthatóak és a csoportösszesítők számíthatóak.</span><span class="sxs-lookup"><span data-stu-id="80a1a-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="80a1a-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80a1a-118">EXAMPLES</span></span>

### <span data-ttu-id="80a1a-119">1. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét</span><span class="sxs-lookup"><span data-stu-id="80a1a-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="80a1a-120">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="80a1a-121">2. példa: A legújabb házirend-államok lekérte a megadott előfizetési hatókört</span><span class="sxs-lookup"><span data-stu-id="80a1a-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="80a1a-122">A megadott előfizetés összes erőforrásához az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="80a1a-123">3. példa: Az előfizetés aktuális hatókörében lévő házirend-állapotok lekérte</span><span class="sxs-lookup"><span data-stu-id="80a1a-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="80a1a-124">Beveszi az összes előzmény házirendállapot-rekordot (beleértve a legutóbbi rekordokat is), amelyek az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="80a1a-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="80a1a-125">4. példa: A legújabb házirend-államok lekérte a felügyeleti csoportok hatókörét</span><span class="sxs-lookup"><span data-stu-id="80a1a-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="80a1a-126">A megadott felügyeleti csoporton belüli összes erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="80a1a-127">5. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés erőforráscsoport-hatókörét</span><span class="sxs-lookup"><span data-stu-id="80a1a-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="80a1a-128">A megadott erőforráscsoport összes erőforrásához (az aktuális munkamenet kontextusában az előfizetésben) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="80a1a-129">6. példa: A legújabb házirend-államok lekérte az erőforráscsoport hatókörét a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="80a1a-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="80a1a-130">A megadott erőforráscsoport összes erőforrásához (a megadott előfizetésben) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="80a1a-131">7. példa: Erőforrás legújabb házirend- states-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="80a1a-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="80a1a-132">A megadott erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="80a1a-133">8. példa: Házirendkészlet-definíció legújabb házirend-állapotának lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="80a1a-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="80a1a-134">A megadott házirendkészlet-definíció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="80a1a-135">9. példa: Házirendkészlet-definíció legújabb házirend-államok lekérte a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="80a1a-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="80a1a-136">A megadott házirendkészlet-definíció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza (a bérlői webhelyen az aktuális munkamenet kontextusában).</span><span class="sxs-lookup"><span data-stu-id="80a1a-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="80a1a-137">10. példa: Házirenddefiníció legújabb állapotának lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="80a1a-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="80a1a-138">A megadott házirenddefiníció által (az aktuális munkamenet kontextusában az előfizetésben megtalálható) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="80a1a-139">11. példa: Házirenddefiníció legújabb házirend-államának lekérte a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="80a1a-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="80a1a-140">A megadott házirenddefiníció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza (a bérlői webhelyen az aktuális munkamenet kontextusában).</span><span class="sxs-lookup"><span data-stu-id="80a1a-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="80a1a-141">12. példa: Házirend-hozzárendelés legújabb házirend-állapotának lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="80a1a-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="80a1a-142">A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetésben létezik) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="80a1a-143">13. példa: Házirend-hozzárendelés legújabb házirend-kiosztási államának lekérte a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="80a1a-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="80a1a-144">A megadott (a megadott előfizetésben létező) házirend-hozzárendelés által az utolsó napon létrehozott összes erőforrásra vonatkozóan (a bérlő aktuális munkamenet kontextusában) létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="80a1a-145">14. példa: Házirend-hozzárendelés legújabb házirend-állapotának lekérte az aktuális előfizetés megadott erőforráscsoportját</span><span class="sxs-lookup"><span data-stu-id="80a1a-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="80a1a-146">A megadott házirend-hozzárendelés által (az előfizetés aktuális munkamenet kontextusában az erőforráscsoportban található) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="80a1a-147">15. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetési hatókört az OrderBy, a Top és a Select lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="80a1a-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="80a1a-148">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="80a1a-149">A parancs időbélyeg és házirend-hozzárendelés nevének tulajdonságai alapján rendeli el az eredményeket, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="80a1a-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="80a1a-150">Azt is kijelöli, hogy az egyes rekordoszlopok csak egy részkészletét sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="80a1a-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="80a1a-151">16. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét, a From and To lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="80a1a-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="80a1a-152">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához megadott dátumtartományon belül létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="80a1a-153">17. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét a Szűrés lekérdezési beállítással</span><span class="sxs-lookup"><span data-stu-id="80a1a-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="80a1a-154">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="80a1a-155">A parancs korlátozza a szűrés által visszaadott eredményeket a házirend-definíciós művelet (beleértve az elutasítási vagy naplózási műveleteket), a megfelelőségi állapotot (csak a nem megfelelő állapotot is beleértve) és az erőforrás helyére (a kelet-európai régiót nem foglalja magában).</span><span class="sxs-lookup"><span data-stu-id="80a1a-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="80a1a-156">18. példa: A legújabb házirendállapotok lekértése az aktuális előfizetés hatókörében a sorszám összesítésének alkalmazásával</span><span class="sxs-lookup"><span data-stu-id="80a1a-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="80a1a-157">Az aktuális munkamenet kontextusában az előfizetésben lévő összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordok számát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="80a1a-158">A parancs csak a házirendállapot-rekordok számát adja vissza, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="80a1a-159">19. példa: A legújabb házirendállapotok lekértése az aktuális előfizetési hatókörben a Csoportosítás alkalmazása aggregációval beállítással</span><span class="sxs-lookup"><span data-stu-id="80a1a-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="80a1a-160">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="80a1a-161">A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="80a1a-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="80a1a-162">Az eredményeket a házirend-hozzárendelés, a házirendkészlet-definíció és a házirend-definíció alapján csoportosítja, és az egyes csoportok rekordjainak számát számítja ki, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="80a1a-163">Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="80a1a-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="80a1a-164">20. példa: A legújabb házirendállapotok lekértése az aktuális előfizetési hatókörben a Csoportosítás alkalmazása összesítés nélkül beállítással</span><span class="sxs-lookup"><span data-stu-id="80a1a-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="80a1a-165">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="80a1a-166">A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="80a1a-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="80a1a-167">Az eredményeket az erőforrás-azonosító alapján csoportosulja. Ez a szolgáltatás létrehozza az előfizetés azon erőforrásainak listáját, amelyek nem kompatibilisek legalább egy házirendnek.</span><span class="sxs-lookup"><span data-stu-id="80a1a-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="80a1a-168">21. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét, és több csoportosítást is megadhat</span><span class="sxs-lookup"><span data-stu-id="80a1a-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="80a1a-169">22. példa: A legújabb házirend-államok, beleértve az erőforrások házirend-kiértékelési részleteit</span><span class="sxs-lookup"><span data-stu-id="80a1a-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="80a1a-170">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="80a1a-171">A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="80a1a-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="80a1a-172">Először a házirend-hozzárendelés, a házirendkészlet-definíció, a házirend-definíció és az erőforrás-azonosító alapján csoportosul az eredmények. Ezután a csoportosítás eredményét az erőforrás-azonosító kivételével ugyanazokkal a tulajdonságokkal csoportosítja, és kiszámítja az egyes csoportok rekordjainak számát, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="80a1a-173">Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="80a1a-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="80a1a-174">Ez a legfelső 5 házirendet hozza létre, amelyekben a legtöbb nem kompatibilis erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="80a1a-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="80a1a-175">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80a1a-175">PARAMETERS</span></span>

### <span data-ttu-id="80a1a-176">-All</span><span class="sxs-lookup"><span data-stu-id="80a1a-176">-All</span></span>
<span data-ttu-id="80a1a-177">A megadott időintervallumon belül csak a legújabb házirendek helyett az összes házirend-államot be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="80a1a-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a1a-178">-Apply</span><span class="sxs-lookup"><span data-stu-id="80a1a-178">-Apply</span></span>
<span data-ttu-id="80a1a-179">Kifejezés alkalmazása aggregációkhoz OData-notation használatával.</span><span class="sxs-lookup"><span data-stu-id="80a1a-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="80a1a-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a1a-180">-DefaultProfile</span></span>
<span data-ttu-id="80a1a-181">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80a1a-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a1a-182">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="80a1a-182">-Expand</span></span>
<span data-ttu-id="80a1a-183">Kifejezés kibontása OData-notation használatával</span><span class="sxs-lookup"><span data-stu-id="80a1a-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a1a-184">-Filter</span><span class="sxs-lookup"><span data-stu-id="80a1a-184">-Filter</span></span>
<span data-ttu-id="80a1a-185">Filter expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="80a1a-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="80a1a-186">-From</span><span class="sxs-lookup"><span data-stu-id="80a1a-186">-From</span></span>
<span data-ttu-id="80a1a-187">ISO 8601 formázott időbélyeg, amely a lekérdezési időköz kezdő idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a1a-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="80a1a-188">Ha nincs megadva, az alapértelmezett érték a "To" paraméter értéke mínusz 1 nap.</span><span class="sxs-lookup"><span data-stu-id="80a1a-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="80a1a-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="80a1a-189">-ManagementGroupName</span></span>
<span data-ttu-id="80a1a-190">Felügyeleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="80a1a-190">Management group name.</span></span>

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

### <span data-ttu-id="80a1a-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="80a1a-191">-OrderBy</span></span>
<span data-ttu-id="80a1a-192">Ordering expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="80a1a-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="80a1a-193">Egy vagy több vesszővel elválasztott oszlopnév opcionális "desc" (alapértelmezett) vagy "asc" értékekkel.</span><span class="sxs-lookup"><span data-stu-id="80a1a-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="80a1a-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="80a1a-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="80a1a-195">Házirend-hozzárendelés neve.</span><span class="sxs-lookup"><span data-stu-id="80a1a-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="80a1a-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="80a1a-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="80a1a-197">Házirenddefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="80a1a-197">Policy definition name.</span></span>

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

### <span data-ttu-id="80a1a-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="80a1a-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="80a1a-199">Házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="80a1a-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="80a1a-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a1a-200">-ResourceGroupName</span></span>
<span data-ttu-id="80a1a-201">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80a1a-201">Resource group name.</span></span>

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

### <span data-ttu-id="80a1a-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a1a-202">-ResourceId</span></span>
<span data-ttu-id="80a1a-203">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="80a1a-203">Resource ID.</span></span>

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

### <span data-ttu-id="80a1a-204">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="80a1a-204">-Select</span></span>
<span data-ttu-id="80a1a-205">Select expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="80a1a-205">Select expression using OData notation.</span></span>
<span data-ttu-id="80a1a-206">Egy vagy több vesszővel elválasztott oszlopnév.</span><span class="sxs-lookup"><span data-stu-id="80a1a-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="80a1a-207">Az egyes rekordokat csak a kért oszlopokra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="80a1a-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="80a1a-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80a1a-208">-SubscriptionId</span></span>
<span data-ttu-id="80a1a-209">Előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="80a1a-209">Subscription ID.</span></span>

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

### <span data-ttu-id="80a1a-210">-To</span><span class="sxs-lookup"><span data-stu-id="80a1a-210">-To</span></span>
<span data-ttu-id="80a1a-211">ISO 8601 formázott időbélyeg, amely megadja a lekérdezési időköz záró idejét.</span><span class="sxs-lookup"><span data-stu-id="80a1a-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="80a1a-212">Ha nincs megadva, a kérések alapértelmezett ideje.</span><span class="sxs-lookup"><span data-stu-id="80a1a-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="80a1a-213">-Top</span><span class="sxs-lookup"><span data-stu-id="80a1a-213">-Top</span></span>
<span data-ttu-id="80a1a-214">A vissza nem térhet rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="80a1a-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="80a1a-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a1a-215">CommonParameters</span></span>
<span data-ttu-id="80a1a-216">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a1a-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a1a-217">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80a1a-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a1a-218">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80a1a-218">INPUTS</span></span>

### <span data-ttu-id="80a1a-219">System.String</span><span class="sxs-lookup"><span data-stu-id="80a1a-219">System.String</span></span>

## <span data-ttu-id="80a1a-220">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80a1a-220">OUTPUTS</span></span>

### <span data-ttu-id="80a1a-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="80a1a-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="80a1a-222">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80a1a-222">NOTES</span></span>

## <span data-ttu-id="80a1a-223">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80a1a-223">RELATED LINKS</span></span>

[<span data-ttu-id="80a1a-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="80a1a-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
