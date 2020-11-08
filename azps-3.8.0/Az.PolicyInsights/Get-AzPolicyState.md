---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012979"
---
# <span data-ttu-id="d4f06-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="d4f06-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="d4f06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4f06-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f06-103">Házirend-megfelelőségi állapotokat kap az erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="d4f06-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="d4f06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4f06-104">SYNTAX</span></span>

### <span data-ttu-id="d4f06-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4f06-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f06-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="d4f06-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f06-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="d4f06-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f06-108">ResourceScope paraméternél</span><span class="sxs-lookup"><span data-stu-id="d4f06-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f06-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="d4f06-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f06-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="d4f06-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f06-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="d4f06-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f06-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="d4f06-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4f06-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4f06-113">DESCRIPTION</span></span>
<span data-ttu-id="d4f06-114">Házirend-megfelelőségi állapotokat kap az erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="d4f06-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="d4f06-115">A házirend-állam rekordjait több hatókörben is lekérdezheti.</span><span class="sxs-lookup"><span data-stu-id="d4f06-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="d4f06-116">A megadott időintervallumon (alapértelmezett esetben az utolsó napon) alapulva lekérdezheti, hogy a legutóbbi házirendek vagy az összes házirend-állam áttűnése elérhető-e.</span><span class="sxs-lookup"><span data-stu-id="d4f06-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="d4f06-117">Az eredmények szűréssel, csoportosítással és csoportosítási lehetőségekkel is kiszámíthatók.</span><span class="sxs-lookup"><span data-stu-id="d4f06-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="d4f06-118">Példák</span><span class="sxs-lookup"><span data-stu-id="d4f06-118">EXAMPLES</span></span>

