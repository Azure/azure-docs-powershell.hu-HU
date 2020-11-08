---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012973"
---
# <span data-ttu-id="7cbfc-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="7cbfc-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="7cbfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbfc-103">Házirend-kármentesítés törlése</span><span class="sxs-lookup"><span data-stu-id="7cbfc-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="7cbfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cbfc-104">SYNTAX</span></span>

### <span data-ttu-id="7cbfc-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cbfc-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cbfc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cbfc-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cbfc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7cbfc-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cbfc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cbfc-108">DESCRIPTION</span></span>
<span data-ttu-id="7cbfc-109">A **Remove-AzPolicyRemediation** parancsmag törli a házirend-szervizelést.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="7cbfc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7cbfc-110">EXAMPLES</span></span>

### <span data-ttu-id="7cbfc-111">Példa 1: házirend-szervizelés törlése az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="7cbfc-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="7cbfc-112">Ez a parancs törli a "remediation1" nevű kármentesítési tevékenységet a "myRG" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="7cbfc-113">2. példa: a kezelési csoport törlése csővezetéken keresztüli szervizeléssel</span><span class="sxs-lookup"><span data-stu-id="7cbfc-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="7cbfc-114">Ez a parancs törli a "remediation1" nevű szervizelést a "mg1" felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="7cbfc-115">A megerősítést kérő üzenet jelenik meg az erőforrás törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="7cbfc-116">3. példa: házirend-kármentesítés megszüntetése és törlése</span><span class="sxs-lookup"><span data-stu-id="7cbfc-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="7cbfc-117">Ez a parancs törli a "remediation1" nevű kármentesítési tevékenységet a "myRG" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="7cbfc-118">Ha a szervizelés folyamatban van, a program törli a törlés előtt.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="7cbfc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cbfc-119">PARAMETERS</span></span>

### <span data-ttu-id="7cbfc-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="7cbfc-120">-AllowStop</span></span>
<span data-ttu-id="7cbfc-121">Engedélyezze, hogy a szervizelés lemondható legyen, ha az folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="7cbfc-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cbfc-122">-AsJob</span></span>
<span data-ttu-id="7cbfc-123">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7cbfc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbfc-124">-DefaultProfile</span></span>
<span data-ttu-id="7cbfc-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cbfc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cbfc-126">-InputObject</span></span>
<span data-ttu-id="7cbfc-127">A Szervizelési objektum.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbfc-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbfc-128">-ManagementGroupName</span></span>
<span data-ttu-id="7cbfc-129">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="7cbfc-129">Management group ID.</span></span>

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

### <span data-ttu-id="7cbfc-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cbfc-130">-Name</span></span>
<span data-ttu-id="7cbfc-131">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="7cbfc-131">Resource name.</span></span>

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

### <span data-ttu-id="7cbfc-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cbfc-132">-PassThru</span></span>
<span data-ttu-id="7cbfc-133">Igaz érték visszaadása, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="7cbfc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbfc-134">-ResourceGroupName</span></span>
<span data-ttu-id="7cbfc-135">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-135">Resource group name.</span></span>

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

### <span data-ttu-id="7cbfc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cbfc-136">-ResourceId</span></span>
<span data-ttu-id="7cbfc-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-137">Resource ID.</span></span>

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

### <span data-ttu-id="7cbfc-138">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="7cbfc-138">-Scope</span></span>
<span data-ttu-id="7cbfc-139">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-139">Scope of the resource.</span></span>
<span data-ttu-id="7cbfc-140">Pl.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-140">E.g.</span></span>
<span data-ttu-id="7cbfc-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="7cbfc-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cbfc-142">-Confirm</span></span>
<span data-ttu-id="7cbfc-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbfc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbfc-144">-WhatIf</span></span>
<span data-ttu-id="7cbfc-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbfc-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbfc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbfc-147">CommonParameters</span></span>
<span data-ttu-id="7cbfc-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cbfc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbfc-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7cbfc-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbfc-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cbfc-150">INPUTS</span></span>

### <span data-ttu-id="7cbfc-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7cbfc-151">System.String</span></span>

### <span data-ttu-id="7cbfc-152">Microsoft. Azure. Command. PolicyInsights. models. remediáció. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="7cbfc-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="7cbfc-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cbfc-153">OUTPUTS</span></span>

### <span data-ttu-id="7cbfc-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cbfc-154">System.Boolean</span></span>

## <span data-ttu-id="7cbfc-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cbfc-155">NOTES</span></span>

## <span data-ttu-id="7cbfc-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cbfc-156">RELATED LINKS</span></span>
