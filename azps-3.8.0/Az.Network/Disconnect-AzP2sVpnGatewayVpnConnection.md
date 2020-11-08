---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
ms.openlocfilehash: ee14842a636ff451e100a75db427934f9f0a1043
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013588"
---
# <span data-ttu-id="9063c-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9063c-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="9063c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9063c-102">SYNOPSIS</span></span>
<span data-ttu-id="9063c-103">Kapcsolat bontása az adott p2s VPN-átjáróval összekapcsolt VPN-ügyfélekkel</span><span class="sxs-lookup"><span data-stu-id="9063c-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="9063c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9063c-104">SYNTAX</span></span>

### <span data-ttu-id="9063c-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9063c-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="9063c-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9063c-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="9063c-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9063c-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="9063c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9063c-108">DESCRIPTION</span></span>
<span data-ttu-id="9063c-109">A **Leválasztás – AzP2sVpnGatewayVpnConnection** parancsmag lehetővé teszi, hogy a P2SVpnGateway-ról a jelenlegi ponttól a webhelyhez való kapcsolat bontása lehetőséget kapja.</span><span class="sxs-lookup"><span data-stu-id="9063c-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="9063c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9063c-110">EXAMPLES</span></span>

### <span data-ttu-id="9063c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9063c-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="9063c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9063c-112">PARAMETERS</span></span>

### <span data-ttu-id="9063c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9063c-113">-InputObject</span></span>
<span data-ttu-id="9063c-114">A módosítani kívánt p2s VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="9063c-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9063c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9063c-115">-Name</span></span>
<span data-ttu-id="9063c-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9063c-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9063c-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="9063c-117">-VpnConnectionId</span></span>
<span data-ttu-id="9063c-118">A VPN-kapcsolat Ida-je</span><span class="sxs-lookup"><span data-stu-id="9063c-118">Vpn Connection Ida</span></span>

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

### <span data-ttu-id="9063c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9063c-119">-ResourceGroupName</span></span>
<span data-ttu-id="9063c-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9063c-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9063c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9063c-121">-ResourceId</span></span>
<span data-ttu-id="9063c-122">P2s virtuális hálózati átjáró erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9063c-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9063c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9063c-123">CommonParameters</span></span>
<span data-ttu-id="9063c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9063c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9063c-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9063c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9063c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9063c-126">INPUTS</span></span>

### <span data-ttu-id="9063c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9063c-127">System.String</span></span>

## <span data-ttu-id="9063c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9063c-128">OUTPUTS</span></span>

### <span data-ttu-id="9063c-129">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9063c-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="9063c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9063c-130">NOTES</span></span>

## <span data-ttu-id="9063c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9063c-131">RELATED LINKS</span></span>
