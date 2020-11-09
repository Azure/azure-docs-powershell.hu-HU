---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 21529e75ab32cf4dde0434b9e2d4de8951beeb39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300659"
---
# <span data-ttu-id="b860f-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b860f-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="b860f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b860f-102">SYNOPSIS</span></span> 
<span data-ttu-id="b860f-103">Az Azure virtuális hálózati átjáró VPN-ügyfél kapcsolati állapotának beszerzése virtuális magánhálózati ügyfélalkalmazás esetén</span><span class="sxs-lookup"><span data-stu-id="b860f-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="b860f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b860f-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="b860f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b860f-105">DESCRIPTION</span></span>
<span data-ttu-id="b860f-106">Az összes csatlakoztatott VPN-ügyfél kapcsolati állapotának listázása</span><span class="sxs-lookup"><span data-stu-id="b860f-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="b860f-107">A következő tartalma: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="b860f-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="b860f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b860f-108">EXAMPLES</span></span>

### <span data-ttu-id="b860f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b860f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName gatewayName -ResourceGroupName resourceGroup

VpnConnectionId           : OVPN_0085393D-B345-4846-0426-140616833F4C
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39672
PrivateIpAddress          : 10.1.1.131
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104084
EgressBytesTransferred    : 4059276
IngressPacketsTransferred : 1410
IngressBytesTransferred   : 67680
MaxPacketsPerSecond       : 1

VpnConnectionId           : OVPN_00F692AC-2D6F-DE7B-DCAF-07BE896233A0
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39692
PrivateIpAddress          : 10.1.1.79
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104623
EgressBytesTransferred    : 4080297
IngressPacketsTransferred : 1416
IngressBytesTransferred   : 67968
MaxPacketsPerSecond       : 1
```

<span data-ttu-id="b860f-110">Az gatewayname nevű Azure Virtual Network Gateway resourceGroup-ban az OpenVpn segítségével beolvassa az aktuálisan összekapcsolt VPN-ügyfél kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="b860f-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="b860f-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="b860f-111">Example 2</span></span>

<span data-ttu-id="b860f-112">Megtudhatja, hogy miként érheti el a VPN-ügyfél kapcsolati állapotát az Azure virtuális hálózati átjáró virtuális magánhálózati ügyfél-kapcsolati állapotának listájával.</span><span class="sxs-lookup"><span data-stu-id="b860f-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="b860f-113">autogenerated</span><span class="sxs-lookup"><span data-stu-id="b860f-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="b860f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b860f-114">PARAMETERS</span></span>

### <span data-ttu-id="b860f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b860f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b860f-116">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b860f-116">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b860f-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b860f-117">-ResourceName</span></span>
<span data-ttu-id="b860f-118">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="b860f-118">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="b860f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b860f-119">-ResourceId</span></span>
<span data-ttu-id="b860f-120">Virtuális hálózati átjáró erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b860f-120">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b860f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b860f-121">-InputObject</span></span>
<span data-ttu-id="b860f-122">Virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="b860f-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b860f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b860f-123">-AsJob</span></span>
<span data-ttu-id="b860f-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b860f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b860f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b860f-125">CommonParameters</span></span>
<span data-ttu-id="b860f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b860f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b860f-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b860f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b860f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b860f-128">INPUTS</span></span>

### <span data-ttu-id="b860f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b860f-129">System.String</span></span>

## <span data-ttu-id="b860f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b860f-130">OUTPUTS</span></span>

### <span data-ttu-id="b860f-131">Microsoft. Azure. commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="b860f-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="b860f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b860f-132">NOTES</span></span>

## <span data-ttu-id="b860f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b860f-133">RELATED LINKS</span></span>
