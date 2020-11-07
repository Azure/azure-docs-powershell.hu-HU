---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 93c31a9a8a1b2f161553efdabce2d97ed19caacd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838397"
---
# <span data-ttu-id="31c28-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="31c28-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="31c28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31c28-102">SYNOPSIS</span></span>
<span data-ttu-id="31c28-103">A legújabb házirend-megfelelőségi állapotok összegzése az erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="31c28-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="31c28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31c28-104">SYNTAX</span></span>

### <span data-ttu-id="31c28-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31c28-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c28-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="31c28-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c28-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="31c28-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31c28-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="31c28-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31c28-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="31c28-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31c28-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="31c28-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31c28-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="31c28-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c28-112">ResourceScope paraméternél</span><span class="sxs-lookup"><span data-stu-id="31c28-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31c28-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="31c28-113">DESCRIPTION</span></span>
<span data-ttu-id="31c28-114">A házirend-hozzárendelések és a házirend-definíciók szerint részletezett, a legutóbb követett házirend-megfelelőségi állapotokat tartalmazó összefoglaló nézetet kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="31c28-115">Csak a nem megfelelő házirend-állapotokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="31c28-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="31c28-116">Példák</span><span class="sxs-lookup"><span data-stu-id="31c28-116">EXAMPLES</span></span>

### <span data-ttu-id="31c28-117">Példa 1: a legújabb, nem kompatibilis házirend-Államok összefoglalása a jelenlegi előfizetési tartományba</span><span class="sxs-lookup"><span data-stu-id="31c28-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="31c28-118">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31c28-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="31c28-119">2. példa: a legújabb, nem kompatibilis házirend-Államok összegzésének beszerzése a megadott előfizetési tartományba</span><span class="sxs-lookup"><span data-stu-id="31c28-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="31c28-120">A megadott előfizetésben szereplő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="31c28-121">3. példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a felügyeleti csoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="31c28-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="31c28-122">Az utolsó napon az adott kezelési csoportban található összes erőforrás utolsó napján generált házirend-megfelelőségi állapotának összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="31c28-123">Példa 4: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése az erőforráscsoport hatókörében a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="31c28-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="31c28-124">Az utolsó napon a megadott erőforráscsoport összes erőforrásának utolsó napján generált házirend-megfelelőségi állapot összefoglaló nézetét kapja (az előfizetésben a jelenlegi munkamenet-környezetben).</span><span class="sxs-lookup"><span data-stu-id="31c28-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="31c28-125">Példa 5: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése az erőforráscsoport hatókörében a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="31c28-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="31c28-126">Az utolsó napon a megadott erőforráscsoport (a megadott előfizetés) összes erőforrásának utolsó napján generált házirend-megfelelőségi állapotának összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="31c28-127">Példa 6: a legkésőbbi, nem kompatibilis házirend-Államok összefoglalójának beszerzése erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="31c28-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="31c28-128">A megadott erőforrás utolsó napján generált házirend-megfelelőségi országok összefoglaló nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31c28-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="31c28-129">7. példa: a legutóbb nem kompatibilis házirend-állapotok összefoglalása egy házirend-készlet definíciójában a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="31c28-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="31c28-130">Az aktuális munkamenetben az előfizetésben szereplő összes erőforrás (az aktuális munkamenet kontextusában megtalálható) utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31c28-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="31c28-131">8. példa: a legutóbb nem kompatibilis házirend-állapotok összefoglalása a megadott előfizetéshez tartozó házirend-definíciós definícióban</span><span class="sxs-lookup"><span data-stu-id="31c28-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="31c28-132">Az utolsó napon az összes erőforrás (az aktuális munkamenetben a bérlőn belül) által generált utolsó, az utolsó napon létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja meg (amely a megadott előfizetésben található).</span><span class="sxs-lookup"><span data-stu-id="31c28-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="31c28-133">Példa 9: a legújabb, nem kompatibilis házirend-Államok összefoglalása a jelenlegi előfizetés házirend-definíciójának összegzése</span><span class="sxs-lookup"><span data-stu-id="31c28-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="31c28-134">A legutóbbi, az előfizetésben az aktuális munkamenet kontextusában található (az előfizetésben a jelenlegi munkamenetben) által megvalósított összes erőforrás utolsó napján generált, a legutóbb létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="31c28-135">10. példa: a legújabb, nem kompatibilis házirend-állapotok összefoglalása a megadott előfizetésben lévő házirend-definícióhoz</span><span class="sxs-lookup"><span data-stu-id="31c28-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="31c28-136">Megtekintheti a legutóbbi, a megadott házirend-definícióval (a megadott előfizetésben található) erőforrásokkal (az aktuális munkamenetben a bérlőn belül) az összes erőforrás utolsó napján létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét.</span><span class="sxs-lookup"><span data-stu-id="31c28-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="31c28-137">11. példa: a legutóbb nem kompatibilis házirendek összegzése a meglévő előfizetésben lévő házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="31c28-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="31c28-138">A legutóbbi, az előfizetésben az aktuális munkamenet kontextusában megtalálható erőforrás-hozzárendelések utolsó napján létrehozott, a legutóbb létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="31c28-139">12. példa: a legutóbb nem kompatibilis házirend-állapotok összefoglalása a megadott előfizetéshez tartozó házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="31c28-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="31c28-140">Az utolsó napon létrehozott, a legutóbb létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja meg a megadott házirend-hozzárendeléssel (amely a megadott előfizetésben létezik).</span><span class="sxs-lookup"><span data-stu-id="31c28-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="31c28-141">13. példa: az aktuális előfizetéshez tartozó meghatározott erőforráscsoport házirend-hozzárendeléseinek összefoglalása a legutóbb nem megfelelő házirend-hozzárendelésekkel</span><span class="sxs-lookup"><span data-stu-id="31c28-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="31c28-142">Az aktuális munkamenetben az előfizetésben szereplő erőforrás-hozzárendelésben (az aktuális munkamenet-környezetben) az összes erőforrás utolsó napján létrehozott, a legutóbb létrehozott házirendek megfelelőségi állapotának összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="31c28-143">14 példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a jelenlegi előfizetési tartományba, a felső lekérdezés beállítással</span><span class="sxs-lookup"><span data-stu-id="31c28-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="31c28-144">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31c28-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="31c28-145">A parancs a házirend-hozzárendelés összefoglalóit nem megfelelő erőforrásokkal rendeli az eredményben, és a házirend-hozzárendelési összesítések közül csak a legfelső 5-öt veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="31c28-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="31c28-146">15. példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a jelenlegi előfizetési tartományba, a feladó és a lekérdezés beállításaival</span><span class="sxs-lookup"><span data-stu-id="31c28-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="31c28-147">Az előfizetésben a jelenlegi munkamenet-környezetben az összes erőforráshoz megadott dátumtartomány által generált legutóbb létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="31c28-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="31c28-148">16. példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a jelenlegi előfizetési tartományba, a szűrő lekérdezése beállítással</span><span class="sxs-lookup"><span data-stu-id="31c28-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="31c28-149">Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31c28-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="31c28-150">A parancs a házirend-definíciós műveleteken (beleértve a Megtagadás vagy a naplózási műveleteket) alapuló szűréssel, valamint az erőforrás helyével (a eastus helyének kivételével) korlátozza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="31c28-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="31c28-151">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31c28-151">PARAMETERS</span></span>

