---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025229"
---
# <span data-ttu-id="ea647-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ea647-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="ea647-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea647-102">SYNOPSIS</span></span> 
<span data-ttu-id="ea647-103">Kapcsolat bontása az adott virtuális hálózati átjáróval összekapcsolt VPN-ügyfélkapcsolatokkal</span><span class="sxs-lookup"><span data-stu-id="ea647-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="ea647-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea647-104">SYNTAX</span></span>
### <span data-ttu-id="ea647-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea647-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="ea647-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ea647-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="ea647-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ea647-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="ea647-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea647-108">DESCRIPTION</span></span>
<span data-ttu-id="ea647-109">A **Leválasztás-AzVirtualNetworkGatewayVpnConnection** parancsmag lehetővé teszi a csatlakoztatott VPN-ügyfél kapcsolatának leválasztását.</span><span class="sxs-lookup"><span data-stu-id="ea647-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="ea647-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ea647-110">EXAMPLES</span></span>

### <span data-ttu-id="ea647-111">Például</span><span class="sxs-lookup"><span data-stu-id="ea647-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="ea647-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea647-112">PARAMETERS</span></span>

### <span data-ttu-id="ea647-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea647-113">-ResourceGroupName</span></span>
<span data-ttu-id="ea647-114">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ea647-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="ea647-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ea647-115">-ResourceName</span></span>
<span data-ttu-id="ea647-116">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="ea647-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="ea647-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea647-117">-ResourceId</span></span>
<span data-ttu-id="ea647-118">Virtuális hálózati átjáró erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ea647-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="ea647-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="ea647-119">-VpnConnectionId</span></span>
<span data-ttu-id="ea647-120">Virtuális magánhálózati kapcsolat-azonosítók</span><span class="sxs-lookup"><span data-stu-id="ea647-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="ea647-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea647-121">-InputObject</span></span>
<span data-ttu-id="ea647-122">Virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="ea647-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="ea647-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea647-123">-AsJob</span></span>
<span data-ttu-id="ea647-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ea647-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea647-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea647-125">CommonParameters</span></span>
<span data-ttu-id="ea647-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea647-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea647-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ea647-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea647-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea647-128">INPUTS</span></span>

### <span data-ttu-id="ea647-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ea647-129">System.String</span></span>

## <span data-ttu-id="ea647-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea647-130">OUTPUTS</span></span>

### <span data-ttu-id="ea647-131">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea647-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ea647-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea647-132">NOTES</span></span>

## <span data-ttu-id="ea647-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea647-133">RELATED LINKS</span></span>
