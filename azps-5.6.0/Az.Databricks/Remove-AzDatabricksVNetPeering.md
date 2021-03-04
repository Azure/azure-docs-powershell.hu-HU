---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 986bea9de45ea8a628cea8eda4d8a63ec74d46fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932994"
---
# <span data-ttu-id="f1b3d-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="f1b3d-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="f1b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b3d-103">Törli a munkaterületi vNetPeeringet.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="f1b3d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1b3d-104">SYNTAX</span></span>

### <span data-ttu-id="f1b3d-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1b3d-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f1b3d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1b3d-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1b3d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1b3d-107">DESCRIPTION</span></span>
<span data-ttu-id="f1b3d-108">Törli a munkaterületi vNetPeeringet.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="f1b3d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1b3d-109">EXAMPLES</span></span>

### <span data-ttu-id="f1b3d-110">1. példa: Adatkapcsolatok vnet-társviszonyának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="f1b3d-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="f1b3d-111">Ez a parancs eltávolítja az adatkapcsolatok név alapján való társviszonyát.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="f1b3d-112">2. példa: Az adatkapcsolatok vnet-társviszonyának eltávolítása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="f1b3d-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="f1b3d-113">Ez a parancs eltávolítja az adatkapcsolatok vnet-társviszonyát objektum szerint</span><span class="sxs-lookup"><span data-stu-id="f1b3d-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="f1b3d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1b3d-114">PARAMETERS</span></span>

### <span data-ttu-id="f1b3d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1b3d-115">-AsJob</span></span>
<span data-ttu-id="f1b3d-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f1b3d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f1b3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3d-117">-DefaultProfile</span></span>
<span data-ttu-id="f1b3d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1b3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1b3d-119">-InputObject</span></span>
<span data-ttu-id="f1b3d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1b3d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1b3d-121">-Name</span></span>
<span data-ttu-id="f1b3d-122">A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="f1b3d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1b3d-123">-NoWait</span></span>
<span data-ttu-id="f1b3d-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f1b3d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1b3d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1b3d-125">-PassThru</span></span>
<span data-ttu-id="f1b3d-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="f1b3d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f1b3d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b3d-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1b3d-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-128">The name of the resource group.</span></span>
<span data-ttu-id="f1b3d-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f1b3d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f1b3d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1b3d-130">-SubscriptionId</span></span>
<span data-ttu-id="f1b3d-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f1b3d-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1b3d-132">-WorkspaceName</span></span>
<span data-ttu-id="f1b3d-133">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="f1b3d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1b3d-134">-Confirm</span></span>
<span data-ttu-id="f1b3d-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1b3d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b3d-136">-WhatIf</span></span>
<span data-ttu-id="f1b3d-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b3d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1b3d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b3d-139">CommonParameters</span></span>
<span data-ttu-id="f1b3d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b3d-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1b3d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b3d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1b3d-142">INPUTS</span></span>

### <span data-ttu-id="f1b3d-143">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.IDatabdatasIdentity</span><span class="sxs-lookup"><span data-stu-id="f1b3d-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f1b3d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1b3d-144">OUTPUTS</span></span>

### <span data-ttu-id="f1b3d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1b3d-145">System.Boolean</span></span>

## <span data-ttu-id="f1b3d-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1b3d-146">NOTES</span></span>

<span data-ttu-id="f1b3d-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f1b3d-147">ALIASES</span></span>

<span data-ttu-id="f1b3d-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f1b3d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1b3d-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1b3d-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1b3d-151">INPUTOBJECT: <IDatabricksIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f1b3d-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1b3d-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f1b3d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1b3d-153">`[PeeringName <String>]`: A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f1b3d-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f1b3d-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f1b3d-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="f1b3d-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f1b3d-157">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f1b3d-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1b3d-158">RELATED LINKS</span></span>

