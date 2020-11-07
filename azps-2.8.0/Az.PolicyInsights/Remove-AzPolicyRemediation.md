---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 96afdd5e0bdf336dec5f2ff1b2a9ecfccf8bac12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838398"
---
# <span data-ttu-id="4fb77-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4fb77-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="4fb77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fb77-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb77-103">Házirend-kármentesítés törlése</span><span class="sxs-lookup"><span data-stu-id="4fb77-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="4fb77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fb77-104">SYNTAX</span></span>

### <span data-ttu-id="4fb77-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fb77-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb77-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fb77-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb77-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4fb77-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb77-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fb77-108">DESCRIPTION</span></span>
<span data-ttu-id="4fb77-109">A **Remove-AzPolicyRemediation** parancsmag törli a házirend-szervizelést.</span><span class="sxs-lookup"><span data-stu-id="4fb77-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="4fb77-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4fb77-110">EXAMPLES</span></span>

### <span data-ttu-id="4fb77-111">Példa 1: házirend-szervizelés törlése az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="4fb77-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="4fb77-112">Ez a parancs törli a "remediation1" nevű kármentesítési tevékenységet a "myRG" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="4fb77-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="4fb77-113">2. példa: a kezelési csoport törlése csővezetéken keresztüli szervizeléssel</span><span class="sxs-lookup"><span data-stu-id="4fb77-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="4fb77-114">Ez a parancs törli a "remediation1" nevű szervizelést a "mg1" felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="4fb77-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="4fb77-115">A megerősítést kérő üzenet jelenik meg az erőforrás törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="4fb77-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="4fb77-116">3. példa: házirend-kármentesítés megszüntetése és törlése</span><span class="sxs-lookup"><span data-stu-id="4fb77-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="4fb77-117">Ez a parancs törli a "remediation1" nevű kármentesítési tevékenységet a "myRG" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="4fb77-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="4fb77-118">Ha a szervizelés folyamatban van, a program törli a törlés előtt.</span><span class="sxs-lookup"><span data-stu-id="4fb77-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="4fb77-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fb77-119">PARAMETERS</span></span>

### <span data-ttu-id="4fb77-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="4fb77-120">-AllowStop</span></span>
<span data-ttu-id="4fb77-121">Engedélyezze, hogy a szervizelés lemondható legyen, ha az folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="4fb77-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="4fb77-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fb77-122">-AsJob</span></span>
<span data-ttu-id="4fb77-123">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="4fb77-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4fb77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb77-124">-DefaultProfile</span></span>
<span data-ttu-id="4fb77-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fb77-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb77-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fb77-126">-InputObject</span></span>
<span data-ttu-id="4fb77-127">A Szervizelési objektum.</span><span class="sxs-lookup"><span data-stu-id="4fb77-127">The Remediation object.</span></span>

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

### <span data-ttu-id="4fb77-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb77-128">-ManagementGroupName</span></span>
<span data-ttu-id="4fb77-129">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="4fb77-129">Management group ID.</span></span>

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

### <span data-ttu-id="4fb77-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fb77-130">-Name</span></span>
<span data-ttu-id="4fb77-131">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4fb77-131">Resource name.</span></span>

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

### <span data-ttu-id="4fb77-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fb77-132">-PassThru</span></span>
<span data-ttu-id="4fb77-133">Igaz érték visszaadása, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="4fb77-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="4fb77-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb77-134">-ResourceGroupName</span></span>
<span data-ttu-id="4fb77-135">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4fb77-135">Resource group name.</span></span>

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

### <span data-ttu-id="4fb77-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fb77-136">-ResourceId</span></span>
<span data-ttu-id="4fb77-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4fb77-137">Resource ID.</span></span>

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

### <span data-ttu-id="4fb77-138">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="4fb77-138">-Scope</span></span>
<span data-ttu-id="4fb77-139">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="4fb77-139">Scope of the resource.</span></span>
<span data-ttu-id="4fb77-140">Pl.</span><span class="sxs-lookup"><span data-stu-id="4fb77-140">E.g.</span></span>
<span data-ttu-id="4fb77-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="4fb77-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="4fb77-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fb77-142">-Confirm</span></span>
<span data-ttu-id="4fb77-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fb77-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb77-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb77-144">-WhatIf</span></span>
<span data-ttu-id="4fb77-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fb77-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fb77-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fb77-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb77-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb77-147">CommonParameters</span></span>
<span data-ttu-id="4fb77-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fb77-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb77-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb77-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb77-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb77-150">INPUTS</span></span>

### <span data-ttu-id="4fb77-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4fb77-151">System.String</span></span>

### <span data-ttu-id="4fb77-152">Microsoft. Azure. Command. PolicyInsights. models. remediáció. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="4fb77-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="4fb77-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb77-153">OUTPUTS</span></span>

### <span data-ttu-id="4fb77-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fb77-154">System.Boolean</span></span>

## <span data-ttu-id="4fb77-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fb77-155">NOTES</span></span>

## <span data-ttu-id="4fb77-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fb77-156">RELATED LINKS</span></span>
