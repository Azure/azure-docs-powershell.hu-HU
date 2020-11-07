---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 1a0b2a4c66dba962518b9bb5ebca565f4bcd41bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838402"
---
# <span data-ttu-id="9b816-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="9b816-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="9b816-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b816-102">SYNOPSIS</span></span>
<span data-ttu-id="9b816-103">Az erőforrások létrehozásakor vagy frissítésekor létrehozott házirend-értékelő eseményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="9b816-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b816-104">SYNTAX</span></span>

### <span data-ttu-id="9b816-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b816-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b816-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="9b816-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b816-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="9b816-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b816-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="9b816-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b816-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="9b816-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b816-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="9b816-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b816-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="9b816-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b816-112">ResourceScope paraméternél</span><span class="sxs-lookup"><span data-stu-id="9b816-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b816-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b816-113">DESCRIPTION</span></span>
<span data-ttu-id="9b816-114">Az erőforrások létrehozásakor vagy frissítésekor létrehozott házirend-értékelő eseményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="9b816-115">A házirend-esemény rekordjait különböző hatókörökben lehet lekérdezni a megadott időintervallumok (az alapértelmezett utolsó nap) alapján.</span><span class="sxs-lookup"><span data-stu-id="9b816-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="9b816-116">Az eredmények szűréssel, csoportosítással és csoportosítási lehetőségekkel is kiszámíthatók.</span><span class="sxs-lookup"><span data-stu-id="9b816-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="9b816-117">Példák</span><span class="sxs-lookup"><span data-stu-id="9b816-117">EXAMPLES</span></span>

