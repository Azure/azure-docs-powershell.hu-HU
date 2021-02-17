---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208638"
---
# <span data-ttu-id="e830b-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="e830b-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="e830b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e830b-102">SYNOPSIS</span></span>
<span data-ttu-id="e830b-103">Munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="e830b-103">Gets the workspace.</span></span>

## <span data-ttu-id="e830b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e830b-104">SYNTAX</span></span>

### <span data-ttu-id="e830b-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e830b-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e830b-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="e830b-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e830b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e830b-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e830b-108">Lista</span><span class="sxs-lookup"><span data-stu-id="e830b-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e830b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e830b-109">DESCRIPTION</span></span>
<span data-ttu-id="e830b-110">Munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="e830b-110">Gets the workspace.</span></span>

## <span data-ttu-id="e830b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e830b-111">EXAMPLES</span></span>

### <span data-ttu-id="e830b-112">1. példa: Adatforrás-munkaterület létrehozása névvel</span><span class="sxs-lookup"><span data-stu-id="e830b-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="e830b-113">Ez a parancs adatforrás-munkaterületet kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e830b-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="e830b-114">2. példa: Az előfizetés összes Datab workspaces munkaterületének felsorolása</span><span class="sxs-lookup"><span data-stu-id="e830b-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e830b-115">Ez a parancs felsorolja az előfizetés összes Datab workspaces munkaterületét.</span><span class="sxs-lookup"><span data-stu-id="e830b-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="e830b-116">3. példa: Egy erőforráscsoport összes adatkapcsolati munkaterületének felsorolása</span><span class="sxs-lookup"><span data-stu-id="e830b-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e830b-117">Ez a parancs felsorolja az erőforráscsoportok adatkapcsolati munkaterületét.</span><span class="sxs-lookup"><span data-stu-id="e830b-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="e830b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e830b-118">PARAMETERS</span></span>

### <span data-ttu-id="e830b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e830b-119">-DefaultProfile</span></span>
<span data-ttu-id="e830b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e830b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e830b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e830b-121">-InputObject</span></span>
<span data-ttu-id="e830b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e830b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e830b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e830b-123">-Name</span></span>
<span data-ttu-id="e830b-124">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e830b-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e830b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e830b-125">-ResourceGroupName</span></span>
<span data-ttu-id="e830b-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e830b-126">The name of the resource group.</span></span>
<span data-ttu-id="e830b-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e830b-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e830b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e830b-128">-SubscriptionId</span></span>
<span data-ttu-id="e830b-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e830b-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e830b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e830b-130">CommonParameters</span></span>
<span data-ttu-id="e830b-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e830b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e830b-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e830b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e830b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e830b-133">INPUTS</span></span>

### <span data-ttu-id="e830b-134">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.IDatabdatasIdentity</span><span class="sxs-lookup"><span data-stu-id="e830b-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e830b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e830b-135">OUTPUTS</span></span>

### <span data-ttu-id="e830b-136">Microsoft.Azure.PowerShell.Cmdlets.Databszolgáltatásokat.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="e830b-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="e830b-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e830b-137">NOTES</span></span>

<span data-ttu-id="e830b-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e830b-138">ALIASES</span></span>

<span data-ttu-id="e830b-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e830b-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e830b-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e830b-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e830b-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e830b-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e830b-142">INPUTOBJECT: <IDatabricksIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e830b-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e830b-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e830b-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e830b-144">`[PeeringName <String>]`: A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="e830b-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e830b-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e830b-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e830b-146">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e830b-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="e830b-147">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e830b-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e830b-148">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e830b-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e830b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e830b-149">RELATED LINKS</span></span>

