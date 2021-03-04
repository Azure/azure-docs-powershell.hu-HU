---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: 60d679cf8540e39d1be293a46f9e4e441e397627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923721"
---
# <span data-ttu-id="ac992-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="ac992-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="ac992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac992-102">SYNOPSIS</span></span>
<span data-ttu-id="ac992-103">Frissítse a vNet-társviszonyt munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="ac992-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="ac992-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac992-104">SYNTAX</span></span>

### <span data-ttu-id="ac992-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac992-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac992-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac992-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac992-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac992-107">DESCRIPTION</span></span>
<span data-ttu-id="ac992-108">Frissítse a vNet-társviszonyt munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="ac992-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="ac992-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac992-109">EXAMPLES</span></span>

### <span data-ttu-id="ac992-110">1. példa: A vnet-társviszony AllowForwardedTraffic frissítésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ac992-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="ac992-111">Ez a parancs frissíti a vnet-társviszony AllowForwardedTraffic-ját.</span><span class="sxs-lookup"><span data-stu-id="ac992-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="ac992-112">2. példa: A vnet társviszony-létesítés engedélyezéseForwardedTraffic frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="ac992-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="ac992-113">Ez a parancs objektum szerint frissíti az AllowForwardedTraffic vnet társviszonyt.</span><span class="sxs-lookup"><span data-stu-id="ac992-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="ac992-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac992-114">PARAMETERS</span></span>

### <span data-ttu-id="ac992-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="ac992-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="ac992-116">[System.Management.Automation.SwitchParameter] Hogy a helyi virtuális hálózat virtuális hálózatában engedélyezve van-e a virtuális hálózat virtuális gépeiből továbbított forgalom.</span><span class="sxs-lookup"><span data-stu-id="ac992-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="ac992-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="ac992-118">[System.Management.Automation.SwitchParameter] Ha átjáróhivatkozások használhatók távoli virtuális hálózatban a virtuális hálózathoz való csatoláshoz.</span><span class="sxs-lookup"><span data-stu-id="ac992-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ac992-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="ac992-120">[System.Management.Automation.SwitchParameter] Hogy a helyi virtuális hálózati térben lévő virtuális gépek hozzáférhetnek-e a távoli virtuális hálózati térben lévő virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="ac992-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac992-121">-AsJob</span></span>
<span data-ttu-id="ac992-122">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="ac992-122">Run the command as a job</span></span>

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

### <span data-ttu-id="ac992-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac992-123">-DefaultProfile</span></span>
<span data-ttu-id="ac992-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac992-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac992-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac992-125">-InputObject</span></span>
<span data-ttu-id="ac992-126">Identity paraméter.</span><span class="sxs-lookup"><span data-stu-id="ac992-126">Identity parameter.</span></span>
<span data-ttu-id="ac992-127">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="ac992-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ac992-128">-Name</span></span>
<span data-ttu-id="ac992-129">A VNetPeering neve.</span><span class="sxs-lookup"><span data-stu-id="ac992-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac992-130">-NoWait</span></span>
<span data-ttu-id="ac992-131">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="ac992-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac992-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac992-132">-ResourceGroupName</span></span>
<span data-ttu-id="ac992-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac992-133">The name of the resource group.</span></span>
<span data-ttu-id="ac992-134">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ac992-134">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac992-135">-SubscriptionId</span></span>
<span data-ttu-id="ac992-136">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac992-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="ac992-137">-UseRemoteGateway</span></span>
<span data-ttu-id="ac992-138">[System.Management.Automation.SwitchParameter] Ha távoli átjárók is használhatók ezen a virtuális hálózaton.</span><span class="sxs-lookup"><span data-stu-id="ac992-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="ac992-139">Ha a jelölő igazra van állítva, és az allowGatewayTransit távoli társviszonyon is igaz, a virtuális hálózat a távoli virtuális hálózat átjáróit fogja használni az átvitelhez.</span><span class="sxs-lookup"><span data-stu-id="ac992-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="ac992-140">Csak egy társviszonyhoz állíthatja be ezt a jelölőt igazra.</span><span class="sxs-lookup"><span data-stu-id="ac992-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="ac992-141">Ez a jelölő nem beállítható, ha a virtuális hálózatnak már van átjárója.</span><span class="sxs-lookup"><span data-stu-id="ac992-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ac992-142">-WorkspaceName</span></span>
<span data-ttu-id="ac992-143">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="ac992-143">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac992-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac992-144">-Confirm</span></span>
<span data-ttu-id="ac992-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ac992-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac992-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac992-146">-WhatIf</span></span>
<span data-ttu-id="ac992-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ac992-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac992-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac992-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac992-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac992-149">CommonParameters</span></span>
<span data-ttu-id="ac992-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac992-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac992-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac992-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac992-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac992-152">INPUTS</span></span>

### <span data-ttu-id="ac992-153">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.IDatabdatasIdentity</span><span class="sxs-lookup"><span data-stu-id="ac992-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="ac992-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac992-154">OUTPUTS</span></span>

### <span data-ttu-id="ac992-155">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ac992-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="ac992-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac992-156">NOTES</span></span>

<span data-ttu-id="ac992-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ac992-157">ALIASES</span></span>

<span data-ttu-id="ac992-158">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ac992-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac992-159">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ac992-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac992-160">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac992-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac992-161">INPUTOBJECT: <IDatabricksIdentity> Identity paraméter.</span><span class="sxs-lookup"><span data-stu-id="ac992-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="ac992-162">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ac992-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac992-163">`[PeeringName <String>]`: A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="ac992-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="ac992-164">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac992-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ac992-165">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ac992-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="ac992-166">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac992-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ac992-167">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="ac992-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="ac992-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac992-168">RELATED LINKS</span></span>

