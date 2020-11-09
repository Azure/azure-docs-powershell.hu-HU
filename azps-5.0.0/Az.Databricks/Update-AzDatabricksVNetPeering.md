---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297302"
---
# <span data-ttu-id="fbb55-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="fbb55-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="fbb55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbb55-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb55-103">VNet frissítése a munkaterületre.</span><span class="sxs-lookup"><span data-stu-id="fbb55-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="fbb55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbb55-104">SYNTAX</span></span>

### <span data-ttu-id="fbb55-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbb55-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fbb55-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fbb55-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbb55-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbb55-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb55-108">VNet frissítése a munkaterületre.</span><span class="sxs-lookup"><span data-stu-id="fbb55-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="fbb55-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fbb55-109">EXAMPLES</span></span>

### <span data-ttu-id="fbb55-110">Példa 1: a vnet AllowForwardedTraffic frissítése</span><span class="sxs-lookup"><span data-stu-id="fbb55-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="fbb55-111">Ez a parancs frissíti a vnet-AllowForwardedTraffic.</span><span class="sxs-lookup"><span data-stu-id="fbb55-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="fbb55-112">2. példa: a vnet AllowForwardedTraffic frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="fbb55-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="fbb55-113">Ez a parancs frissíti az objektum AllowForwardedTraffic vnet.</span><span class="sxs-lookup"><span data-stu-id="fbb55-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="fbb55-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbb55-114">PARAMETERS</span></span>

### <span data-ttu-id="fbb55-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="fbb55-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="fbb55-116">[System. Management. Automation. SwitchParameter] azt, hogy a virtuális magánhálózaton a virtuális forgalomból érkező forgalmat a helyi virtuális hálózatban engedélyezi/letiltja-e a távoli virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="fbb55-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="fbb55-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="fbb55-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="fbb55-118">[System. Management. Automation. SwitchParameter] Ha az átjáró hivatkozásait a távoli virtuális hálózatban is használhatja, a virtuális hálózatra mutató hivatkozással.</span><span class="sxs-lookup"><span data-stu-id="fbb55-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="fbb55-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="fbb55-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="fbb55-120">[System. Management. Automation. SwitchParameter] azt, hogy a helyi virtuális hálózatban a virtuális VMs-kapcsolat elérhető-e a virtuális magánhálózaton a távoli virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="fbb55-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="fbb55-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbb55-121">-AsJob</span></span>
<span data-ttu-id="fbb55-122">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="fbb55-122">Run the command as a job</span></span>

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

### <span data-ttu-id="fbb55-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb55-123">-DefaultProfile</span></span>
<span data-ttu-id="fbb55-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbb55-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb55-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb55-125">-InputObject</span></span>
<span data-ttu-id="fbb55-126">Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="fbb55-126">Identity parameter.</span></span>
<span data-ttu-id="fbb55-127">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="fbb55-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fbb55-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fbb55-128">-Name</span></span>
<span data-ttu-id="fbb55-129">A VNetPeering neve.</span><span class="sxs-lookup"><span data-stu-id="fbb55-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="fbb55-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="fbb55-130">-NoWait</span></span>
<span data-ttu-id="fbb55-131">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="fbb55-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fbb55-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb55-132">-ResourceGroupName</span></span>
<span data-ttu-id="fbb55-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fbb55-133">The name of the resource group.</span></span>
<span data-ttu-id="fbb55-134">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="fbb55-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fbb55-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbb55-135">-SubscriptionId</span></span>
<span data-ttu-id="fbb55-136">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fbb55-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fbb55-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="fbb55-137">-UseRemoteGateway</span></span>
<span data-ttu-id="fbb55-138">[System. Management. Automation. SwitchParameter] Ha távoli átjárók is használhatók ennél a virtuális hálózaton.</span><span class="sxs-lookup"><span data-stu-id="fbb55-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="fbb55-139">Ha a jelző True értékre van állítva, és a távoli allowGatewayTransit is igaz, a virtuális hálózat a távoli virtuális hálózat átjáróit fogja használni a továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="fbb55-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="fbb55-140">Csak egy társközi lehet, hogy ez a jelző True értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="fbb55-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="fbb55-141">Ez a jelző nem állítható be, ha a virtuális hálózat már rendelkezik átjáróval.</span><span class="sxs-lookup"><span data-stu-id="fbb55-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="fbb55-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbb55-142">-WorkspaceName</span></span>
<span data-ttu-id="fbb55-143">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="fbb55-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="fbb55-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fbb55-144">-Confirm</span></span>
<span data-ttu-id="fbb55-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fbb55-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb55-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb55-146">-WhatIf</span></span>
<span data-ttu-id="fbb55-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fbb55-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb55-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbb55-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb55-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb55-149">CommonParameters</span></span>
<span data-ttu-id="fbb55-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbb55-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb55-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fbb55-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb55-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb55-152">INPUTS</span></span>

### <span data-ttu-id="fbb55-153">Microsoft. Azure. PowerShell. parancsmagok. Databricks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="fbb55-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="fbb55-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb55-154">OUTPUTS</span></span>

### <span data-ttu-id="fbb55-155">Microsoft. Azure. PowerShell. parancsmagok. Databricks. modellek. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fbb55-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="fbb55-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbb55-156">NOTES</span></span>

<span data-ttu-id="fbb55-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fbb55-157">ALIASES</span></span>

<span data-ttu-id="fbb55-158">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="fbb55-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fbb55-159">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="fbb55-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fbb55-160">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="fbb55-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fbb55-161">INPUTOBJECT <IDatabricksIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="fbb55-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="fbb55-162">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fbb55-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fbb55-163">`[PeeringName <String>]`: A munkaterület vNete.</span><span class="sxs-lookup"><span data-stu-id="fbb55-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="fbb55-164">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fbb55-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fbb55-165">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="fbb55-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="fbb55-166">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fbb55-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fbb55-167">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="fbb55-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="fbb55-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbb55-168">RELATED LINKS</span></span>

