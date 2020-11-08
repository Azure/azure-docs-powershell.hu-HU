---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017812"
---
# <span data-ttu-id="9db05-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="9db05-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="9db05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9db05-102">SYNOPSIS</span></span>
<span data-ttu-id="9db05-103">VNet-alapú társközi munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9db05-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="9db05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9db05-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9db05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9db05-105">DESCRIPTION</span></span>
<span data-ttu-id="9db05-106">VNet-alapú társközi munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9db05-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="9db05-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9db05-107">EXAMPLES</span></span>

### <span data-ttu-id="9db05-108">1. példa: vnet-alapú társközi databricks létrehozása</span><span class="sxs-lookup"><span data-stu-id="9db05-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="9db05-109">Ez a parancs létrehoz egy vnet a databricks.</span><span class="sxs-lookup"><span data-stu-id="9db05-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="9db05-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9db05-110">PARAMETERS</span></span>

### <span data-ttu-id="9db05-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="9db05-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="9db05-112">Annak megállapítása, hogy a virtuális VMs-kapcsolaton keresztül továbbított forgalom a helyi virtuális hálózaton engedélyezve van-e a távoli virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="9db05-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="9db05-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="9db05-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="9db05-114">Ha az átjáró hivatkozásait a virtuális hálózatra mutató hivatkozással lehet használni a távoli virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="9db05-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="9db05-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9db05-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="9db05-116">Azt, hogy a VMs a helyi virtuális hálózatban van-e a virtuális magánhálózaton való eléréshez a távoli virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="9db05-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="9db05-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9db05-117">-AsJob</span></span>
<span data-ttu-id="9db05-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9db05-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9db05-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="9db05-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="9db05-120">Az CIDR-ban a virtuális hálózat számára fenntartott címterület listája.</span><span class="sxs-lookup"><span data-stu-id="9db05-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="9db05-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9db05-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="9db05-122">A databricks virtuális hálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9db05-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="9db05-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db05-123">-DefaultProfile</span></span>
<span data-ttu-id="9db05-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9db05-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9db05-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9db05-125">-Name</span></span>
<span data-ttu-id="9db05-126">Annak a munkaterület-vNet a neve, amelyen a peering látható.</span><span class="sxs-lookup"><span data-stu-id="9db05-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="9db05-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="9db05-127">-NoWait</span></span>
<span data-ttu-id="9db05-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9db05-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9db05-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="9db05-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="9db05-130">Az CIDR-ban a virtuális hálózat számára fenntartott címterület listája.</span><span class="sxs-lookup"><span data-stu-id="9db05-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="9db05-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9db05-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="9db05-132">A távoli virtuális hálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9db05-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="9db05-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db05-133">-ResourceGroupName</span></span>
<span data-ttu-id="9db05-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9db05-134">The name of the resource group.</span></span>
<span data-ttu-id="9db05-135">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="9db05-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9db05-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9db05-136">-SubscriptionId</span></span>
<span data-ttu-id="9db05-137">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9db05-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9db05-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="9db05-138">-UseRemoteGateway</span></span>
<span data-ttu-id="9db05-139">Ha távoli átjárók is használhatók ennél a virtuális hálózaton.</span><span class="sxs-lookup"><span data-stu-id="9db05-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="9db05-140">Ha a jelző True értékre van állítva, és a távoli allowGatewayTransit is igaz, a virtuális hálózat a távoli virtuális hálózat átjáróit fogja használni a továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="9db05-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="9db05-141">Csak egy társközi lehet, hogy ez a jelző True értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="9db05-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="9db05-142">Ez a jelző nem állítható be, ha a virtuális hálózat már rendelkezik átjáróval.</span><span class="sxs-lookup"><span data-stu-id="9db05-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="9db05-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9db05-143">-WorkspaceName</span></span>
<span data-ttu-id="9db05-144">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9db05-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="9db05-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9db05-145">-Confirm</span></span>
<span data-ttu-id="9db05-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9db05-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db05-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db05-147">-WhatIf</span></span>
<span data-ttu-id="9db05-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9db05-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9db05-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9db05-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9db05-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db05-150">CommonParameters</span></span>
<span data-ttu-id="9db05-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9db05-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db05-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9db05-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db05-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9db05-153">INPUTS</span></span>

## <span data-ttu-id="9db05-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9db05-154">OUTPUTS</span></span>

### <span data-ttu-id="9db05-155">Microsoft. Azure. PowerShell. parancsmagok. Databricks. modellek. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="9db05-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="9db05-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9db05-156">NOTES</span></span>

<span data-ttu-id="9db05-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9db05-157">ALIASES</span></span>

## <span data-ttu-id="9db05-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9db05-158">RELATED LINKS</span></span>