### <span data-ttu-id="d4f06-119">Példa 1: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba</span><span class="sxs-lookup"><span data-stu-id="d4f06-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="d4f06-120">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="d4f06-121">2. példa: a legutóbbi házirend-állapot beszerzése a megadott előfizetési tartományba</span><span class="sxs-lookup"><span data-stu-id="d4f06-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="d4f06-122">A megadott előfizetésben lévő összes erőforrás utolsó napján generált legutóbb létrehozott házirend-nyilvántartási rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="d4f06-123">3. példa: az összes házirend-állapot beolvasása a jelenlegi előfizetési tartományba</span><span class="sxs-lookup"><span data-stu-id="d4f06-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="d4f06-124">Az előfizetésben a jelenlegi munkamenet-környezetben az összes erőforrás utolsó napján generált összes korábbi házirend-rekord (a legújabbat is tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="d4f06-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="d4f06-125">Példa 4: a legújabb házirendek beszerzése a felügyeleti csoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="d4f06-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="d4f06-126">Az utolsó napon az adott kezelési csoportban található összes erőforrás esetében generálta a legutóbb létrehozott házirend-nyilvántartást.</span><span class="sxs-lookup"><span data-stu-id="d4f06-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="d4f06-127">5. példa: a legutóbbi házirend-állapot beolvasása az erőforráscsoport hatókörében a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d4f06-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d4f06-128">A megadott erőforráscsoport összes erőforrását (az előfizetést az aktuális munkamenet kontextusában) az utolsó napon generált házirend-nyilvántartási rekordok utolsó napján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d4f06-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="d4f06-129">Példa 6: a legújabb házirendek beszerzése az erőforráscsoport hatókörében a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d4f06-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d4f06-130">A megadott erőforráscsoport összes erőforrásának utolsó napján generált legutóbb létrehozott házirend-nyilvántartási rekordok (a megadott előfizetésben).</span><span class="sxs-lookup"><span data-stu-id="d4f06-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="d4f06-131">7. példa: a legutóbbi házirend-állapot beszerzése egy erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="d4f06-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="d4f06-132">A megadott erőforrás utolsó napján generált naplórend-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="d4f06-133">8. példa: a legutóbbi előfizetésben beállított házirend-definíciós szabályok beszerzése</span><span class="sxs-lookup"><span data-stu-id="d4f06-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d4f06-134">Az utolsó napon az összes erőforrás (a bérlő a jelenlegi munkamenet-környezetében) által generált legújabb házirend-nyilvántartási rekordokat kapja meg (amely az előfizetésben a jelenlegi munkamenet-környezetben létezik).</span><span class="sxs-lookup"><span data-stu-id="d4f06-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d4f06-135">Példa 9: a legújabb házirendek beszerzése egy házirend-készlet definíciója a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d4f06-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d4f06-136">Az utolsó napon az utolsó napon generált házirend-nyilvántartási rekordokat kapja meg (a megadott előfizetésben megtalálható a bérlői környezeten belül).</span><span class="sxs-lookup"><span data-stu-id="d4f06-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d4f06-137">10. példa: a legutóbbi előfizetéshez tartozó házirend-definíció beszerzése a legutóbbi házirendek szerint</span><span class="sxs-lookup"><span data-stu-id="d4f06-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d4f06-138">Az utolsó napon az utolsó napon létrehozott házirend-nyilvántartási rekordok (az aktuális munkamenetben a bérlői környezetben) által megadott házirend-definícióval</span><span class="sxs-lookup"><span data-stu-id="d4f06-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d4f06-139">Példa: a legutóbbi házirendek beszerzése házirend-definícióra a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="d4f06-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d4f06-140">Az utolsó napon az utolsó napon generált házirend-nyilvántartási rekordokat kapja meg (a megadott előfizetésben megtalálható) a megadott házirend-definícióval (amely a megadott előfizetésben létezik).</span><span class="sxs-lookup"><span data-stu-id="d4f06-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d4f06-141">12. példa: a legutóbbi előfizetésben lévő házirend-hozzárendelés legutóbbi házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d4f06-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d4f06-142">Az utolsó napon az utolsó napon létrehozott házirend-nyilvántartási rekordok (az aktuális munkamenetben az előfizetésben megtalálható) által megvalósított összes erőforrás (az aktuális munkamenet-környezetben)</span><span class="sxs-lookup"><span data-stu-id="d4f06-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d4f06-143">Példa: a legutóbbi házirendek beszerzése a megadott előfizetéshez tartozó házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="d4f06-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d4f06-144">Az utolsó napon az utolsó napon generált házirend-nyilvántartási rekordokat kapja meg (a megadott előfizetésben megtalálható a bérlői környezeten belül).</span><span class="sxs-lookup"><span data-stu-id="d4f06-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d4f06-145">14. példa: a legutóbbi előfizetéshez tartozó erőforráscsoport házirend-hozzárendeléséhez szükséges legutóbbi házirendek beszerzése</span><span class="sxs-lookup"><span data-stu-id="d4f06-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d4f06-146">Az utolsó napon az összes erőforrás (az aktuális munkamenetben a bérlői környezetben) által létrehozott, a megadott házirend-hozzárendeléssel (amely az előfizetéshez tartozó erőforrás csoportban található)</span><span class="sxs-lookup"><span data-stu-id="d4f06-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="d4f06-147">15. példa: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba, a OrderBy, a felső és a lekérdezési beállítások megadása</span><span class="sxs-lookup"><span data-stu-id="d4f06-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="d4f06-148">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d4f06-149">A parancs időbélyegző és házirend-hozzárendelési név tulajdonságai szerint rendeli az eredményeket, és az adott sorrendben szereplő adatok közül csak az 5-öt veszi át.</span><span class="sxs-lookup"><span data-stu-id="d4f06-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="d4f06-150">Azt is megadhatja, hogy csak az egyes rekordok oszlopait szeretné megjeleníteni.</span><span class="sxs-lookup"><span data-stu-id="d4f06-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="d4f06-151">16. példa: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba, a lekérdezési és a lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="d4f06-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="d4f06-152">Az előfizetésben szereplő összes erőforráshoz megadott dátumtartomány által az aktuális munkamenet-környezetben létrehozott legújabb házirend-nyilvántartásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="d4f06-153">17. példa: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba, a szűrő lekérdezése beállítással</span><span class="sxs-lookup"><span data-stu-id="d4f06-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="d4f06-154">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="d4f06-155">A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (beleértve a Megtagadás vagy a könyvvizsgálati műveleteket is), a megfelelőségi állapotot (csak a nem megfelelő állapotot tartalmazza) és az erőforrás helyének korlátozásával (kivéve a eastus helyét).</span><span class="sxs-lookup"><span data-stu-id="d4f06-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="d4f06-156">18. példa: a legutóbbi házirend-adatok beszerzése a jelenlegi előfizetési tartományba, a sor számlálási összesítésének megadása</span><span class="sxs-lookup"><span data-stu-id="d4f06-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="d4f06-157">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált legutóbb létrehozott házirend-rekordok számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d4f06-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="d4f06-158">A parancs csak a AdditionalProperties tulajdonságban megadott irányelvmodul-rekordok számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d4f06-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="d4f06-159">19. példa: a legutóbbi házirend-állapot beszerzése a jelenlegi előfizetési tartományba, az összesítéssel történő csoportosítás megadása</span><span class="sxs-lookup"><span data-stu-id="d4f06-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="d4f06-160">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d4f06-161">A parancs a megfelelőségi állapoton alapuló szűréssel visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="d4f06-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="d4f06-162">A házirend-hozzárendelés, a házirend-definíció és a házirend-definíció alapján csoportosítja az eredményeket, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d4f06-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="d4f06-163">Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="d4f06-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="d4f06-164">20. példa: a legutóbbi házirend-állapot beszerzése a jelenlegi előfizetési tartományba, az Összesítés nélküli csoportosítás megadása</span><span class="sxs-lookup"><span data-stu-id="d4f06-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="d4f06-165">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d4f06-166">A parancs a megfelelőségi állapoton alapuló szűréssel visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="d4f06-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="d4f06-167">Az eredmény az erőforrás-azonosító alapján csoportosítja a találatokat. Ezzel létrehozhatja az előfizetéshez tartozó összes erőforrás listáját, amelyek nem felelnek meg legalább egy házirendnek.</span><span class="sxs-lookup"><span data-stu-id="d4f06-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="d4f06-168">21. példa: a legutóbbi házirend-állapot beszerzése a jelenlegi előfizetési tartományba</span><span class="sxs-lookup"><span data-stu-id="d4f06-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="d4f06-169">22. példa: a legutóbbi házirendek beszerzése, valamint az erőforrásokra vonatkozó házirendek kiértékelésének részletei</span><span class="sxs-lookup"><span data-stu-id="d4f06-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="d4f06-170">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d4f06-171">A parancs a megfelelőségi állapoton alapuló szűréssel visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).</span><span class="sxs-lookup"><span data-stu-id="d4f06-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="d4f06-172">Az eredményeket először a házirend-hozzárendelés, a házirend-definíció, a házirend-definíció és az erőforrás-azonosító alapján csoportosítja. Ezután az erőforrás-azonosító kivételével továbbra is csoportosítja a csoportosítás eredményét, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d4f06-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="d4f06-173">Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="d4f06-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="d4f06-174">Ez a felső 5 házirendet hozza létre a nem megfelelő erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="d4f06-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="d4f06-175">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4f06-175">PARAMETERS</span></span>

