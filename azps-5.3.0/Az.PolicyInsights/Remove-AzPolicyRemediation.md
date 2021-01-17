---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481036"
---
# <span data-ttu-id="875c2-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="875c2-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="875c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="875c2-102">SYNOPSIS</span></span>
<span data-ttu-id="875c2-103">Törli a házirend-szervizelést.</span><span class="sxs-lookup"><span data-stu-id="875c2-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="875c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="875c2-104">SYNTAX</span></span>

### <span data-ttu-id="875c2-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="875c2-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="875c2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="875c2-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="875c2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="875c2-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="875c2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="875c2-108">DESCRIPTION</span></span>
<span data-ttu-id="875c2-109">A **Remove-AzPolicyRemediation** parancsmag törli a házirend-szervizelést.</span><span class="sxs-lookup"><span data-stu-id="875c2-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="875c2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="875c2-110">EXAMPLES</span></span>

### <span data-ttu-id="875c2-111">1. példa: Házirend-szerviz törlése az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="875c2-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="875c2-112">Ez a parancs törli a "szervizelés1" nevű szervizelést a "myRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="875c2-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="875c2-113">2. példa: Felügyeleti csoport szervizelésének törlése pipával</span><span class="sxs-lookup"><span data-stu-id="875c2-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="875c2-114">Ez a parancs törli a "remediation1" nevű szervizelést a "1" felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="875c2-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="875c2-115">Az erőforrás törlése előtt megjelenik egy megerősítési üzenet.</span><span class="sxs-lookup"><span data-stu-id="875c2-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="875c2-116">3. példa: Házirend-szervizelés megszakítása és törlése</span><span class="sxs-lookup"><span data-stu-id="875c2-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="875c2-117">Ez a parancs törli a "szervizelés1" nevű szervizelést a "myRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="875c2-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="875c2-118">Ha a szervizelés folyamatban van, a törlés előtt a rendszer törli azt.</span><span class="sxs-lookup"><span data-stu-id="875c2-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="875c2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="875c2-119">PARAMETERS</span></span>

### <span data-ttu-id="875c2-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="875c2-120">-AllowStop</span></span>
<span data-ttu-id="875c2-121">A szervizelés megszakításának engedélyezése folyamatban lévő gombra való áttűnés esetén.</span><span class="sxs-lookup"><span data-stu-id="875c2-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="875c2-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="875c2-122">-AsJob</span></span>
<span data-ttu-id="875c2-123">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="875c2-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="875c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875c2-124">-DefaultProfile</span></span>
<span data-ttu-id="875c2-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="875c2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="875c2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="875c2-126">-InputObject</span></span>
<span data-ttu-id="875c2-127">A Szervizelés objektum.</span><span class="sxs-lookup"><span data-stu-id="875c2-127">The Remediation object.</span></span>

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

### <span data-ttu-id="875c2-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="875c2-128">-ManagementGroupName</span></span>
<span data-ttu-id="875c2-129">Felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="875c2-129">Management group ID.</span></span>

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

### <span data-ttu-id="875c2-130">-Name</span><span class="sxs-lookup"><span data-stu-id="875c2-130">-Name</span></span>
<span data-ttu-id="875c2-131">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="875c2-131">Resource name.</span></span>

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

### <span data-ttu-id="875c2-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="875c2-132">-PassThru</span></span>
<span data-ttu-id="875c2-133">Igaz érték visszaadva, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="875c2-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="875c2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="875c2-134">-ResourceGroupName</span></span>
<span data-ttu-id="875c2-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="875c2-135">Resource group name.</span></span>

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

### <span data-ttu-id="875c2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="875c2-136">-ResourceId</span></span>
<span data-ttu-id="875c2-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="875c2-137">Resource ID.</span></span>

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

### <span data-ttu-id="875c2-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="875c2-138">-Scope</span></span>
<span data-ttu-id="875c2-139">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="875c2-139">Scope of the resource.</span></span>
<span data-ttu-id="875c2-140">Például:</span><span class="sxs-lookup"><span data-stu-id="875c2-140">E.g.</span></span>
<span data-ttu-id="875c2-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="875c2-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="875c2-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="875c2-142">-Confirm</span></span>
<span data-ttu-id="875c2-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="875c2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="875c2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="875c2-144">-WhatIf</span></span>
<span data-ttu-id="875c2-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="875c2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="875c2-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="875c2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="875c2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875c2-147">CommonParameters</span></span>
<span data-ttu-id="875c2-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="875c2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875c2-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="875c2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875c2-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="875c2-150">INPUTS</span></span>

### <span data-ttu-id="875c2-151">System.String</span><span class="sxs-lookup"><span data-stu-id="875c2-151">System.String</span></span>

### <span data-ttu-id="875c2-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="875c2-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="875c2-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="875c2-153">OUTPUTS</span></span>

### <span data-ttu-id="875c2-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="875c2-154">System.Boolean</span></span>

## <span data-ttu-id="875c2-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="875c2-155">NOTES</span></span>

## <span data-ttu-id="875c2-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="875c2-156">RELATED LINKS</span></span>
