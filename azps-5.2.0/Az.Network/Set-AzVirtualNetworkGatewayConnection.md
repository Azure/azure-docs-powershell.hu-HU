---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331758"
---
# <span data-ttu-id="cc2ce-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc2ce-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cc2ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cc2ce-103">Konfigurál egy virtuális hálózati átjárókapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="cc2ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc2ce-104">SYNTAX</span></span>

### <span data-ttu-id="cc2ce-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc2ce-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc2ce-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="cc2ce-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc2ce-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc2ce-107">DESCRIPTION</span></span>
<span data-ttu-id="cc2ce-108">A **Set-AzVirtualNetworkGatewayConnection** parancsmag virtuális hálózati átjárókapcsolatot konfigurál.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="cc2ce-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc2ce-109">EXAMPLES</span></span>

### <span data-ttu-id="cc2ce-110">1. példa:</span><span class="sxs-lookup"><span data-stu-id="cc2ce-110">Example 1:</span></span>
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

### <span data-ttu-id="cc2ce-111">2. példa: Címkék hozzáadása/frissítése meglévő VirtualNetworkGatewayConnectionhoz</span><span class="sxs-lookup"><span data-stu-id="cc2ce-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="cc2ce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc2ce-112">PARAMETERS</span></span>

### <span data-ttu-id="cc2ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc2ce-113">-AsJob</span></span>
<span data-ttu-id="cc2ce-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cc2ce-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc2ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc2ce-115">-DefaultProfile</span></span>
<span data-ttu-id="cc2ce-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc2ce-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="cc2ce-117">-EnableBgp</span></span>
<span data-ttu-id="cc2ce-118">BGP-munkamenet használata S2S VPN-csatornán keresztül</span><span class="sxs-lookup"><span data-stu-id="cc2ce-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="cc2ce-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="cc2ce-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="cc2ce-120">A kapcsolat elhalt társ észlelési időkorlátja másodpercek alatt</span><span class="sxs-lookup"><span data-stu-id="cc2ce-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="cc2ce-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cc2ce-121">-Force</span></span>
<span data-ttu-id="cc2ce-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc2ce-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="cc2ce-123">-IpsecPolicies</span></span>
<span data-ttu-id="cc2ce-124">AZ IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="cc2ce-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc2ce-125">-Tag</span></span>
<span data-ttu-id="cc2ce-126">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cc2ce-127">-TrafficSelepolicy</span><span class="sxs-lookup"><span data-stu-id="cc2ce-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="cc2ce-128">A Forgalomválasztó házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-128">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="cc2ce-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc2ce-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="cc2ce-130">A PrivateIP használata S2S-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="cc2ce-130">Whether to use PrivateIP for a S2S connection</span></span>

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

### <span data-ttu-id="cc2ce-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="cc2ce-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="cc2ce-132">Házirendalapú forgalomválasztók használata S2S-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="cc2ce-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="cc2ce-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc2ce-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="cc2ce-134">Megadja azt a PSVirtualNetworkGatewayConnection objektumot, amely a parancsmag segítségével módosítja a virtuális hálózati átjáró kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="cc2ce-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc2ce-135">-Confirm</span></span>
<span data-ttu-id="cc2ce-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc2ce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc2ce-137">-WhatIf</span></span>
<span data-ttu-id="cc2ce-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc2ce-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc2ce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc2ce-140">CommonParameters</span></span>
<span data-ttu-id="cc2ce-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc2ce-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc2ce-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc2ce-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc2ce-143">INPUTS</span></span>

### <span data-ttu-id="cc2ce-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc2ce-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="cc2ce-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc2ce-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cc2ce-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="cc2ce-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="cc2ce-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelepolicy[]</span><span class="sxs-lookup"><span data-stu-id="cc2ce-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="cc2ce-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc2ce-148">OUTPUTS</span></span>

### <span data-ttu-id="cc2ce-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc2ce-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cc2ce-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc2ce-150">NOTES</span></span>

## <span data-ttu-id="cc2ce-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc2ce-151">RELATED LINKS</span></span>

[<span data-ttu-id="cc2ce-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc2ce-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cc2ce-153">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc2ce-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cc2ce-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc2ce-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