### <span data-ttu-id="d4f06-176">-All (mind)</span><span class="sxs-lookup"><span data-stu-id="d4f06-176">-All</span></span>
<span data-ttu-id="d4f06-177">A megadott időintervallumon belül csak a legkésőbbi időpontban kapja meg az összes házirendet.</span><span class="sxs-lookup"><span data-stu-id="d4f06-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="d4f06-178">-Apply (alkalmazás)</span><span class="sxs-lookup"><span data-stu-id="d4f06-178">-Apply</span></span>
<span data-ttu-id="d4f06-179">A kifejezés alkalmazása az összesítésekre a OData jelöléssel.</span><span class="sxs-lookup"><span data-stu-id="d4f06-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="d4f06-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f06-180">-DefaultProfile</span></span>
<span data-ttu-id="d4f06-181">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4f06-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f06-182">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="d4f06-182">-Expand</span></span>
<span data-ttu-id="d4f06-183">A kifejezés kibontása OData jelöléssel</span><span class="sxs-lookup"><span data-stu-id="d4f06-183">Expand expression using OData notation.</span></span>

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

### <span data-ttu-id="d4f06-184">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="d4f06-184">-Filter</span></span>
<span data-ttu-id="d4f06-185">A kifejezés szűrése OData jelöléssel</span><span class="sxs-lookup"><span data-stu-id="d4f06-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="d4f06-186">-From</span><span class="sxs-lookup"><span data-stu-id="d4f06-186">-From</span></span>
<span data-ttu-id="d4f06-187">Az ISO 8601 formázott időbélyegző adja meg a lekérdezni kívánt intervallum kezdési időpontját.</span><span class="sxs-lookup"><span data-stu-id="d4f06-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="d4f06-188">Ha nincs megadva, az alapértelmezett érték "to" paraméterérték mínusz 1 nap.</span><span class="sxs-lookup"><span data-stu-id="d4f06-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="d4f06-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f06-189">-ManagementGroupName</span></span>
<span data-ttu-id="d4f06-190">A felügyeleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4f06-190">Management group name.</span></span>

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

