---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: aeb86609e06417147f5ef4600c430665f28da454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937482"
---
# <span data-ttu-id="d35ec-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d35ec-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="d35ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d35ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d35ec-103">Házirend-hozzárendeléshez létrehoz és elindít egy házirend-szervizelést.</span><span class="sxs-lookup"><span data-stu-id="d35ec-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="d35ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d35ec-104">SYNTAX</span></span>

### <span data-ttu-id="d35ec-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d35ec-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d35ec-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d35ec-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d35ec-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d35ec-107">DESCRIPTION</span></span>
<span data-ttu-id="d35ec-108">A **Start-AzPolicyRemediation** parancsmag létrehoz egy házirend-szervizelést egy adott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="d35ec-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="d35ec-109">A szervizelés hatókörében vagy alatt található, nem megfelelő erőforrásokat orvosolni fogjuk.</span><span class="sxs-lookup"><span data-stu-id="d35ec-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="d35ec-110">A szervizelés csak a "deployIfNotExists" effektusú házirendek esetén támogatott.</span><span class="sxs-lookup"><span data-stu-id="d35ec-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="d35ec-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d35ec-111">EXAMPLES</span></span>

### <span data-ttu-id="d35ec-112">1. példa: Szervizelés az előfizetés hatókörében</span><span class="sxs-lookup"><span data-stu-id="d35ec-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="d35ec-113">Ez a parancs új házirend-szervizelést hoz létre az előfizetés "Saját előfizetés" szolgáltatásában az adott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="d35ec-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="d35ec-114">2. példa: Szervizelés kezdése a felügyeleti csoport hatókörében opcionális szűrőkkel</span><span class="sxs-lookup"><span data-stu-id="d35ec-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="d35ec-115">Ez a parancs új házirend-szervizelést hoz létre a "1" felügyeleti csoportban az adott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="d35ec-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="d35ec-116">Csak a "westus" vagy "eastus" helyeken található erőforrások lesznek szervizbe stb.</span><span class="sxs-lookup"><span data-stu-id="d35ec-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="d35ec-117">3. példa: Szervizelés kezdése az erőforráscsoport hatókörében egy házirendkészlet-definíciós hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="d35ec-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="d35ec-118">Ez a parancs új házirend-szervizelést hoz létre a "myRG" erőforráscsoportban az adott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="d35ec-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="d35ec-119">A házirend-hozzárendelés hozzárendel egy házirendkészlet-definíciót (más néven kezdeményezést).</span><span class="sxs-lookup"><span data-stu-id="d35ec-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="d35ec-120">A házirenddefiníciós hivatkozásazonosító azt jelzi, hogy a kezdeményezésen belül melyik házirendet kell orvosolni.</span><span class="sxs-lookup"><span data-stu-id="d35ec-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="d35ec-121">4. példa: Szervizelés kezdése és várakozás a háttérben</span><span class="sxs-lookup"><span data-stu-id="d35ec-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="d35ec-122">Ez a parancs új házirend-szervizelést kezd az előfizetés "Saját előfizetés" szolgáltatásában az adott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="d35ec-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="d35ec-123">A végleges szervizelési állapot visszaadása előtt megvárja, amíg befejeződik a szervizelés.</span><span class="sxs-lookup"><span data-stu-id="d35ec-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="d35ec-124">5. példa: Szervizelést kell kezdeni, amely felderíti a nem megfelelő erőforrásokat a szervizelés előtt.</span><span class="sxs-lookup"><span data-stu-id="d35ec-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="d35ec-125">Ez a parancs új házirend-szervizelést hoz létre az előfizetés "Saját előfizetés" szolgáltatásában az adott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="d35ec-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="d35ec-126">Az előfizetésben a megfelelőségi állapot az erőforrásokat újra kiértékeli a házirend-hozzárendelés alapján, és a nem megfelelő erőforrásokat orvosolni fogjuk.</span><span class="sxs-lookup"><span data-stu-id="d35ec-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="d35ec-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d35ec-127">PARAMETERS</span></span>

