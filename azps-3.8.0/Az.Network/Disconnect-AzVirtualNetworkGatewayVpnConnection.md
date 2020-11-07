---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845454"
---
# <span data-ttu-id="aefa7-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="aefa7-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="aefa7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aefa7-102">SYNOPSIS</span></span> 
<span data-ttu-id="aefa7-103">Kapcsolat bontása az adott virtuális hálózati átjáróval összekapcsolt VPN-ügyfélkapcsolatokkal</span><span class="sxs-lookup"><span data-stu-id="aefa7-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="aefa7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aefa7-104">SYNTAX</span></span>
### <span data-ttu-id="aefa7-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aefa7-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="aefa7-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="aefa7-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="aefa7-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="aefa7-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="aefa7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aefa7-108">DESCRIPTION</span></span>
<span data-ttu-id="aefa7-109">A **Leválasztás-AzVirtualNetworkGatewayVpnConnection** parancsmag lehetővé teszi a csatlakoztatott VPN-ügyfél kapcsolatának leválasztását.</span><span class="sxs-lookup"><span data-stu-id="aefa7-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="aefa7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aefa7-110">EXAMPLES</span></span>

### <span data-ttu-id="aefa7-111">Például</span><span class="sxs-lookup"><span data-stu-id="aefa7-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="aefa7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aefa7-112">PARAMETERS</span></span>

### <span data-ttu-id="aefa7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aefa7-113">-ResourceGroupName</span></span>
<span data-ttu-id="aefa7-114">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="aefa7-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aefa7-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aefa7-115">-ResourceName</span></span>
<span data-ttu-id="aefa7-116">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="aefa7-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aefa7-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aefa7-117">-ResourceId</span></span>
<span data-ttu-id="aefa7-118">Virtuális hálózati átjáró erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="aefa7-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aefa7-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="aefa7-119">-VpnConnectionId</span></span>
<span data-ttu-id="aefa7-120">Virtuális magánhálózati kapcsolat-azonosítók</span><span class="sxs-lookup"><span data-stu-id="aefa7-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aefa7-121">-InputObject</span></span>
<span data-ttu-id="aefa7-122">Virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="aefa7-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aefa7-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aefa7-123">-AsJob</span></span>
<span data-ttu-id="aefa7-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aefa7-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aefa7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefa7-125">CommonParameters</span></span>
<span data-ttu-id="aefa7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aefa7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefa7-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aefa7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefa7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aefa7-128">INPUTS</span></span>

### <span data-ttu-id="aefa7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aefa7-129">System.String</span></span>

## <span data-ttu-id="aefa7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aefa7-130">OUTPUTS</span></span>

### <span data-ttu-id="aefa7-131">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aefa7-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="aefa7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aefa7-132">NOTES</span></span>

## <span data-ttu-id="aefa7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aefa7-133">RELATED LINKS</span></span>