### <span data-ttu-id="31c28-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c28-152">-DefaultProfile</span></span>
<span data-ttu-id="31c28-153">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31c28-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31c28-154">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="31c28-154">-Filter</span></span>
<span data-ttu-id="31c28-155">A kifejezés szűrése OData jelöléssel</span><span class="sxs-lookup"><span data-stu-id="31c28-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="31c28-156">-From</span><span class="sxs-lookup"><span data-stu-id="31c28-156">-From</span></span>
<span data-ttu-id="31c28-157">Az ISO 8601 formázott időbélyegző adja meg a lekérdezni kívánt intervallum kezdési időpontját.</span><span class="sxs-lookup"><span data-stu-id="31c28-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="31c28-158">Ha nincs megadva, az alapértelmezett érték "to" paraméterérték mínusz 1 nap.</span><span class="sxs-lookup"><span data-stu-id="31c28-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="31c28-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="31c28-159">-ManagementGroupName</span></span>
<span data-ttu-id="31c28-160">A felügyeleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="31c28-160">Management group name.</span></span>

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

### <span data-ttu-id="31c28-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="31c28-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="31c28-162">Házirend-hozzárendelés neve</span><span class="sxs-lookup"><span data-stu-id="31c28-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="31c28-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="31c28-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="31c28-164">Házirend-definíció neve</span><span class="sxs-lookup"><span data-stu-id="31c28-164">Policy definition name.</span></span>

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

### <span data-ttu-id="31c28-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="31c28-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="31c28-166">Házirend-definíció neve</span><span class="sxs-lookup"><span data-stu-id="31c28-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="31c28-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c28-167">-ResourceGroupName</span></span>
<span data-ttu-id="31c28-168">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="31c28-168">Resource group name.</span></span>

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

### <span data-ttu-id="31c28-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31c28-169">-ResourceId</span></span>
<span data-ttu-id="31c28-170">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="31c28-170">Resource ID.</span></span>

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

### <span data-ttu-id="31c28-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31c28-171">-SubscriptionId</span></span>
<span data-ttu-id="31c28-172">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="31c28-172">Subscription ID.</span></span>

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

### <span data-ttu-id="31c28-173">-To</span><span class="sxs-lookup"><span data-stu-id="31c28-173">-To</span></span>
<span data-ttu-id="31c28-174">ISO 8601 formázott időbélyegző a lekérdezési intervallum befejezési időpontjának megadásával.</span><span class="sxs-lookup"><span data-stu-id="31c28-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="31c28-175">Ha nincs megadva, az alapértelmezett beállítás a kérés időpontjában.</span><span class="sxs-lookup"><span data-stu-id="31c28-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="31c28-176">-Top</span><span class="sxs-lookup"><span data-stu-id="31c28-176">-Top</span></span>
<span data-ttu-id="31c28-177">A visszaadni kívánt rekordok maximális száma</span><span class="sxs-lookup"><span data-stu-id="31c28-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="31c28-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c28-178">CommonParameters</span></span>
<span data-ttu-id="31c28-179">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31c28-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c28-180">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c28-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c28-181">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31c28-181">INPUTS</span></span>

### <span data-ttu-id="31c28-182">System. String</span><span class="sxs-lookup"><span data-stu-id="31c28-182">System.String</span></span>

## <span data-ttu-id="31c28-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31c28-183">OUTPUTS</span></span>

### <span data-ttu-id="31c28-184">Microsoft. Azure. Command. PolicyInsights. models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="31c28-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="31c28-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31c28-185">NOTES</span></span>

## <span data-ttu-id="31c28-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31c28-186">RELATED LINKS</span></span>

[<span data-ttu-id="31c28-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="31c28-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