### <span data-ttu-id="9b816-118">1. példa: házirend-események beolvasása a jelenlegi előfizetési tartományban</span><span class="sxs-lookup"><span data-stu-id="9b816-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="9b816-119">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="9b816-120">2. példa: házirend-események beolvasása a megadott előfizetési tartományba</span><span class="sxs-lookup"><span data-stu-id="9b816-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="9b816-121">A megadott előfizetésben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="9b816-122">3. példa: házirend-események beolvasása a felügyeleti csoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="9b816-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="9b816-123">A megadott felügyeleti csoport összes erőforrásának utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="9b816-124">Példa 4: házirend-események beolvasása az erőforráscsoport hatókörében a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="9b816-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9b816-125">A megadott erőforráscsoporthoz tartozó összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja (az előfizetésben a jelenlegi munkamenet-környezetben).</span><span class="sxs-lookup"><span data-stu-id="9b816-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="9b816-126">Példa 5: házirend-események beolvasása az erőforráscsoport hatókörében a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="9b816-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9b816-127">A megadott erőforráscsoporthoz tartozó összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja (a megadott előfizetésben).</span><span class="sxs-lookup"><span data-stu-id="9b816-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="9b816-128">Példa 6: házirend-események beszerzése egy erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="9b816-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="9b816-129">A megadott erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="9b816-130">7. példa: házirend-események beolvasása egy házirend-definíciós definícióban a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="9b816-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9b816-131">Az utolsó nap során az összes erőforrás (a bérlői fiók jelenlegi környezetében) által generált házirend-esemény rekordjait kapja meg (ez az előfizetésben a jelenlegi munkamenet-környezetben létezik).</span><span class="sxs-lookup"><span data-stu-id="9b816-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9b816-132">8. példa: házirend-események beolvasása a megadott előfizetéshez beállított házirend-definícióban</span><span class="sxs-lookup"><span data-stu-id="9b816-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9b816-133">Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői környezetben), amelyet a megadott házirend-készlet definíciója (amely a megadott előfizetésben létezik).</span><span class="sxs-lookup"><span data-stu-id="9b816-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9b816-134">Példa 9: házirend-események beolvasása egy házirend-definícióra a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="9b816-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9b816-135">Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői környezetben), amelyet a megadott házirend-definíció (amely az előfizetésben létezik a jelenlegi munkamenet-környezetben).</span><span class="sxs-lookup"><span data-stu-id="9b816-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9b816-136">10. példa: házirend-események beolvasása a megadott előfizetésben lévő házirend-definícióhoz</span><span class="sxs-lookup"><span data-stu-id="9b816-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9b816-137">A megadott házirend-definíció (amely a megadott előfizetésben található) minden erőforrásnál (az aktuális munkamenetben) szereplő összes erőforrás utolsó napján keletkezett házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9b816-138">11-es példa: házirend-hozzárendelések beszerzése a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="9b816-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9b816-139">Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői környezetben), amelyet a megadott házirend-hozzárendelés (amely az előfizetésben létezik a jelenlegi munkamenet-környezetben).</span><span class="sxs-lookup"><span data-stu-id="9b816-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9b816-140">12 példa: házirend-események beszerzése a megadott előfizetésben szereplő házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="9b816-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9b816-141">A megadott házirend-hozzárendeléssel (amely a megadott előfizetésben található) minden erőforrás esetében az utolsó napon generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9b816-142">Példa: házirend-események beszerzése az aktuális előfizetéshez megadott erőforráscsoport házirend-hozzárendeléseihez</span><span class="sxs-lookup"><span data-stu-id="9b816-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9b816-143">Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői kontextusban), amelyet a megadott házirend-hozzárendelés (amely az előfizetéshez tartozó erőforrás csoportban található) adott meg.</span><span class="sxs-lookup"><span data-stu-id="9b816-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="9b816-144">14 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, a OrderBy, a felső és a lekérdezési beállítások megadása</span><span class="sxs-lookup"><span data-stu-id="9b816-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="9b816-145">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9b816-146">A parancs időbélyegző és házirend-hozzárendelési név tulajdonságai szerint rendeli az eredményeket, és az adott sorrendben szereplő adatok közül csak az 5-öt veszi át.</span><span class="sxs-lookup"><span data-stu-id="9b816-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="9b816-147">Azt is megadhatja, hogy csak az egyes rekordok oszlopait szeretné megjeleníteni.</span><span class="sxs-lookup"><span data-stu-id="9b816-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="9b816-148">15 példa: házirend-események beolvasása a jelenlegi előfizetési tartományból, a feladó és a lekérdezés beállításaival</span><span class="sxs-lookup"><span data-stu-id="9b816-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="9b816-149">Az előfizetésben az összes erőforráshoz megadott időtartományon belül az aktuális munkamenet-környezetben megjelenő házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="9b816-150">16 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, a szűrő lekérdezése beállítással</span><span class="sxs-lookup"><span data-stu-id="9b816-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="9b816-151">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="9b816-152">A parancs a házirend-definíciós művelet (beleértve a Megtagadás vagy a naplózási műveletek) és az erőforrás hely szerinti szűréssel visszaadott eredményeket korlátozza (a eastus helyének kizárása).</span><span class="sxs-lookup"><span data-stu-id="9b816-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="9b816-153">17 példa: házirend-események beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="9b816-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="9b816-154">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjainak számát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9b816-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="9b816-155">A parancs csak a AdditionalProperties tulajdonságban megadott házirend-esemény rekordjainak számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9b816-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="9b816-156">18 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, az összesítéssel való csoportosítást alkalmazva</span><span class="sxs-lookup"><span data-stu-id="9b816-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="9b816-157">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9b816-158">A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (csak a naplózási és elutasítási eseményeket tartalmazza) korlátozza.</span><span class="sxs-lookup"><span data-stu-id="9b816-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="9b816-159">A házirend-hozzárendelés, a házirend-definíció, a házirend-definíciós műveletek és az erőforrás-azonosító alapján csoportosítja az eredményeket, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9b816-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="9b816-160">Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="9b816-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="9b816-161">19 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, az Összesítés nélküli csoportosítás megadása</span><span class="sxs-lookup"><span data-stu-id="9b816-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="9b816-162">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9b816-163">A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (csak a naplózási és elutasítási eseményeket tartalmazza) korlátozza.</span><span class="sxs-lookup"><span data-stu-id="9b816-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="9b816-164">Az eredmény az erőforrás-azonosító alapján csoportosítja a találatokat. Ezzel létrehozhatja az előfizetésben szereplő összes erőforrás listáját, amely egy házirend-eseményt generált legalább egy naplózási vagy elutasítási házirendhez.</span><span class="sxs-lookup"><span data-stu-id="9b816-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="9b816-165">20 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, a több csoportra vonatkozó meghatározás alkalmazása</span><span class="sxs-lookup"><span data-stu-id="9b816-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="9b816-166">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.</span><span class="sxs-lookup"><span data-stu-id="9b816-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9b816-167">A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (csak a Megtagadás eseményeket tartalmazza) korlátozza.</span><span class="sxs-lookup"><span data-stu-id="9b816-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="9b816-168">Az eredményeket először a házirend-hozzárendelés, a házirend-definíció és az erőforrás-azonosító alapján csoportosítja. Ezután az erőforrás-azonosító kivételével továbbra is csoportosítja a csoportosítás eredményét, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9b816-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="9b816-169">Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="9b816-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="9b816-170">Ez a Top 5 tiltó házirendet hozza létre a legtöbb megtagadott erőforrással.</span><span class="sxs-lookup"><span data-stu-id="9b816-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="9b816-171">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b816-171">PARAMETERS</span></span>

