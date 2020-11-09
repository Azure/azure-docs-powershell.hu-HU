---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297305"
---
# <span data-ttu-id="985ca-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="985ca-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="985ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="985ca-102">SYNOPSIS</span></span>
<span data-ttu-id="985ca-103">Törli a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="985ca-103">Deletes the workspace.</span></span>

## <span data-ttu-id="985ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="985ca-104">SYNTAX</span></span>

### <span data-ttu-id="985ca-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="985ca-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="985ca-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="985ca-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="985ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="985ca-107">DESCRIPTION</span></span>
<span data-ttu-id="985ca-108">Törli a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="985ca-108">Deletes the workspace.</span></span>

## <span data-ttu-id="985ca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="985ca-109">EXAMPLES</span></span>

### <span data-ttu-id="985ca-110">1. példa: Databricks-munkaterület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="985ca-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="985ca-111">Ez a parancs eltávolítja a Databricks-munkaterületet egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="985ca-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="985ca-112">2. példa: Databricks-munkaterület eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="985ca-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="985ca-113">Ez a parancs eltávolítja a Databricks-munkaterületet egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="985ca-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="985ca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="985ca-114">PARAMETERS</span></span>

### <span data-ttu-id="985ca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="985ca-115">-AsJob</span></span>
<span data-ttu-id="985ca-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="985ca-116">Run the command as a job</span></span>

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

### <span data-ttu-id="985ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985ca-117">-DefaultProfile</span></span>
<span data-ttu-id="985ca-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="985ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="985ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="985ca-119">-InputObject</span></span>
<span data-ttu-id="985ca-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="985ca-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="985ca-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="985ca-121">-Name</span></span>
<span data-ttu-id="985ca-122">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="985ca-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="985ca-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="985ca-123">-NoWait</span></span>
<span data-ttu-id="985ca-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="985ca-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="985ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="985ca-125">-PassThru</span></span>
<span data-ttu-id="985ca-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="985ca-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="985ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="985ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="985ca-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="985ca-128">The name of the resource group.</span></span>
<span data-ttu-id="985ca-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="985ca-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="985ca-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="985ca-130">-SubscriptionId</span></span>
<span data-ttu-id="985ca-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="985ca-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="985ca-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="985ca-132">-Confirm</span></span>
<span data-ttu-id="985ca-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="985ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="985ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="985ca-134">-WhatIf</span></span>
<span data-ttu-id="985ca-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="985ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="985ca-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="985ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="985ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985ca-137">CommonParameters</span></span>
<span data-ttu-id="985ca-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="985ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985ca-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="985ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985ca-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="985ca-140">INPUTS</span></span>

### <span data-ttu-id="985ca-141">Microsoft. Azure. PowerShell. parancsmagok. Databricks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="985ca-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="985ca-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="985ca-142">OUTPUTS</span></span>

### <span data-ttu-id="985ca-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="985ca-143">System.Boolean</span></span>

## <span data-ttu-id="985ca-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="985ca-144">NOTES</span></span>

<span data-ttu-id="985ca-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="985ca-145">ALIASES</span></span>

<span data-ttu-id="985ca-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="985ca-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="985ca-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="985ca-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="985ca-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="985ca-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="985ca-149">INPUTOBJECT <IDatabricksIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="985ca-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="985ca-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="985ca-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="985ca-151">`[PeeringName <String>]`: A munkaterület vNete.</span><span class="sxs-lookup"><span data-stu-id="985ca-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="985ca-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="985ca-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="985ca-153">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="985ca-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="985ca-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="985ca-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="985ca-155">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="985ca-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="985ca-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="985ca-156">RELATED LINKS</span></span>

