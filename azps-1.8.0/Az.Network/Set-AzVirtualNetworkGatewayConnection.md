---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 15023fbbb0576f99f66519198c893080ebe1c92f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669961"
---
# <span data-ttu-id="54fa2-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54fa2-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="54fa2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="54fa2-103">Virtuális hálózati átjáró kapcsolatának beállítása.</span><span class="sxs-lookup"><span data-stu-id="54fa2-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="54fa2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54fa2-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fa2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="54fa2-106">A **set-AzVirtualNetworkGatewayConnection** parancsmag a virtuális hálózati átjáró kapcsolatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="54fa2-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="54fa2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="54fa2-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="54fa2-108">Example 1:</span></span>
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

## <span data-ttu-id="54fa2-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54fa2-109">PARAMETERS</span></span>

### <span data-ttu-id="54fa2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54fa2-110">-AsJob</span></span>
<span data-ttu-id="54fa2-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="54fa2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54fa2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fa2-112">-DefaultProfile</span></span>
<span data-ttu-id="54fa2-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54fa2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54fa2-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="54fa2-114">-EnableBgp</span></span>
<span data-ttu-id="54fa2-115">Szeretné-e, hogy a BGP-munkamenetet egy S2S VPN-alagúton keresztül használja</span><span class="sxs-lookup"><span data-stu-id="54fa2-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="54fa2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="54fa2-116">-Force</span></span>
<span data-ttu-id="54fa2-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="54fa2-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54fa2-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="54fa2-118">-IpsecPolicies</span></span>
<span data-ttu-id="54fa2-119">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="54fa2-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="54fa2-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="54fa2-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="54fa2-121">A S2S-kapcsolatokhoz használható házirend-alapú forgalom kiválasztása</span><span class="sxs-lookup"><span data-stu-id="54fa2-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="54fa2-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54fa2-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="54fa2-123">Azt a PSVirtualNetworkGatewayConnection-objektumot adja meg, amelyre a parancsmag a virtuális hálózati átjáró kapcsolatának módosítását használja.</span><span class="sxs-lookup"><span data-stu-id="54fa2-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="54fa2-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54fa2-124">-Confirm</span></span>
<span data-ttu-id="54fa2-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54fa2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fa2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fa2-126">-WhatIf</span></span>
<span data-ttu-id="54fa2-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54fa2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fa2-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54fa2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fa2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fa2-129">CommonParameters</span></span>
<span data-ttu-id="54fa2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54fa2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fa2-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fa2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fa2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54fa2-132">INPUTS</span></span>

### <span data-ttu-id="54fa2-133">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54fa2-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="54fa2-134">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54fa2-134">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="54fa2-135">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="54fa2-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="54fa2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54fa2-136">OUTPUTS</span></span>

### <span data-ttu-id="54fa2-137">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54fa2-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="54fa2-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54fa2-138">NOTES</span></span>

## <span data-ttu-id="54fa2-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54fa2-139">RELATED LINKS</span></span>

[<span data-ttu-id="54fa2-140">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54fa2-140">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="54fa2-141">Új – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54fa2-141">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="54fa2-142">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54fa2-142">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


