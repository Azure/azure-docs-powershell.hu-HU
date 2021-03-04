---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: a5654fa0974accf4319df4cbbd08ef220fa7ad9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925850"
---
# <span data-ttu-id="486e1-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="486e1-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="486e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="486e1-102">SYNOPSIS</span></span>
<span data-ttu-id="486e1-103">A munkaterületi vNet-társviszonyt kapja.</span><span class="sxs-lookup"><span data-stu-id="486e1-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="486e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="486e1-104">SYNTAX</span></span>

### <span data-ttu-id="486e1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="486e1-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="486e1-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="486e1-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="486e1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="486e1-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="486e1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="486e1-108">DESCRIPTION</span></span>
<span data-ttu-id="486e1-109">A munkaterületi vNet-társviszonyt kapja.</span><span class="sxs-lookup"><span data-stu-id="486e1-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="486e1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="486e1-110">EXAMPLES</span></span>

### <span data-ttu-id="486e1-111">1. példa: List all vnet peering under a datab</span><span class="sxs-lookup"><span data-stu-id="486e1-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="486e1-112">Ez a parancs felsorolja az adatkapcsolatok alatt található összes vnet-társviszonyt.</span><span class="sxs-lookup"><span data-stu-id="486e1-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="486e1-113">2. példa: Virtuális hálózat társviszonyának lekérte</span><span class="sxs-lookup"><span data-stu-id="486e1-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="486e1-114">Ez a parancs vnet-társviszonyt kap.</span><span class="sxs-lookup"><span data-stu-id="486e1-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="486e1-115">3. példa: Vnet-társviszony-létesítés objektum alapján</span><span class="sxs-lookup"><span data-stu-id="486e1-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="486e1-116">Ez a parancs egy vnet-társviszonyt kap objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="486e1-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="486e1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="486e1-117">PARAMETERS</span></span>

### <span data-ttu-id="486e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486e1-118">-DefaultProfile</span></span>
<span data-ttu-id="486e1-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="486e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="486e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="486e1-120">-InputObject</span></span>
<span data-ttu-id="486e1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="486e1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="486e1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="486e1-122">-Name</span></span>
<span data-ttu-id="486e1-123">A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="486e1-123">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486e1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="486e1-124">-PassThru</span></span>
<span data-ttu-id="486e1-125">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="486e1-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="486e1-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="486e1-127">The name of the resource group.</span></span>
<span data-ttu-id="486e1-128">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="486e1-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="486e1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="486e1-129">-SubscriptionId</span></span>
<span data-ttu-id="486e1-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="486e1-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486e1-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="486e1-131">-WorkspaceName</span></span>
<span data-ttu-id="486e1-132">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="486e1-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="486e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486e1-133">CommonParameters</span></span>
<span data-ttu-id="486e1-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486e1-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="486e1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486e1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="486e1-136">INPUTS</span></span>

### <span data-ttu-id="486e1-137">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.IDatabdatasIdentity</span><span class="sxs-lookup"><span data-stu-id="486e1-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="486e1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="486e1-138">OUTPUTS</span></span>

### <span data-ttu-id="486e1-139">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="486e1-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="486e1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="486e1-140">NOTES</span></span>

<span data-ttu-id="486e1-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="486e1-141">ALIASES</span></span>

<span data-ttu-id="486e1-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="486e1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="486e1-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="486e1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="486e1-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="486e1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="486e1-145">INPUTOBJECT: <IDatabricksIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="486e1-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="486e1-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="486e1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="486e1-147">`[PeeringName <String>]`: A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="486e1-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="486e1-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="486e1-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="486e1-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="486e1-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="486e1-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="486e1-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="486e1-151">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="486e1-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="486e1-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="486e1-152">RELATED LINKS</span></span>