### <span data-ttu-id="d4f06-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d4f06-191">-OrderBy</span></span>
<span data-ttu-id="d4f06-192">A kifejezés megrendelése OData jelöléssel</span><span class="sxs-lookup"><span data-stu-id="d4f06-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="d4f06-193">Egy vagy több vesszővel elválasztott oszlop neve, amely nem kötelező "desc" (alapértelmezett) vagy "ASC".</span><span class="sxs-lookup"><span data-stu-id="d4f06-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="d4f06-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d4f06-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="d4f06-195">Házirend-hozzárendelés neve</span><span class="sxs-lookup"><span data-stu-id="d4f06-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="d4f06-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d4f06-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="d4f06-197">Házirend-definíció neve</span><span class="sxs-lookup"><span data-stu-id="d4f06-197">Policy definition name.</span></span>

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

### <span data-ttu-id="d4f06-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d4f06-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="d4f06-199">Házirend-definíció neve</span><span class="sxs-lookup"><span data-stu-id="d4f06-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="d4f06-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f06-200">-ResourceGroupName</span></span>
<span data-ttu-id="d4f06-201">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d4f06-201">Resource group name.</span></span>

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

### <span data-ttu-id="d4f06-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4f06-202">-ResourceId</span></span>
<span data-ttu-id="d4f06-203">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d4f06-203">Resource ID.</span></span>

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

### <span data-ttu-id="d4f06-204">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="d4f06-204">-Select</span></span>
<span data-ttu-id="d4f06-205">Jelölje ki a kifejezést a OData jelöléssel.</span><span class="sxs-lookup"><span data-stu-id="d4f06-205">Select expression using OData notation.</span></span>
<span data-ttu-id="d4f06-206">Egy vagy több pontosvesszővel tagolt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="d4f06-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="d4f06-207">Az egyes rekordok oszlopait csak a kért értékekre korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="d4f06-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="d4f06-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4f06-208">-SubscriptionId</span></span>
<span data-ttu-id="d4f06-209">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="d4f06-209">Subscription ID.</span></span>

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

### <span data-ttu-id="d4f06-210">-To</span><span class="sxs-lookup"><span data-stu-id="d4f06-210">-To</span></span>
<span data-ttu-id="d4f06-211">ISO 8601 formázott időbélyegző a lekérdezési intervallum befejezési időpontjának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d4f06-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="d4f06-212">Ha nincs megadva, az alapértelmezett beállítás a kérés időpontjában.</span><span class="sxs-lookup"><span data-stu-id="d4f06-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="d4f06-213">-Top</span><span class="sxs-lookup"><span data-stu-id="d4f06-213">-Top</span></span>
<span data-ttu-id="d4f06-214">A visszaadni kívánt rekordok maximális száma</span><span class="sxs-lookup"><span data-stu-id="d4f06-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="d4f06-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f06-215">CommonParameters</span></span>
<span data-ttu-id="d4f06-216">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4f06-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f06-217">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4f06-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f06-218">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4f06-218">INPUTS</span></span>

### <span data-ttu-id="d4f06-219">System. String</span><span class="sxs-lookup"><span data-stu-id="d4f06-219">System.String</span></span>

## <span data-ttu-id="d4f06-220">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4f06-220">OUTPUTS</span></span>

### <span data-ttu-id="d4f06-221">Microsoft. Azure. Command. PolicyInsights. models. PolicyState</span><span class="sxs-lookup"><span data-stu-id="d4f06-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="d4f06-222">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4f06-222">NOTES</span></span>

## <span data-ttu-id="d4f06-223">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4f06-223">RELATED LINKS</span></span>

[<span data-ttu-id="d4f06-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="d4f06-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
