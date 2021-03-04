---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: a569f605c139d5cd34c42ee1567989acebabbe61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923738"
---
# <span data-ttu-id="8e073-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="8e073-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="8e073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e073-102">SYNOPSIS</span></span>
<span data-ttu-id="8e073-103">VNet-társviszonyt hoz létre a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="8e073-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="8e073-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e073-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e073-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e073-105">DESCRIPTION</span></span>
<span data-ttu-id="8e073-106">VNet-társviszonyt hoz létre a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="8e073-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="8e073-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e073-107">EXAMPLES</span></span>

### <span data-ttu-id="8e073-108">1. példa: Vnet-társviszony létrehozása adatokhoz</span><span class="sxs-lookup"><span data-stu-id="8e073-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="8e073-109">Ez a parancs egy vnet-társviszonyt hoz létre az adatkapcsolatok számára.</span><span class="sxs-lookup"><span data-stu-id="8e073-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="8e073-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e073-110">PARAMETERS</span></span>

### <span data-ttu-id="8e073-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="8e073-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="8e073-112">A helyi virtuális hálózat virtuális hálózatában a virtuális gépről továbbított adatforgalom engedélyezett/engedélyezett lesz-e a távoli virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="8e073-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="8e073-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="8e073-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="8e073-114">Ha átjáróhivatkozások használhatók távoli virtuális hálózatban a virtuális hálózathoz való csatoláshoz.</span><span class="sxs-lookup"><span data-stu-id="8e073-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="8e073-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="8e073-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="8e073-116">Hogy a helyi virtuális hálózati térben lévő virtuális gépek hozzáférhetnek-e a virtuális hálózatok távoli virtuális térben való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8e073-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="8e073-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e073-117">-AsJob</span></span>
<span data-ttu-id="8e073-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="8e073-118">Run the command as a job</span></span>

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

### <span data-ttu-id="8e073-119">-DatabspacesAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="8e073-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="8e073-120">A CIDR-listában a virtuális hálózathoz fenntartott címblokkok listája.</span><span class="sxs-lookup"><span data-stu-id="8e073-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-121">-DatabeidsVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8e073-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="8e073-122">Az adatkapcsolat virtuális hálózatának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e073-122">The Id of the databricks virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e073-123">-DefaultProfile</span></span>
<span data-ttu-id="8e073-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e073-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e073-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8e073-125">-Name</span></span>
<span data-ttu-id="8e073-126">A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="8e073-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8e073-127">-NoWait</span></span>
<span data-ttu-id="8e073-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="8e073-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8e073-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="8e073-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="8e073-130">A CIDR-listában a virtuális hálózathoz fenntartott címblokkok listája.</span><span class="sxs-lookup"><span data-stu-id="8e073-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8e073-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="8e073-132">A távoli virtuális hálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e073-132">The Id of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e073-133">-ResourceGroupName</span></span>
<span data-ttu-id="8e073-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e073-134">The name of the resource group.</span></span>
<span data-ttu-id="8e073-135">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="8e073-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e073-136">-SubscriptionId</span></span>
<span data-ttu-id="8e073-137">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e073-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="8e073-138">-UseRemoteGateway</span></span>
<span data-ttu-id="8e073-139">Ha távoli átjárók használhatók ezen a virtuális hálózaton.</span><span class="sxs-lookup"><span data-stu-id="8e073-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="8e073-140">Ha a jelölő igazra van állítva, és az allowGatewayTransit távoli társviszonyon is igaz, a virtuális hálózat a távoli virtuális hálózat átjáróit fogja használni az átvitelhez.</span><span class="sxs-lookup"><span data-stu-id="8e073-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="8e073-141">Csak egy társviszonyhoz állíthatja be ezt a jelölőt igazra.</span><span class="sxs-lookup"><span data-stu-id="8e073-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="8e073-142">Ez a jelölő nem beállítható, ha a virtuális hálózatnak már van átjárója.</span><span class="sxs-lookup"><span data-stu-id="8e073-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="8e073-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e073-143">-WorkspaceName</span></span>
<span data-ttu-id="8e073-144">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="8e073-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e073-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e073-145">-Confirm</span></span>
<span data-ttu-id="8e073-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e073-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e073-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e073-147">-WhatIf</span></span>
<span data-ttu-id="8e073-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e073-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e073-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e073-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e073-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e073-150">CommonParameters</span></span>
<span data-ttu-id="8e073-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e073-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e073-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e073-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e073-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e073-153">INPUTS</span></span>

## <span data-ttu-id="8e073-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e073-154">OUTPUTS</span></span>

### <span data-ttu-id="8e073-155">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8e073-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="8e073-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e073-156">NOTES</span></span>

<span data-ttu-id="8e073-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8e073-157">ALIASES</span></span>

## <span data-ttu-id="8e073-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e073-158">RELATED LINKS</span></span>