### <span data-ttu-id="d35ec-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d35ec-128">-AsJob</span></span>
<span data-ttu-id="d35ec-129">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="d35ec-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d35ec-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d35ec-130">-DefaultProfile</span></span>
<span data-ttu-id="d35ec-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d35ec-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d35ec-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="d35ec-132">-LocationFilter</span></span>
<span data-ttu-id="d35ec-133">A szervizelésben szerepelve szereplő erőforráshelyek.</span><span class="sxs-lookup"><span data-stu-id="d35ec-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="d35ec-134">Azok az erőforrások, amelyek nem ezeken a helyeken találhatók, nem lesznek szervizbe 100 000 000 000 között.</span><span class="sxs-lookup"><span data-stu-id="d35ec-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d35ec-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d35ec-135">-ManagementGroupName</span></span>
<span data-ttu-id="d35ec-136">Felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d35ec-136">Management group ID.</span></span>

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

### <span data-ttu-id="d35ec-137">-Name</span><span class="sxs-lookup"><span data-stu-id="d35ec-137">-Name</span></span>
<span data-ttu-id="d35ec-138">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d35ec-138">Resource name.</span></span>

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

### <span data-ttu-id="d35ec-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="d35ec-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="d35ec-140">Házirend-hozzárendelés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d35ec-140">Policy assignment ID.</span></span>
<span data-ttu-id="d35ec-141">Például:</span><span class="sxs-lookup"><span data-stu-id="d35ec-141">E.g.</span></span>
<span data-ttu-id="d35ec-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="d35ec-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d35ec-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="d35ec-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="d35ec-144">Annak az egyéni definíciónak a házirenddefiníciós hivatkozásazonosítóját kapja meg, amely szervizben van.</span><span class="sxs-lookup"><span data-stu-id="d35ec-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="d35ec-145">Akkor szükséges, amikor a házirend-hozzárendelés hozzárendel egy házirendkészlet-definíciót.</span><span class="sxs-lookup"><span data-stu-id="d35ec-145">Required when the policy assignment assigns a policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d35ec-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="d35ec-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="d35ec-147">Ez a cikk bemutatja, hogy a szervizelési tevékenység hogyan fogja felderíti a szervizelésre szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="d35ec-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="d35ec-148">A felügyeleti csoportok hatókörének szervizelhetővé tevében a ReEvaluateCompliance nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="d35ec-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d35ec-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d35ec-149">-ResourceGroupName</span></span>
<span data-ttu-id="d35ec-150">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d35ec-150">Resource group name.</span></span>

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

### <span data-ttu-id="d35ec-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d35ec-151">-ResourceId</span></span>
<span data-ttu-id="d35ec-152">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d35ec-152">Resource ID.</span></span>

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

### <span data-ttu-id="d35ec-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="d35ec-153">-Scope</span></span>
<span data-ttu-id="d35ec-154">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="d35ec-154">Scope of the resource.</span></span>
<span data-ttu-id="d35ec-155">Például:</span><span class="sxs-lookup"><span data-stu-id="d35ec-155">E.g.</span></span>
<span data-ttu-id="d35ec-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="d35ec-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="d35ec-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d35ec-157">-Confirm</span></span>
<span data-ttu-id="d35ec-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d35ec-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35ec-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d35ec-159">-WhatIf</span></span>
<span data-ttu-id="d35ec-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d35ec-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d35ec-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d35ec-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35ec-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35ec-162">CommonParameters</span></span>
<span data-ttu-id="d35ec-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d35ec-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35ec-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d35ec-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35ec-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d35ec-165">INPUTS</span></span>

### <span data-ttu-id="d35ec-166">System.String</span><span class="sxs-lookup"><span data-stu-id="d35ec-166">System.String</span></span>

### <span data-ttu-id="d35ec-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d35ec-167">System.String[]</span></span>

## <span data-ttu-id="d35ec-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d35ec-168">OUTPUTS</span></span>

### <span data-ttu-id="d35ec-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="d35ec-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="d35ec-170">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d35ec-170">NOTES</span></span>

## <span data-ttu-id="d35ec-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d35ec-171">RELATED LINKS</span></span>
