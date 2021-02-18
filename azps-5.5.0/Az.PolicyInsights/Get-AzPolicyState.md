---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206271"
---
# <span data-ttu-id="b9fb3-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b9fb3-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="b9fb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fb3-103">Házirend-megfelelőségi államokat biztosít az erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="b9fb3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9fb3-104">SYNTAX</span></span>

### <span data-ttu-id="b9fb3-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9fb3-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fb3-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="b9fb3-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fb3-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="b9fb3-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fb3-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="b9fb3-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fb3-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="b9fb3-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fb3-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="b9fb3-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fb3-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="b9fb3-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fb3-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="b9fb3-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fb3-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9fb3-113">DESCRIPTION</span></span>
<span data-ttu-id="b9fb3-114">Házirend-megfelelőségi államokat biztosít az erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="b9fb3-115">A házirendállapot-rekordok lekérdezhetők különböző hatókörökben.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="b9fb3-116">A megadott időintervallum alapján (alapértelmezés szerint az utolsó nap) lekérdezhető a legújabb házirendállapotok vagy az összes házirendállapot-áttűnés.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="b9fb3-117">Az eredmények szűrhetők, csoportosíthatóak és csoportos összesítések is kiszámíthatók.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="b9fb3-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9fb3-118">EXAMPLES</span></span>

