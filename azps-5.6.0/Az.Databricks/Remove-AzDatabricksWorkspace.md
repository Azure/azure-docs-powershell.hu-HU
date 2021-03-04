---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: c8e63bd0a6496b1c0ce0899f0e183fb10db32a7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923730"
---
# <span data-ttu-id="aaca3-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="aaca3-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="aaca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaca3-102">SYNOPSIS</span></span>
<span data-ttu-id="aaca3-103">Törli a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="aaca3-103">Deletes the workspace.</span></span>

## <span data-ttu-id="aaca3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aaca3-104">SYNTAX</span></span>

### <span data-ttu-id="aaca3-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aaca3-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aaca3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aaca3-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aaca3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aaca3-107">DESCRIPTION</span></span>
<span data-ttu-id="aaca3-108">Törli a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="aaca3-108">Deletes the workspace.</span></span>

## <span data-ttu-id="aaca3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aaca3-109">EXAMPLES</span></span>

### <span data-ttu-id="aaca3-110">1. példa: Datab workspace eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aaca3-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="aaca3-111">Ez a parancs eltávolítja az Adatkapcsolatok munkaterületet egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="aaca3-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="aaca3-112">2. példa: Datab workspace eltávolítása objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="aaca3-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="aaca3-113">Ez a parancs eltávolítja az Adatkapcsolatok munkaterületet egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="aaca3-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="aaca3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaca3-114">PARAMETERS</span></span>

### <span data-ttu-id="aaca3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaca3-115">-AsJob</span></span>
<span data-ttu-id="aaca3-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="aaca3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aaca3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaca3-117">-DefaultProfile</span></span>
<span data-ttu-id="aaca3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaca3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaca3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaca3-119">-InputObject</span></span>
<span data-ttu-id="aaca3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="aaca3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaca3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="aaca3-121">-Name</span></span>
<span data-ttu-id="aaca3-122">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="aaca3-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaca3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aaca3-123">-NoWait</span></span>
<span data-ttu-id="aaca3-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="aaca3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aaca3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaca3-125">-PassThru</span></span>
<span data-ttu-id="aaca3-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="aaca3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aaca3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaca3-127">-ResourceGroupName</span></span>
<span data-ttu-id="aaca3-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aaca3-128">The name of the resource group.</span></span>
<span data-ttu-id="aaca3-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="aaca3-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaca3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaca3-130">-SubscriptionId</span></span>
<span data-ttu-id="aaca3-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aaca3-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaca3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaca3-132">-Confirm</span></span>
<span data-ttu-id="aaca3-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aaca3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaca3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaca3-134">-WhatIf</span></span>
<span data-ttu-id="aaca3-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aaca3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaca3-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aaca3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaca3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaca3-137">CommonParameters</span></span>
<span data-ttu-id="aaca3-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaca3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaca3-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaca3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaca3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaca3-140">INPUTS</span></span>

### <span data-ttu-id="aaca3-141">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.IDatabdatasIdentity</span><span class="sxs-lookup"><span data-stu-id="aaca3-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="aaca3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaca3-142">OUTPUTS</span></span>

### <span data-ttu-id="aaca3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aaca3-143">System.Boolean</span></span>

## <span data-ttu-id="aaca3-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aaca3-144">NOTES</span></span>

<span data-ttu-id="aaca3-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aaca3-145">ALIASES</span></span>

<span data-ttu-id="aaca3-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="aaca3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aaca3-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="aaca3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaca3-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aaca3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aaca3-149">INPUTOBJECT: <IDatabricksIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="aaca3-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aaca3-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="aaca3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aaca3-151">`[PeeringName <String>]`: A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="aaca3-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="aaca3-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aaca3-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aaca3-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="aaca3-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="aaca3-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aaca3-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="aaca3-155">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="aaca3-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="aaca3-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaca3-156">RELATED LINKS</span></span>

