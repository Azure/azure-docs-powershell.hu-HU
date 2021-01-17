---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481037"
---
# <span data-ttu-id="19dda-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="19dda-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="19dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19dda-102">SYNOPSIS</span></span>
<span data-ttu-id="19dda-103">Az erőforrásokra vonatkozó legújabb szabályzat-megfelelőségi összefoglalást kap.</span><span class="sxs-lookup"><span data-stu-id="19dda-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="19dda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19dda-104">SYNTAX</span></span>

### <span data-ttu-id="19dda-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19dda-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19dda-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="19dda-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19dda-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="19dda-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="19dda-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="19dda-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="19dda-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="19dda-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19dda-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="19dda-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19dda-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19dda-113">DESCRIPTION</span></span>
<span data-ttu-id="19dda-114">Összegző nézetet kap a házirendek megfelelőségi állapotszámairól különböző hatókörökben, házirend-hozzárendelések és házirend-definíciók szerint bontva.</span><span class="sxs-lookup"><span data-stu-id="19dda-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="19dda-115">Csak a házirendnek nem megfelelő államokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="19dda-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="19dda-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19dda-116">EXAMPLES</span></span>

### <span data-ttu-id="19dda-117">1. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben</span><span class="sxs-lookup"><span data-stu-id="19dda-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="19dda-118">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja.</span><span class="sxs-lookup"><span data-stu-id="19dda-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="19dda-119">2. példa: A házirendek legújabb, nem megfelelő államokkal kapcsolatos összesítése a megadott előfizetési hatókörben</span><span class="sxs-lookup"><span data-stu-id="19dda-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="19dda-120">A megadott előfizetésben található összes erőforrás utolsó napján létrehozott legújabb házirend-megfelelőségi államok összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="19dda-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="19dda-121">3. példa: A házirendek legújabb, nem megfelelő államokkal kapcsolatos összegzése a felügyeleti csoportok hatókörében</span><span class="sxs-lookup"><span data-stu-id="19dda-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="19dda-122">A megadott felügyeleti csoportban található összes erőforrás utolsó napján létrehozott legújabb házirend-megfelelőségi államok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="19dda-123">4. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetés erőforráscsoport-hatókörében</span><span class="sxs-lookup"><span data-stu-id="19dda-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="19dda-124">A megadott erőforráscsoport összes erőforrásához (az aktuális munkamenet kontextusában az előfizetéshez) az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="19dda-125">5. példa: Legújabb, nem megfelelő házirend-államok összesítése a megadott előfizetés erőforráscsoport-hatókörében</span><span class="sxs-lookup"><span data-stu-id="19dda-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="19dda-126">A megadott erőforráscsoporton belül (a megadott előfizetésben) az utolsó napon létrehozott legújabb házirend-megfelelőségi államok összegzését kapja.</span><span class="sxs-lookup"><span data-stu-id="19dda-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="19dda-127">6. példa: Az erőforrás legújabb, nem megfelelő házirend-államokra vonatkozó összesítésének lekérte</span><span class="sxs-lookup"><span data-stu-id="19dda-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="19dda-128">A megadott erőforrás utolsó napján létrehozott legújabb házirend-megfelelőségi államok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="19dda-129">7. példa: Az aktuális előfizetés házirendkészlet-definíciójának legújabb, nem megfelelő házirend-állapotok összesítése</span><span class="sxs-lookup"><span data-stu-id="19dda-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="19dda-130">A megadott házirendkészlet-definíció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="19dda-131">8. példa: A házirend-definíció legújabb, nem megfelelő házirend-államokra vonatkozó összegzése a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="19dda-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="19dda-132">A megadott házirendkészlet-definíció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirend-megfelelőségi állapotok összegzési nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="19dda-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="19dda-133">9. példa: Az aktuális előfizetés házirenddefiníciójának legújabb, nem megfelelő házirend-állapotok összesítése</span><span class="sxs-lookup"><span data-stu-id="19dda-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="19dda-134">A megadott házirenddefiníció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="19dda-135">10. példa: A házirendek legújabb, nem megfelelő államokkal kapcsolatos összesítése a megadott előfizetés házirenddefinícióiról</span><span class="sxs-lookup"><span data-stu-id="19dda-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="19dda-136">A megadott házirenddefiníció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="19dda-137">11. példa: Az aktuális előfizetés házirend-hozzárendelésének legújabb, nem megfelelő házirend-állapotok összefoglalása</span><span class="sxs-lookup"><span data-stu-id="19dda-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="19dda-138">A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="19dda-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="19dda-139">12. példa: A házirendek legújabb, nem megfelelő államokra vonatkozó összegzése a megadott előfizetés házirend-hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="19dda-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="19dda-140">A megadott házirend-hozzárendelés által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott házirend-megfelelőségi állapotok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="19dda-141">13. példa: Az aktuális előfizetés megadott erőforráscsoportja házirend-hozzárendelésének legújabb, nem megfelelő házirend-állapotok összegzése</span><span class="sxs-lookup"><span data-stu-id="19dda-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="19dda-142">A megadott házirend-hozzárendelés által (az előfizetés aktuális munkamenet kontextusában az erőforráscsoportban megtalálható) összes erőforrásra vonatkozóan az utolsó napon létrehozott házirend-megfelelőségi állapotok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="19dda-143">14. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben, felülről lekérdezhető beállítással</span><span class="sxs-lookup"><span data-stu-id="19dda-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="19dda-144">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja.</span><span class="sxs-lookup"><span data-stu-id="19dda-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="19dda-145">A parancs csökkenő sorrendbe rendezi az eredményekben a házirend-hozzárendelések összegzését úgy, hogy a nem megfelelő erőforrások száma csökkenő sorrendben van, és a házirend-hozzárendelések összefoglalói közül csak az első 5-öt veszi fel.</span><span class="sxs-lookup"><span data-stu-id="19dda-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="19dda-146">15. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben, a From and To lekérdezési beállításokkal</span><span class="sxs-lookup"><span data-stu-id="19dda-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="19dda-147">Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához megadott dátumtartományon belül létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.</span><span class="sxs-lookup"><span data-stu-id="19dda-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="19dda-148">16. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben a Szűrő lekérdezés lehetőséggel</span><span class="sxs-lookup"><span data-stu-id="19dda-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="19dda-149">Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja.</span><span class="sxs-lookup"><span data-stu-id="19dda-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="19dda-150">A parancs korlátozza a házirenddefiníciós művelet (beleértve az elutasítási vagy naplózási műveleteket) és az erőforrás helye alapján végzett szűrés által visszaadott eredményeket (a független helyeket nem foglalja magában).</span><span class="sxs-lookup"><span data-stu-id="19dda-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="19dda-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19dda-151">PARAMETERS</span></span>

