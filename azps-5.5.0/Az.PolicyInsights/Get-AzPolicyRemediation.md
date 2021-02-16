---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160395"
---
# <span data-ttu-id="3166c-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="3166c-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="3166c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3166c-102">SYNOPSIS</span></span>
<span data-ttu-id="3166c-103">Házirend-szervizelést kap.</span><span class="sxs-lookup"><span data-stu-id="3166c-103">Gets policy remediations.</span></span>

## <span data-ttu-id="3166c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3166c-104">SYNTAX</span></span>

### <span data-ttu-id="3166c-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3166c-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3166c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3166c-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3166c-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="3166c-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3166c-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="3166c-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3166c-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="3166c-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3166c-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3166c-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3166c-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3166c-111">DESCRIPTION</span></span>
<span data-ttu-id="3166c-112">A **Get-AzPolicyRemediation** parancsmag minden házirend-szervizelést egy adott hatókörben vagy egy adott szervizelésben kap.</span><span class="sxs-lookup"><span data-stu-id="3166c-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="3166c-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3166c-113">EXAMPLES</span></span>

### <span data-ttu-id="3166c-114">1. példa: Az aktuális előfizetés összes házirend-szervizelése</span><span class="sxs-lookup"><span data-stu-id="3166c-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="3166c-115">Ez a parancs a "Saját előfizetés" nevű előfizetésben vagy alatt létrehozott összes szervizelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="3166c-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="3166c-116">2. példa: Házirend-szervizelés és a telepítés részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="3166c-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="3166c-117">Ez a parancs a "myResourceGroup" erőforráscsoportból a "szervizelés1" nevű szervizelést kapja.</span><span class="sxs-lookup"><span data-stu-id="3166c-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="3166c-118">A szervizbe foglalt erőforrások részletei is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="3166c-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="3166c-119">3. példa: 10 házirend-szervizelés egy felügyeleti csoportban opcionális szűrőkkel</span><span class="sxs-lookup"><span data-stu-id="3166c-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="3166c-120">Ez a parancs legfeljebb 10 házirend-szervizelést kap egy "1" nevű felügyeleti csoporttól.</span><span class="sxs-lookup"><span data-stu-id="3166c-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="3166c-121">A program csak az adott házirend-hozzárendelésre vonatkozó házirend-szervizeléseket olvassa be.</span><span class="sxs-lookup"><span data-stu-id="3166c-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="3166c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3166c-122">PARAMETERS</span></span>

### <span data-ttu-id="3166c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3166c-123">-DefaultProfile</span></span>
<span data-ttu-id="3166c-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3166c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3166c-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="3166c-125">-Filter</span></span>
<span data-ttu-id="3166c-126">Kifejezésszűrés OData-ként</span><span class="sxs-lookup"><span data-stu-id="3166c-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="3166c-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="3166c-127">-IncludeDetail</span></span>
<span data-ttu-id="3166c-128">Tartalmazza a szervizelés által létrehozott telepítéseket.</span><span class="sxs-lookup"><span data-stu-id="3166c-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="3166c-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3166c-129">-ManagementGroupName</span></span>
<span data-ttu-id="3166c-130">Felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3166c-130">Management group ID.</span></span>

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

### <span data-ttu-id="3166c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3166c-131">-Name</span></span>
<span data-ttu-id="3166c-132">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3166c-132">Resource name.</span></span>

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

### <span data-ttu-id="3166c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3166c-133">-ResourceGroupName</span></span>
<span data-ttu-id="3166c-134">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3166c-134">Resource group name.</span></span>

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

### <span data-ttu-id="3166c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3166c-135">-ResourceId</span></span>
<span data-ttu-id="3166c-136">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3166c-136">Resource ID.</span></span>

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

### <span data-ttu-id="3166c-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="3166c-137">-Scope</span></span>
<span data-ttu-id="3166c-138">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="3166c-138">Scope of the resource.</span></span> <span data-ttu-id="3166c-139">Például: '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="3166c-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="3166c-140">-Top</span><span class="sxs-lookup"><span data-stu-id="3166c-140">-Top</span></span>
<span data-ttu-id="3166c-141">A vissza nem térhet rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="3166c-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="3166c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3166c-142">CommonParameters</span></span>
<span data-ttu-id="3166c-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3166c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3166c-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3166c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3166c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3166c-145">INPUTS</span></span>

### <span data-ttu-id="3166c-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3166c-146">System.String</span></span>

## <span data-ttu-id="3166c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3166c-147">OUTPUTS</span></span>

### <span data-ttu-id="3166c-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="3166c-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="3166c-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3166c-149">NOTES</span></span>

## <span data-ttu-id="3166c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3166c-150">RELATED LINKS</span></span>
