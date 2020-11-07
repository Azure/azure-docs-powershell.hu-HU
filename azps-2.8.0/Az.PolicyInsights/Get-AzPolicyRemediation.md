---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44f7d3331d32092636c53850b0315f34b7df7808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838401"
---
# <span data-ttu-id="7e585-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="7e585-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="7e585-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e585-102">SYNOPSIS</span></span>
<span data-ttu-id="7e585-103">Házirend-visszaközvetítést kap.</span><span class="sxs-lookup"><span data-stu-id="7e585-103">Gets policy remediations.</span></span>

## <span data-ttu-id="7e585-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e585-104">SYNTAX</span></span>

### <span data-ttu-id="7e585-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e585-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e585-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7e585-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e585-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="7e585-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e585-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="7e585-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e585-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="7e585-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e585-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e585-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e585-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e585-111">DESCRIPTION</span></span>
<span data-ttu-id="7e585-112">A **Get-AzPolicyRemediation** parancsmag az összes házirend-szervizelést egy hatókörben vagy egy bizonyos szervizelésben kapja.</span><span class="sxs-lookup"><span data-stu-id="7e585-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="7e585-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7e585-113">EXAMPLES</span></span>

### <span data-ttu-id="7e585-114">Példa 1: az összes házirend-kármentesítés beszerzése az aktuális előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="7e585-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="7e585-115">Ez a parancs a "saját előfizetés" nevű előfizetéshez tartozó vagy alatt létrehozott összes szervizelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="7e585-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="7e585-116">2. példa: speciális házirend-szervizelés és a központi üzembe állítás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="7e585-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="7e585-117">Ez a parancs a "remediation1" nevű "myResourceGroup" nevű szervizelést kapja.</span><span class="sxs-lookup"><span data-stu-id="7e585-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="7e585-118">A program felveszi a visszaközvetített források részleteit.</span><span class="sxs-lookup"><span data-stu-id="7e585-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="7e585-119">3. példa: a kezelési csoportban 10 házirend-rehabilitáció beszerzése választható szűrőkkel</span><span class="sxs-lookup"><span data-stu-id="7e585-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="7e585-120">Ez a parancs az "mg1" nevű felügyeleti csoportból legfeljebb 10 házirend-szervizelést kap.</span><span class="sxs-lookup"><span data-stu-id="7e585-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="7e585-121">A program csak a megadott házirend-hozzárendeléshez tartozó házirend-szervizelést olvassa be.</span><span class="sxs-lookup"><span data-stu-id="7e585-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="7e585-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e585-122">PARAMETERS</span></span>

### <span data-ttu-id="7e585-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e585-123">-DefaultProfile</span></span>
<span data-ttu-id="7e585-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e585-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e585-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="7e585-125">-Filter</span></span>
<span data-ttu-id="7e585-126">A kifejezés szűrése OData jelöléssel</span><span class="sxs-lookup"><span data-stu-id="7e585-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e585-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="7e585-127">-IncludeDetail</span></span>
<span data-ttu-id="7e585-128">A kármentesítés által létrehozott bevezetések részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7e585-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e585-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7e585-129">-ManagementGroupName</span></span>
<span data-ttu-id="7e585-130">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="7e585-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="7e585-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e585-131">-Name</span></span>
<span data-ttu-id="7e585-132">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="7e585-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e585-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e585-133">-ResourceGroupName</span></span>
<span data-ttu-id="7e585-134">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7e585-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e585-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e585-135">-ResourceId</span></span>
<span data-ttu-id="7e585-136">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7e585-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e585-137">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="7e585-137">-Scope</span></span>
<span data-ttu-id="7e585-138">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="7e585-138">Scope of the resource.</span></span> <span data-ttu-id="7e585-139">Például "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="7e585-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e585-140">-Top</span><span class="sxs-lookup"><span data-stu-id="7e585-140">-Top</span></span>
<span data-ttu-id="7e585-141">A visszaadni kívánt rekordok maximális száma</span><span class="sxs-lookup"><span data-stu-id="7e585-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="7e585-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e585-142">CommonParameters</span></span>
<span data-ttu-id="7e585-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e585-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e585-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e585-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e585-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e585-145">INPUTS</span></span>

### <span data-ttu-id="7e585-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7e585-146">System.String</span></span>

## <span data-ttu-id="7e585-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e585-147">OUTPUTS</span></span>

### <span data-ttu-id="7e585-148">Microsoft. Azure. Command. PolicyInsights. models. remediáció. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="7e585-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="7e585-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e585-149">NOTES</span></span>

## <span data-ttu-id="7e585-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e585-150">RELATED LINKS</span></span>