### <span data-ttu-id="9b816-172">-Apply (alkalmazás)</span><span class="sxs-lookup"><span data-stu-id="9b816-172">-Apply</span></span>
<span data-ttu-id="9b816-173">A kifejezés alkalmazása az összesítésekre a OData jelöléssel.</span><span class="sxs-lookup"><span data-stu-id="9b816-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="9b816-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b816-174">-DefaultProfile</span></span>
<span data-ttu-id="9b816-175">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b816-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b816-176">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="9b816-176">-Filter</span></span>
<span data-ttu-id="9b816-177">A kifejezés szűrése OData jelöléssel</span><span class="sxs-lookup"><span data-stu-id="9b816-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="9b816-178">-From</span><span class="sxs-lookup"><span data-stu-id="9b816-178">-From</span></span>
<span data-ttu-id="9b816-179">Az ISO 8601 formázott időbélyegző adja meg a lekérdezni kívánt intervallum kezdési időpontját.</span><span class="sxs-lookup"><span data-stu-id="9b816-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="9b816-180">Ha nincs megadva, az alapértelmezett érték "to" paraméterérték mínusz 1 nap.</span><span class="sxs-lookup"><span data-stu-id="9b816-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="9b816-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9b816-181">-ManagementGroupName</span></span>
<span data-ttu-id="9b816-182">A felügyeleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b816-182">Management group name.</span></span>

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

### <span data-ttu-id="9b816-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9b816-183">-OrderBy</span></span>
<span data-ttu-id="9b816-184">A kifejezés megrendelése OData jelöléssel</span><span class="sxs-lookup"><span data-stu-id="9b816-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="9b816-185">Egy vagy több vesszővel elválasztott oszlop neve, amely nem kötelező "desc" (alapértelmezett) vagy "ASC".</span><span class="sxs-lookup"><span data-stu-id="9b816-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="9b816-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9b816-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="9b816-187">Házirend-hozzárendelés neve</span><span class="sxs-lookup"><span data-stu-id="9b816-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="9b816-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9b816-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="9b816-189">Házirend-definíció neve</span><span class="sxs-lookup"><span data-stu-id="9b816-189">Policy definition name.</span></span>

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

### <span data-ttu-id="9b816-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9b816-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="9b816-191">Házirend-definíció neve</span><span class="sxs-lookup"><span data-stu-id="9b816-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="9b816-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b816-192">-ResourceGroupName</span></span>
<span data-ttu-id="9b816-193">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9b816-193">Resource group name.</span></span>

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

### <span data-ttu-id="9b816-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b816-194">-ResourceId</span></span>
<span data-ttu-id="9b816-195">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9b816-195">Resource ID.</span></span>

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

### <span data-ttu-id="9b816-196">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="9b816-196">-Select</span></span>
<span data-ttu-id="9b816-197">Jelölje ki a kifejezést a OData jelöléssel.</span><span class="sxs-lookup"><span data-stu-id="9b816-197">Select expression using OData notation.</span></span>
<span data-ttu-id="9b816-198">Egy vagy több pontosvesszővel tagolt oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9b816-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="9b816-199">Az egyes rekordok oszlopait csak a kért értékekre korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="9b816-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="9b816-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b816-200">-SubscriptionId</span></span>
<span data-ttu-id="9b816-201">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="9b816-201">Subscription ID.</span></span>

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

### <span data-ttu-id="9b816-202">-To</span><span class="sxs-lookup"><span data-stu-id="9b816-202">-To</span></span>
<span data-ttu-id="9b816-203">ISO 8601 formázott időbélyegző a lekérdezési intervallum befejezési időpontjának megadásával.</span><span class="sxs-lookup"><span data-stu-id="9b816-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="9b816-204">Ha nincs megadva, az alapértelmezett beállítás a kérés időpontjában.</span><span class="sxs-lookup"><span data-stu-id="9b816-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="9b816-205">-Top</span><span class="sxs-lookup"><span data-stu-id="9b816-205">-Top</span></span>
<span data-ttu-id="9b816-206">A visszaadni kívánt rekordok maximális száma</span><span class="sxs-lookup"><span data-stu-id="9b816-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="9b816-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b816-207">CommonParameters</span></span>
<span data-ttu-id="9b816-208">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b816-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b816-209">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b816-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b816-210">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b816-210">INPUTS</span></span>

### <span data-ttu-id="9b816-211">System. String</span><span class="sxs-lookup"><span data-stu-id="9b816-211">System.String</span></span>

## <span data-ttu-id="9b816-212">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b816-212">OUTPUTS</span></span>

### <span data-ttu-id="9b816-213">Microsoft. Azure. Command. PolicyInsights. models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="9b816-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="9b816-214">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b816-214">NOTES</span></span>

## <span data-ttu-id="9b816-215">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b816-215">RELATED LINKS</span></span>
