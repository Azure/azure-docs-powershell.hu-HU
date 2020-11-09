---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297341"
---
# <span data-ttu-id="e3e93-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3e93-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="e3e93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3e93-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e93-103">Megkapja a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="e3e93-103">Gets the workspace.</span></span>

## <span data-ttu-id="e3e93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3e93-104">SYNTAX</span></span>

### <span data-ttu-id="e3e93-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3e93-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3e93-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3e93-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3e93-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3e93-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3e93-108">Lista</span><span class="sxs-lookup"><span data-stu-id="e3e93-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e3e93-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3e93-109">DESCRIPTION</span></span>
<span data-ttu-id="e3e93-110">Megkapja a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="e3e93-110">Gets the workspace.</span></span>

## <span data-ttu-id="e3e93-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e3e93-111">EXAMPLES</span></span>

### <span data-ttu-id="e3e93-112">Példa 1: Databricks-munkaterület beszerzése névvel</span><span class="sxs-lookup"><span data-stu-id="e3e93-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="e3e93-113">Ez a parancs Databricks-munkaterületet kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="e3e93-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="e3e93-114">2. példa: az előfizetésben az összes Databricks-munkaterület listázása</span><span class="sxs-lookup"><span data-stu-id="e3e93-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e3e93-115">Ez a parancs felsorolja az előfizetésben lévő összes Databricks-munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="e3e93-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="e3e93-116">3. példa: egy erőforráscsoport összes Databricks-munkaterületének listázása</span><span class="sxs-lookup"><span data-stu-id="e3e93-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e3e93-117">Ez a parancs felsorolja az erőforráscsoport összes Databricks-munkaterületét.</span><span class="sxs-lookup"><span data-stu-id="e3e93-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="e3e93-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3e93-118">PARAMETERS</span></span>

### <span data-ttu-id="e3e93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e93-119">-DefaultProfile</span></span>
<span data-ttu-id="e3e93-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3e93-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3e93-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3e93-121">-InputObject</span></span>
<span data-ttu-id="e3e93-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e3e93-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3e93-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3e93-123">-Name</span></span>
<span data-ttu-id="e3e93-124">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e3e93-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="e3e93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e93-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3e93-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3e93-126">The name of the resource group.</span></span>
<span data-ttu-id="e3e93-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="e3e93-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e3e93-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3e93-128">-SubscriptionId</span></span>
<span data-ttu-id="e3e93-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e3e93-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e3e93-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e93-130">CommonParameters</span></span>
<span data-ttu-id="e3e93-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3e93-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e93-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e3e93-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e93-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3e93-133">INPUTS</span></span>

### <span data-ttu-id="e3e93-134">Microsoft. Azure. PowerShell. parancsmagok. Databricks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="e3e93-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e3e93-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3e93-135">OUTPUTS</span></span>

### <span data-ttu-id="e3e93-136">Microsoft. Azure. PowerShell. parancsmagok. Databricks. modellek. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3e93-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="e3e93-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3e93-137">NOTES</span></span>

<span data-ttu-id="e3e93-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e3e93-138">ALIASES</span></span>

<span data-ttu-id="e3e93-139">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e3e93-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3e93-140">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e3e93-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3e93-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e3e93-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3e93-142">INPUTOBJECT <IDatabricksIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e3e93-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3e93-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e3e93-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3e93-144">`[PeeringName <String>]`: A munkaterület vNete.</span><span class="sxs-lookup"><span data-stu-id="e3e93-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e3e93-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3e93-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e3e93-146">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="e3e93-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="e3e93-147">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e3e93-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e3e93-148">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e3e93-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e3e93-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3e93-149">RELATED LINKS</span></span>

