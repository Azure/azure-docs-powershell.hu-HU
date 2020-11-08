---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012969"
---
# <span data-ttu-id="a8bd7-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a8bd7-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="a8bd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bd7-103">Házirend-hozzárendelést hoz létre, és elindítja a házirend-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="a8bd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8bd7-104">SYNTAX</span></span>

### <span data-ttu-id="a8bd7-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8bd7-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8bd7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8bd7-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8bd7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8bd7-107">DESCRIPTION</span></span>
<span data-ttu-id="a8bd7-108">A **Start-AzPolicyRemediation** parancsmag házirend-hozzárendelést hoz létre egy bizonyos házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="a8bd7-109">Az összes nem megfelelő erőforrást visszaközvetíti a program a Szervizelési hatókörben vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="a8bd7-110">A kármentesítés csak az "deployIfNotExists" befolyással rendelkező házirendek esetében támogatott.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="a8bd7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a8bd7-111">EXAMPLES</span></span>

### <span data-ttu-id="a8bd7-112">Példa 1: szervizelés indítása az előfizetéses hatókörben</span><span class="sxs-lookup"><span data-stu-id="a8bd7-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="a8bd7-113">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="a8bd7-114">2. példa: a Szervizelési csoport hatókörének kezdése választható szűrőkkel</span><span class="sxs-lookup"><span data-stu-id="a8bd7-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="a8bd7-115">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó "mg1" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="a8bd7-116">A program csak a "westus" vagy a "eastus" helyeken lévő erőforrásokat közvetíti.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="a8bd7-117">3. példa: szervizelés kezdése erőforráscsoport hatókörében egy házirend-definíciós hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="a8bd7-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="a8bd7-118">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó "myRG" erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="a8bd7-119">A házirend-hozzárendelés egy házirend-készlet definícióját rendeli hozzá (más néven kezdeményezés).</span><span class="sxs-lookup"><span data-stu-id="a8bd7-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="a8bd7-120">A házirend-definíciós hivatkozási azonosító azt jelzi, hogy a kezdeményezésen belül milyen házirendet kell átirányítani.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="a8bd7-121">Példa 4: kármentesítés indítása, és várakozás a háttérben való befejezésre</span><span class="sxs-lookup"><span data-stu-id="a8bd7-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="a8bd7-122">Ez a parancs új házirend-szervizelést indít el az előfizetésben a megadott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="a8bd7-123">A felszámolás befejezését követően várni fog a kármentesítés befejezésére.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="a8bd7-124">Példa 5: olyan kármentesítés indítása, amely nem megfelelő erőforrásokat fog észlelni a megszüntető előtt</span><span class="sxs-lookup"><span data-stu-id="a8bd7-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="a8bd7-125">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="a8bd7-126">Az előfizetésben szereplő erőforrások megfelelőségi állapotát a program újra kiértékeli a házirend-hozzárendeléssel és a nem megfelelő erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="a8bd7-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8bd7-127">PARAMETERS</span></span>

### <span data-ttu-id="a8bd7-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8bd7-128">-AsJob</span></span>
<span data-ttu-id="a8bd7-129">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a8bd7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bd7-130">-DefaultProfile</span></span>
<span data-ttu-id="a8bd7-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8bd7-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="a8bd7-132">-LocationFilter</span></span>
<span data-ttu-id="a8bd7-133">Az erőforrás-helyek, amelyeket fel kell venni a szervizelésbe.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="a8bd7-134">Az ezeken a helyeken nem található erőforrásokat a program nem fogja újraközvetíteni.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="a8bd7-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bd7-135">-ManagementGroupName</span></span>
<span data-ttu-id="a8bd7-136">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="a8bd7-136">Management group ID.</span></span>

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

### <span data-ttu-id="a8bd7-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8bd7-137">-Name</span></span>
<span data-ttu-id="a8bd7-138">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a8bd7-138">Resource name.</span></span>

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

### <span data-ttu-id="a8bd7-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="a8bd7-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="a8bd7-140">Házirend-hozzárendelés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-140">Policy assignment ID.</span></span>
<span data-ttu-id="a8bd7-141">Pl.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-141">E.g.</span></span>
<span data-ttu-id="a8bd7-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="a8bd7-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="a8bd7-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="a8bd7-144">Beolvassa a házirend-definíciós hivatkozási azonosítót a visszaközvetített egyéni definícióhoz.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="a8bd7-145">Szükséges, ha a házirend-hozzárendeléshez társít egy házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="a8bd7-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="a8bd7-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="a8bd7-147">Ez a cikk azt mutatja be, hogy a kármentesítési tevékenység hogyan fogja feltárni a szervizelésre szorult erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="a8bd7-148">A ReEvaluateCompliance nem támogatott a megszüntető-kezelési csoportok hatókörének használatakor.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="a8bd7-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bd7-149">-ResourceGroupName</span></span>
<span data-ttu-id="a8bd7-150">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-150">Resource group name.</span></span>

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

### <span data-ttu-id="a8bd7-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8bd7-151">-ResourceId</span></span>
<span data-ttu-id="a8bd7-152">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-152">Resource ID.</span></span>

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

### <span data-ttu-id="a8bd7-153">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="a8bd7-153">-Scope</span></span>
<span data-ttu-id="a8bd7-154">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-154">Scope of the resource.</span></span>
<span data-ttu-id="a8bd7-155">Pl.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-155">E.g.</span></span>
<span data-ttu-id="a8bd7-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="a8bd7-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8bd7-157">-Confirm</span></span>
<span data-ttu-id="a8bd7-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8bd7-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8bd7-159">-WhatIf</span></span>
<span data-ttu-id="a8bd7-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8bd7-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8bd7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bd7-162">CommonParameters</span></span>
<span data-ttu-id="a8bd7-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8bd7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bd7-164">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a8bd7-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bd7-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8bd7-165">INPUTS</span></span>

### <span data-ttu-id="a8bd7-166">System. String</span><span class="sxs-lookup"><span data-stu-id="a8bd7-166">System.String</span></span>

### <span data-ttu-id="a8bd7-167">System. string []</span><span class="sxs-lookup"><span data-stu-id="a8bd7-167">System.String[]</span></span>

## <span data-ttu-id="a8bd7-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8bd7-168">OUTPUTS</span></span>

### <span data-ttu-id="a8bd7-169">Microsoft. Azure. Command. PolicyInsights. models. remediáció. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="a8bd7-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a8bd7-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8bd7-170">NOTES</span></span>

## <span data-ttu-id="a8bd7-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8bd7-171">RELATED LINKS</span></span>
