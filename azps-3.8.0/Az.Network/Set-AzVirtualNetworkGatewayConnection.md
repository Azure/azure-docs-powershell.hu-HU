---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d6a499292521632b7e0a307a6c745d1606ae4d2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010662"
---
# <span data-ttu-id="70e2b-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="70e2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="70e2b-103">Virtuális hálózati átjáró kapcsolatának beállítása.</span><span class="sxs-lookup"><span data-stu-id="70e2b-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="70e2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70e2b-104">SYNTAX</span></span>

### <span data-ttu-id="70e2b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70e2b-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
<<<<<<< HEAD
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70e2b-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="70e2b-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
<<<<<<< HEAD
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70e2b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70e2b-107">DESCRIPTION</span></span>
<span data-ttu-id="70e2b-108">A **set-AzVirtualNetworkGatewayConnection** parancsmag a virtuális hálózati átjáró kapcsolatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70e2b-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="70e2b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="70e2b-109">EXAMPLES</span></span>

### <span data-ttu-id="70e2b-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="70e2b-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="70e2b-111">2. példa: Címkék hozzáadása és frissítése meglévő VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="70e2b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70e2b-112">PARAMETERS</span></span>

### <span data-ttu-id="70e2b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70e2b-113">-AsJob</span></span>
<span data-ttu-id="70e2b-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="70e2b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70e2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e2b-115">-DefaultProfile</span></span>
<span data-ttu-id="70e2b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70e2b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="70e2b-117">-EnableBgp</span></span>
<span data-ttu-id="70e2b-118">Szeretné-e, hogy a BGP-munkamenetet egy S2S VPN-alagúton keresztül használja</span><span class="sxs-lookup"><span data-stu-id="70e2b-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="70e2b-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="70e2b-120">A kapcsolat elhalt-észlelési időtúllépése másodpercben</span><span class="sxs-lookup"><span data-stu-id="70e2b-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="70e2b-121">-Force</span></span>
<span data-ttu-id="70e2b-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="70e2b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70e2b-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="70e2b-123">-IpsecPolicies</span></span>
<span data-ttu-id="70e2b-124">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="70e2b-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="70e2b-125">-Tag</span></span>
<span data-ttu-id="70e2b-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="70e2b-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="70e2b-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="70e2b-128">A forgalom kiválasztó házirendjeinek listája.</span><span class="sxs-lookup"><span data-stu-id="70e2b-128">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="70e2b-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="70e2b-130">A PrivateIP használata S2S-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="70e2b-130">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="70e2b-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="70e2b-132">A S2S-kapcsolatokhoz használható házirend-alapú forgalom kiválasztása</span><span class="sxs-lookup"><span data-stu-id="70e2b-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="70e2b-134">Azt a PSVirtualNetworkGatewayConnection-objektumot adja meg, amelyre a parancsmag a virtuális hálózati átjáró kapcsolatának módosítását használja.</span><span class="sxs-lookup"><span data-stu-id="70e2b-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70e2b-135">-Confirm</span></span>
<span data-ttu-id="70e2b-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70e2b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e2b-137">-WhatIf</span></span>
<span data-ttu-id="70e2b-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70e2b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e2b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70e2b-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e2b-140">CommonParameters</span></span>
<span data-ttu-id="70e2b-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70e2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e2b-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e2b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e2b-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70e2b-143">INPUTS</span></span>

### <span data-ttu-id="70e2b-144">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="70e2b-145">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="70e2b-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="70e2b-146">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="70e2b-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="70e2b-147">Microsoft. Azure. commands. Network. models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="70e2b-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="70e2b-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70e2b-148">OUTPUTS</span></span>

### <span data-ttu-id="70e2b-149">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="70e2b-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70e2b-150">NOTES</span></span>

## <span data-ttu-id="70e2b-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70e2b-151">RELATED LINKS</span></span>

[<span data-ttu-id="70e2b-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="70e2b-153">Új – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="70e2b-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="70e2b-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


