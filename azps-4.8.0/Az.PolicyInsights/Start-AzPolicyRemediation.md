---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184711"
---
# <span data-ttu-id="c8358-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="c8358-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="c8358-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8358-102">SYNOPSIS</span></span>
<span data-ttu-id="c8358-103">Házirend-hozzárendelést hoz létre, és elindítja a házirend-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="c8358-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="c8358-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8358-104">SYNTAX</span></span>

### <span data-ttu-id="c8358-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8358-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8358-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c8358-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8358-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8358-107">DESCRIPTION</span></span>
<span data-ttu-id="c8358-108">A **Start-AzPolicyRemediation** parancsmag házirend-hozzárendelést hoz létre egy bizonyos házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="c8358-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="c8358-109">Az összes nem megfelelő erőforrást visszaközvetíti a program a Szervizelési hatókörben vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="c8358-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="c8358-110">A kármentesítés csak az "deployIfNotExists" befolyással rendelkező házirendek esetében támogatott.</span><span class="sxs-lookup"><span data-stu-id="c8358-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="c8358-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c8358-111">EXAMPLES</span></span>

### <span data-ttu-id="c8358-112">Példa 1: szervizelés indítása az előfizetéses hatókörben</span><span class="sxs-lookup"><span data-stu-id="c8358-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="c8358-113">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="c8358-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="c8358-114">2. példa: a Szervizelési csoport hatókörének kezdése választható szűrőkkel</span><span class="sxs-lookup"><span data-stu-id="c8358-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="c8358-115">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó "mg1" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="c8358-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="c8358-116">A program csak a "westus" vagy a "eastus" helyeken lévő erőforrásokat közvetíti.</span><span class="sxs-lookup"><span data-stu-id="c8358-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="c8358-117">3. példa: szervizelés kezdése erőforráscsoport hatókörében egy házirend-definíciós hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="c8358-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="c8358-118">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó "myRG" erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="c8358-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="c8358-119">A házirend-hozzárendelés egy házirend-készlet definícióját rendeli hozzá (más néven kezdeményezés).</span><span class="sxs-lookup"><span data-stu-id="c8358-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="c8358-120">A házirend-definíciós hivatkozási azonosító azt jelzi, hogy a kezdeményezésen belül milyen házirendet kell átirányítani.</span><span class="sxs-lookup"><span data-stu-id="c8358-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="c8358-121">Példa 4: kármentesítés indítása, és várakozás a háttérben való befejezésre</span><span class="sxs-lookup"><span data-stu-id="c8358-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="c8358-122">Ez a parancs új házirend-szervizelést indít el az előfizetésben a megadott házirend-hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="c8358-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="c8358-123">A felszámolás befejezését követően várni fog a kármentesítés befejezésére.</span><span class="sxs-lookup"><span data-stu-id="c8358-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="c8358-124">Példa 5: olyan kármentesítés indítása, amely nem megfelelő erőforrásokat fog észlelni a megszüntető előtt</span><span class="sxs-lookup"><span data-stu-id="c8358-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="c8358-125">Ez a parancs új házirend-szervizelést hoz létre a megadott házirend-hozzárendeléshez tartozó előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="c8358-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="c8358-126">Az előfizetésben szereplő erőforrások megfelelőségi állapotát a program újra kiértékeli a házirend-hozzárendeléssel és a nem megfelelő erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="c8358-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="c8358-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8358-127">PARAMETERS</span></span>

### <span data-ttu-id="c8358-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8358-128">-AsJob</span></span>
<span data-ttu-id="c8358-129">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="c8358-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c8358-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8358-130">-DefaultProfile</span></span>
<span data-ttu-id="c8358-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8358-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8358-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="c8358-132">-LocationFilter</span></span>
<span data-ttu-id="c8358-133">Az erőforrás-helyek, amelyeket fel kell venni a szervizelésbe.</span><span class="sxs-lookup"><span data-stu-id="c8358-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="c8358-134">Az ezeken a helyeken nem található erőforrásokat a program nem fogja újraközvetíteni.</span><span class="sxs-lookup"><span data-stu-id="c8358-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="c8358-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c8358-135">-ManagementGroupName</span></span>
<span data-ttu-id="c8358-136">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="c8358-136">Management group ID.</span></span>

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

### <span data-ttu-id="c8358-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8358-137">-Name</span></span>
<span data-ttu-id="c8358-138">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="c8358-138">Resource name.</span></span>

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

### <span data-ttu-id="c8358-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="c8358-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="c8358-140">Házirend-hozzárendelés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c8358-140">Policy assignment ID.</span></span>
<span data-ttu-id="c8358-141">Pl.</span><span class="sxs-lookup"><span data-stu-id="c8358-141">E.g.</span></span>
<span data-ttu-id="c8358-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="c8358-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="c8358-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="c8358-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="c8358-144">Beolvassa a házirend-definíciós hivatkozási azonosítót a visszaközvetített egyéni definícióhoz.</span><span class="sxs-lookup"><span data-stu-id="c8358-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="c8358-145">Szükséges, ha a házirend-hozzárendeléshez társít egy házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="c8358-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="c8358-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="c8358-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="c8358-147">Ez a cikk azt mutatja be, hogy a kármentesítési tevékenység hogyan fogja feltárni a szervizelésre szorult erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="c8358-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="c8358-148">A ReEvaluateCompliance nem támogatott a megszüntető-kezelési csoportok hatókörének használatakor.</span><span class="sxs-lookup"><span data-stu-id="c8358-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="c8358-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8358-149">-ResourceGroupName</span></span>
<span data-ttu-id="c8358-150">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c8358-150">Resource group name.</span></span>

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

### <span data-ttu-id="c8358-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8358-151">-ResourceId</span></span>
<span data-ttu-id="c8358-152">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c8358-152">Resource ID.</span></span>

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

### <span data-ttu-id="c8358-153">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="c8358-153">-Scope</span></span>
<span data-ttu-id="c8358-154">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="c8358-154">Scope of the resource.</span></span>
<span data-ttu-id="c8358-155">Pl.</span><span class="sxs-lookup"><span data-stu-id="c8358-155">E.g.</span></span>
<span data-ttu-id="c8358-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="c8358-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="c8358-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8358-157">-Confirm</span></span>
<span data-ttu-id="c8358-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8358-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8358-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8358-159">-WhatIf</span></span>
<span data-ttu-id="c8358-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8358-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8358-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8358-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8358-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8358-162">CommonParameters</span></span>
<span data-ttu-id="c8358-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8358-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8358-164">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8358-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8358-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8358-165">INPUTS</span></span>

### <span data-ttu-id="c8358-166">System. String</span><span class="sxs-lookup"><span data-stu-id="c8358-166">System.String</span></span>

### <span data-ttu-id="c8358-167">System. string []</span><span class="sxs-lookup"><span data-stu-id="c8358-167">System.String[]</span></span>

## <span data-ttu-id="c8358-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8358-168">OUTPUTS</span></span>

### <span data-ttu-id="c8358-169">Microsoft. Azure. Command. PolicyInsights. models. remediáció. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="c8358-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="c8358-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8358-170">NOTES</span></span>

## <span data-ttu-id="c8358-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8358-171">RELATED LINKS</span></span>
