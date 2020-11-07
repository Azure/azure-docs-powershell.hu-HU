---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 83d91b7761200813e2973dfe4a76067e92f9bf42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838310"
---
# <span data-ttu-id="b8384-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b8384-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8384-102">SYNOPSIS</span></span>
<span data-ttu-id="b8384-103">Virtuális hálózati átjáró kapcsolatának beállítása.</span><span class="sxs-lookup"><span data-stu-id="b8384-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="b8384-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8384-104">SYNTAX</span></span>

### <span data-ttu-id="b8384-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8384-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecPolTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8384-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="b8384-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecPolTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] 
 -Tag <Hashtable> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8384-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8384-107">DESCRIPTION</span></span>
<span data-ttu-id="b8384-108">A **set-AzVirtualNetworkGatewayConnection** parancsmag a virtuális hálózati átjáró kapcsolatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8384-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="b8384-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b8384-109">EXAMPLES</span></span>

### <span data-ttu-id="b8384-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="b8384-110">Example 1:</span></span>
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

### <span data-ttu-id="b8384-111">2. példa: Címkék hozzáadása és frissítése meglévő VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="b8384-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8384-112">PARAMETERS</span></span>

### <span data-ttu-id="b8384-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8384-113">-AsJob</span></span>
<span data-ttu-id="b8384-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b8384-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8384-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8384-115">-DefaultProfile</span></span>
<span data-ttu-id="b8384-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8384-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8384-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b8384-117">-EnableBgp</span></span>
<span data-ttu-id="b8384-118">Szeretné-e, hogy a BGP-munkamenetet egy S2S VPN-alagúton keresztül használja</span><span class="sxs-lookup"><span data-stu-id="b8384-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="b8384-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b8384-119">-Force</span></span>
<span data-ttu-id="b8384-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b8384-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8384-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="b8384-121">-IpsecPolicies</span></span>
<span data-ttu-id="b8384-122">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="b8384-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="b8384-123">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b8384-123">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="b8384-124">A forgalom kiválasztó házirendjeinek listája.</span><span class="sxs-lookup"><span data-stu-id="b8384-124">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="b8384-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="b8384-125">-Tag</span></span>
<span data-ttu-id="b8384-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b8384-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b8384-127">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="b8384-127">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="b8384-128">A S2S-kapcsolatokhoz használható házirend-alapú forgalom kiválasztása</span><span class="sxs-lookup"><span data-stu-id="b8384-128">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="b8384-129">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-129">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="b8384-130">Azt a PSVirtualNetworkGatewayConnection-objektumot adja meg, amelyre a parancsmag a virtuális hálózati átjáró kapcsolatának módosítását használja.</span><span class="sxs-lookup"><span data-stu-id="b8384-130">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="b8384-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8384-131">-Confirm</span></span>
<span data-ttu-id="b8384-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8384-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8384-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8384-133">-WhatIf</span></span>
<span data-ttu-id="b8384-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8384-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8384-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8384-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8384-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8384-136">CommonParameters</span></span>
<span data-ttu-id="b8384-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8384-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8384-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8384-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8384-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8384-139">INPUTS</span></span>

### <span data-ttu-id="b8384-140">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="b8384-141">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8384-141">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8384-142">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="b8384-142">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="b8384-143">Microsoft. Azure. commands. Network. models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="b8384-143">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="b8384-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8384-144">OUTPUTS</span></span>

### <span data-ttu-id="b8384-145">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b8384-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8384-146">NOTES</span></span>

## <span data-ttu-id="b8384-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8384-147">RELATED LINKS</span></span>

[<span data-ttu-id="b8384-148">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-148">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b8384-149">Új – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-149">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b8384-150">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b8384-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