### <span data-ttu-id="19dda-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dda-152">-DefaultProfile</span></span>
<span data-ttu-id="19dda-153">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19dda-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19dda-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="19dda-154">-Filter</span></span>
<span data-ttu-id="19dda-155">Filter expression using OData notation.</span><span class="sxs-lookup"><span data-stu-id="19dda-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="19dda-156">-From</span><span class="sxs-lookup"><span data-stu-id="19dda-156">-From</span></span>
<span data-ttu-id="19dda-157">ISO 8601 formázott időbélyeg, amely a lekérdezési időköz kezdő idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19dda-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="19dda-158">Ha nincs megadva, az alapértelmezett érték a "To" paraméter értéke mínusz 1 nap.</span><span class="sxs-lookup"><span data-stu-id="19dda-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="19dda-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="19dda-159">-ManagementGroupName</span></span>
<span data-ttu-id="19dda-160">Felügyeleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="19dda-160">Management group name.</span></span>

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

### <span data-ttu-id="19dda-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="19dda-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="19dda-162">Házirend-hozzárendelés neve.</span><span class="sxs-lookup"><span data-stu-id="19dda-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="19dda-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="19dda-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="19dda-164">Házirenddefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="19dda-164">Policy definition name.</span></span>

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

### <span data-ttu-id="19dda-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="19dda-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="19dda-166">Házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="19dda-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="19dda-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19dda-167">-ResourceGroupName</span></span>
<span data-ttu-id="19dda-168">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="19dda-168">Resource group name.</span></span>

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

### <span data-ttu-id="19dda-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19dda-169">-ResourceId</span></span>
<span data-ttu-id="19dda-170">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="19dda-170">Resource ID.</span></span>

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

### <span data-ttu-id="19dda-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19dda-171">-SubscriptionId</span></span>
<span data-ttu-id="19dda-172">Előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="19dda-172">Subscription ID.</span></span>

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

### <span data-ttu-id="19dda-173">-To</span><span class="sxs-lookup"><span data-stu-id="19dda-173">-To</span></span>
<span data-ttu-id="19dda-174">ISO 8601 formázott időbélyeg, amely megadja a lekérdezési időköz záró idejét.</span><span class="sxs-lookup"><span data-stu-id="19dda-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="19dda-175">Ha nincs megadva, a kérések alapértelmezett ideje.</span><span class="sxs-lookup"><span data-stu-id="19dda-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="19dda-176">-Top</span><span class="sxs-lookup"><span data-stu-id="19dda-176">-Top</span></span>
<span data-ttu-id="19dda-177">A vissza nem térhet rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="19dda-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="19dda-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dda-178">CommonParameters</span></span>
<span data-ttu-id="19dda-179">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dda-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dda-180">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19dda-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dda-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19dda-181">INPUTS</span></span>

### <span data-ttu-id="19dda-182">System.String</span><span class="sxs-lookup"><span data-stu-id="19dda-182">System.String</span></span>

## <span data-ttu-id="19dda-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19dda-183">OUTPUTS</span></span>

### <span data-ttu-id="19dda-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="19dda-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="19dda-185">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19dda-185">NOTES</span></span>

## <span data-ttu-id="19dda-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19dda-186">RELATED LINKS</span></span>

[<span data-ttu-id="19dda-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="19dda-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