### <span data-ttu-id="b9fb3-119">1. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét</span><span class="sxs-lookup"><span data-stu-id="b9fb3-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="b9fb3-120">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="b9fb3-121">2. példa: A legújabb házirend-államok lekérte a megadott előfizetési hatókört</span><span class="sxs-lookup"><span data-stu-id="b9fb3-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="b9fb3-122">A megadott előfizetésen belüli összes erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="b9fb3-123">3. példa: Az előfizetés aktuális hatókörében lévő házirend-állapotok lekérte</span><span class="sxs-lookup"><span data-stu-id="b9fb3-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="b9fb3-124">Az aktuális munkamenet kontextusában az előfizetésben lévő összes erőforrásra vonatkozóan az utolsó napon létrehozott összes előzmény-házirendállapot-rekordot (beleértve a legutóbbi rekordokat is) beveszi.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="b9fb3-125">4. példa: A legújabb házirend-államok lekérte a felügyeleti csoportok hatókörét</span><span class="sxs-lookup"><span data-stu-id="b9fb3-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="b9fb3-126">A megadott felügyeleti csoporton belüli összes erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="b9fb3-127">5. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés erőforráscsoport-hatókörét</span><span class="sxs-lookup"><span data-stu-id="b9fb3-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="b9fb3-128">A megadott erőforráscsoport összes erőforrásához (az aktuális munkamenet kontextusában az előfizetésben) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="b9fb3-129">6. példa: A legújabb házirend-államok lekérte az erőforráscsoport hatókörét a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="b9fb3-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="b9fb3-130">A megadott erőforráscsoport összes erőforrásához (a megadott előfizetésben) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="b9fb3-131">7. példa: Erőforrás legújabb házirend- states-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="b9fb3-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="b9fb3-132">A megadott erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="b9fb3-133">8. példa: Házirendkészlet-definíció legújabb házirend-állapotának lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="b9fb3-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="b9fb3-134">A megadott házirendkészlet-definíció által (az aktuális munkamenet kontextusában az előfizetésben megtalálható) összes erőforrásra vonatkozóan (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="b9fb3-135">9. példa: Házirendkészlet-definíció legújabb házirend-államok lekérte a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="b9fb3-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="b9fb3-136">A megadott házirendkészlet-definíció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza (a bérlői webhelyen az aktuális munkamenet kontextusában).</span><span class="sxs-lookup"><span data-stu-id="b9fb3-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="b9fb3-137">10. példa: Házirenddefiníció legújabb házirend-állapotának lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="b9fb3-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="b9fb3-138">A megadott házirenddefiníció által (az aktuális munkamenet kontextusában az előfizetésben megtalálható) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="b9fb3-139">11. példa: Házirenddefiníció legújabb házirend-államának lekérte a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="b9fb3-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="b9fb3-140">A megadott házirenddefiníció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza (a bérlői webhelyen az aktuális munkamenet kontextusában).</span><span class="sxs-lookup"><span data-stu-id="b9fb3-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="b9fb3-141">12. példa: Házirend-hozzárendelés legújabb házirend-állapotának lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="b9fb3-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="b9fb3-142">A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetésben létezik) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="b9fb3-143">13. példa: Házirend-hozzárendelés legújabb házirend-kiosztási államának lekérte a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="b9fb3-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="b9fb3-144">A megadott (a megadott előfizetésben létező) házirend-hozzárendelés által az utolsó napon létrehozott összes erőforrásra vonatkozóan (a bérlő aktuális munkamenet kontextusában) létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="b9fb3-145">14. példa: Házirend-hozzárendelés legújabb házirend-állapotának lekérte az aktuális előfizetés megadott erőforráscsoportját</span><span class="sxs-lookup"><span data-stu-id="b9fb3-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="b9fb3-146">A megadott házirend-hozzárendelés által (az előfizetés aktuális munkamenet kontextusában az erőforráscsoportban található) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="b9fb3-147">15. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetési hatókört az OrderBy, a Top és a Select lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="b9fb3-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="b9fb3-148">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="b9fb3-149">A parancs időbélyeg és házirend-hozzárendelés nevének tulajdonságai alapján rendeli el az eredményeket, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="b9fb3-150">Azt is kijelöli, hogy az egyes rekordoszlopok csak egy részkészletét sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="b9fb3-151">16. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét, a From and To lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="b9fb3-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="b9fb3-152">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához megadott dátumtartományon belül létrehozott legújabb házirendállapot-rekordokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="b9fb3-153">17. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét a Szűrés lekérdezési beállítással</span><span class="sxs-lookup"><span data-stu-id="b9fb3-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="b9fb3-154">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="b9fb3-155">A parancs korlátozza a szűrés által visszaadott eredményeket a házirenddefiníciós művelet (beleértve az elutasítási vagy naplózási műveleteket), a megfelelőségi állapot (csak a nem megfelelő állapotot is beleértve) és az erőforrás helye alapján (a kelettől függetlenül).</span><span class="sxs-lookup"><span data-stu-id="b9fb3-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="b9fb3-156">18. példa: A legújabb házirendállapotok lekértése az aktuális előfizetés hatókörében a sorszám összesítésének alkalmazásával</span><span class="sxs-lookup"><span data-stu-id="b9fb3-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="b9fb3-157">Az aktuális munkamenet kontextusában az előfizetésben lévő összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordok számát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="b9fb3-158">A parancs csak a házirendállapot-rekordok számát adja vissza, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="b9fb3-159">19. példa: A legújabb házirendállapotok lekértése az aktuális előfizetési hatókörben a Csoportosítás alkalmazása aggregációval beállítással</span><span class="sxs-lookup"><span data-stu-id="b9fb3-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="b9fb3-160">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="b9fb3-161">A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="b9fb3-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="b9fb3-162">Az eredményeket a házirend-hozzárendelés, a házirendkészlet-definíció és a házirend-definíció alapján csoportosítja, és az egyes csoportok rekordjainak számát számítja ki, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="b9fb3-163">Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="b9fb3-164">20. példa: A legújabb házirendállapotok lekértése az aktuális előfizetési hatókörben a Csoportosítás alkalmazása összesítés nélkül beállítással</span><span class="sxs-lookup"><span data-stu-id="b9fb3-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="b9fb3-165">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="b9fb3-166">A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="b9fb3-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="b9fb3-167">Az eredményeket az erőforrás-azonosító alapján csoportosulja. Ez a szolgáltatás létrehozza az előfizetés azon erőforrásainak listáját, amelyek nem kompatibilisek legalább egy házirendnek.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="b9fb3-168">21. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét, és több csoportosítást is megadhat az Alkalmazás beállítással</span><span class="sxs-lookup"><span data-stu-id="b9fb3-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="b9fb3-169">22. példa: Az erőforrás legújabb házirend-ének megtekintése, beleértve a házirendek kiértékelési részleteit</span><span class="sxs-lookup"><span data-stu-id="b9fb3-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="b9fb3-170">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="b9fb3-171">A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="b9fb3-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="b9fb3-172">Az eredményeket először a házirend-hozzárendelés, a házirend-definíció, a házirend-definíció és az erőforrás-azonosító alapján csoportosulja. Ezután a csoportosítás eredményét az erőforrás-azonosító kivételével ugyanazokkal a tulajdonságokkal csoportosítja, és kiszámítja az egyes csoportok rekordjainak számát, amelyet az AdditionalProperties tulajdonságban ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="b9fb3-173">Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="b9fb3-174">Ez a legfelső 5 házirendet hozza létre, amelyekben a legtöbb nem kompatibilis erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="b9fb3-175">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9fb3-175">PARAMETERS</span></span>

