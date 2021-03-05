---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: 1cbbfcbc87ed1d9be869066f8ec6dd288ba3d4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003702"
---
# <span data-ttu-id="46353-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="46353-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="46353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46353-102">SYNOPSIS</span></span> 
<span data-ttu-id="46353-103">Leválaszthatja a vpn-ügyfélkapcsolatokat egy adott virtuális hálózati átjáróval.</span><span class="sxs-lookup"><span data-stu-id="46353-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="46353-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46353-104">SYNTAX</span></span>
### <span data-ttu-id="46353-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46353-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="46353-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="46353-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="46353-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="46353-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="46353-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46353-108">DESCRIPTION</span></span>
<span data-ttu-id="46353-109">A **Disconnect-AzVirtualNetworkGatewayVpnConnection** parancsmag lehetővé teszi, hogy leválasztsa az adott csatlakoztatott VPN-ügyfélkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="46353-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="46353-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46353-110">EXAMPLES</span></span>

### <span data-ttu-id="46353-111">Példa</span><span class="sxs-lookup"><span data-stu-id="46353-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="46353-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46353-112">PARAMETERS</span></span>

### <span data-ttu-id="46353-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46353-113">-ResourceGroupName</span></span>
<span data-ttu-id="46353-114">Virtuális hálózati átjáró erőforráscsoportja neve</span><span class="sxs-lookup"><span data-stu-id="46353-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="46353-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="46353-115">-ResourceName</span></span>
<span data-ttu-id="46353-116">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="46353-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="46353-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46353-117">-ResourceId</span></span>
<span data-ttu-id="46353-118">Virtuális hálózati átjáró erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="46353-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="46353-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="46353-119">-VpnConnectionId</span></span>
<span data-ttu-id="46353-120">Vpn-kapcsolatazonosítók</span><span class="sxs-lookup"><span data-stu-id="46353-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="46353-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46353-121">-InputObject</span></span>
<span data-ttu-id="46353-122">Virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="46353-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="46353-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46353-123">-AsJob</span></span>
<span data-ttu-id="46353-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="46353-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46353-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46353-125">CommonParameters</span></span>
<span data-ttu-id="46353-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46353-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46353-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46353-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46353-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46353-128">INPUTS</span></span>

### <span data-ttu-id="46353-129">System.String</span><span class="sxs-lookup"><span data-stu-id="46353-129">System.String</span></span>

## <span data-ttu-id="46353-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46353-130">OUTPUTS</span></span>

### <span data-ttu-id="46353-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46353-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="46353-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46353-132">NOTES</span></span>

## <span data-ttu-id="46353-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46353-133">RELATED LINKS</span></span>
