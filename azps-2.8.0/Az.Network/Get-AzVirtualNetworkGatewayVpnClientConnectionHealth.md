---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 994539648e6ae0d507af556e9a861bc341d5c73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837534"
---
# <span data-ttu-id="6471a-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6471a-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="6471a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6471a-102">SYNOPSIS</span></span> 
<span data-ttu-id="6471a-103">Az Azure virtuális hálózati átjáró VPN-ügyfél kapcsolati állapotának beszerzése virtuális magánhálózati ügyfélalkalmazás esetén</span><span class="sxs-lookup"><span data-stu-id="6471a-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="6471a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6471a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="6471a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6471a-105">DESCRIPTION</span></span>
<span data-ttu-id="6471a-106">Az összes csatlakoztatott VPN-ügyfél kapcsolati állapotának listázása</span><span class="sxs-lookup"><span data-stu-id="6471a-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="6471a-107">A következő tartalma: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="6471a-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="6471a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6471a-108">EXAMPLES</span></span>

### <span data-ttu-id="6471a-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6471a-109">Example 1</span></span>
```
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

<span data-ttu-id="6471a-110">Az gatewayname nevű Azure Virtual Network Gateway resourceGroup-ban az OpenVpn segítségével beolvassa az aktuálisan összekapcsolt VPN-ügyfél kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="6471a-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

## <span data-ttu-id="6471a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6471a-111">PARAMETERS</span></span>

### <span data-ttu-id="6471a-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6471a-112">-ResourceGroupName</span></span>
<span data-ttu-id="6471a-113">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6471a-113">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="6471a-114">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6471a-114">-ResourceName</span></span>
<span data-ttu-id="6471a-115">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="6471a-115">Virtual network gateway name</span></span>

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
### <span data-ttu-id="6471a-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6471a-116">-ResourceId</span></span>
<span data-ttu-id="6471a-117">Virtuális hálózati átjáró erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6471a-117">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="6471a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6471a-118">-InputObject</span></span>
<span data-ttu-id="6471a-119">Virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="6471a-119">Virtual network gateway object</span></span>

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

### <span data-ttu-id="6471a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6471a-120">-AsJob</span></span>
<span data-ttu-id="6471a-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6471a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6471a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6471a-122">CommonParameters</span></span>
<span data-ttu-id="6471a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6471a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6471a-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6471a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6471a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6471a-125">INPUTS</span></span>

### <span data-ttu-id="6471a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6471a-126">System.String</span></span>

## <span data-ttu-id="6471a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6471a-127">OUTPUTS</span></span>

### <span data-ttu-id="6471a-128">Microsoft. Azure. commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="6471a-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="6471a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6471a-129">NOTES</span></span>

## <span data-ttu-id="6471a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6471a-130">RELATED LINKS</span></span>