### <span data-ttu-id="b9fb3-176">-All</span><span class="sxs-lookup"><span data-stu-id="b9fb3-176">-All</span></span>
<span data-ttu-id="b9fb3-177">A megadott időintervallumon belül csak a legújabb házirendek helyett az összes házirend-államot be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="b9fb3-178">-Apply</span><span class="sxs-lookup"><span data-stu-id="b9fb3-178">-Apply</span></span>
<span data-ttu-id="b9fb3-179">Kifejezés alkalmazása aggregációkhoz OData-notation használatával.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="b9fb3-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fb3-180">-DefaultProfile</span></span>
<span data-ttu-id="b9fb3-181">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9fb3-182">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="b9fb3-182">-Expand</span></span>
<span data-ttu-id="b9fb3-183">Kifejezés kibontása OData-notation használatával</span><span class="sxs-lookup"><span data-stu-id="b9fb3-183">Expand expression using OData notation.</span></span>

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

### <span data-ttu-id="b9fb3-184">-Filter</span><span class="sxs-lookup"><span data-stu-id="b9fb3-184">-Filter</span></span>
<span data-ttu-id="b9fb3-185">Kifejezésszűrés OData-ként</span><span class="sxs-lookup"><span data-stu-id="b9fb3-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="b9fb3-186">-From</span><span class="sxs-lookup"><span data-stu-id="b9fb3-186">-From</span></span>
<span data-ttu-id="b9fb3-187">ISO 8601 formázott időbélyeg, amely megadja a lekérdezési időköz kezdő idejét.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="b9fb3-188">Ha nincs megadva, az alapértelmezett érték a "To" paraméter értéke mínusz 1 nap.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="b9fb3-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fb3-189">-ManagementGroupName</span></span>
<span data-ttu-id="b9fb3-190">Felügyeleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-190">Management group name.</span></span>

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

### <span data-ttu-id="b9fb3-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b9fb3-191">-OrderBy</span></span>
<span data-ttu-id="b9fb3-192">Ordering expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="b9fb3-193">Egy vagy több vesszővel elválasztott oszlopnév opcionális "desc" (alapértelmezett) vagy "asc" értékekkel.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="b9fb3-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b9fb3-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="b9fb3-195">Házirend-hozzárendelés neve.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="b9fb3-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b9fb3-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="b9fb3-197">Házirenddefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-197">Policy definition name.</span></span>

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

### <span data-ttu-id="b9fb3-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b9fb3-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="b9fb3-199">Házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="b9fb3-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fb3-200">-ResourceGroupName</span></span>
<span data-ttu-id="b9fb3-201">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-201">Resource group name.</span></span>

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

### <span data-ttu-id="b9fb3-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9fb3-202">-ResourceId</span></span>
<span data-ttu-id="b9fb3-203">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-203">Resource ID.</span></span>

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

### <span data-ttu-id="b9fb3-204">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="b9fb3-204">-Select</span></span>
<span data-ttu-id="b9fb3-205">Select expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-205">Select expression using OData notation.</span></span>
<span data-ttu-id="b9fb3-206">Egy vagy több vesszővel elválasztott oszlopnév.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="b9fb3-207">Az egyes rekordokat csak a kért oszlopokra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="b9fb3-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9fb3-208">-SubscriptionId</span></span>
<span data-ttu-id="b9fb3-209">Előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-209">Subscription ID.</span></span>

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

### <span data-ttu-id="b9fb3-210">-To</span><span class="sxs-lookup"><span data-stu-id="b9fb3-210">-To</span></span>
<span data-ttu-id="b9fb3-211">ISO 8601 formázott időbélyeg, amely megadja a lekérdezési időköz záró idejét.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="b9fb3-212">Ha nincs megadva, a kérések alapértelmezett ideje.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="b9fb3-213">-Top</span><span class="sxs-lookup"><span data-stu-id="b9fb3-213">-Top</span></span>
<span data-ttu-id="b9fb3-214">A vissza nem térhet rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="b9fb3-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fb3-215">CommonParameters</span></span>
<span data-ttu-id="b9fb3-216">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fb3-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fb3-217">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9fb3-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fb3-218">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9fb3-218">INPUTS</span></span>

### <span data-ttu-id="b9fb3-219">System.String</span><span class="sxs-lookup"><span data-stu-id="b9fb3-219">System.String</span></span>

## <span data-ttu-id="b9fb3-220">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9fb3-220">OUTPUTS</span></span>

### <span data-ttu-id="b9fb3-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="b9fb3-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="b9fb3-222">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9fb3-222">NOTES</span></span>

## <span data-ttu-id="b9fb3-223">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9fb3-223">RELATED LINKS</span></span>

[<span data-ttu-id="b9fb3-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="b9fb3-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
