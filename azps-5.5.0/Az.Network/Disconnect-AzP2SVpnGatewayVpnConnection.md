---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
ms.openlocfilehash: 106e924913af3df113f81c75bf2fa44bc4ee8b5c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157170"
---
# <span data-ttu-id="ac9b1-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ac9b1-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="ac9b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac9b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9b1-103">A csatlakoztatott VPN-ügyfélkapcsolatok leválasztása adott p2s vpn-átjáróval</span><span class="sxs-lookup"><span data-stu-id="ac9b1-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="ac9b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac9b1-104">SYNTAX</span></span>

### <span data-ttu-id="ac9b1-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac9b1-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="ac9b1-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ac9b1-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="ac9b1-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ac9b1-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="ac9b1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac9b1-108">DESCRIPTION</span></span>
<span data-ttu-id="ac9b1-109">A **Disconnect-AzP2sVpnGatewayVpnConnection** parancsmag lehetővé teszi, hogy a P2SVpnGatewayről leválasztsa a helykapcsolat aktuális pontját.</span><span class="sxs-lookup"><span data-stu-id="ac9b1-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="ac9b1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac9b1-110">EXAMPLES</span></span>

### <span data-ttu-id="ac9b1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ac9b1-111">Example 1</span></span>
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

## <span data-ttu-id="ac9b1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac9b1-112">PARAMETERS</span></span>

### <span data-ttu-id="ac9b1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac9b1-113">-InputObject</span></span>
<span data-ttu-id="ac9b1-114">A módosítható p2s vpn átjáróobjektum</span><span class="sxs-lookup"><span data-stu-id="ac9b1-114">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="ac9b1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ac9b1-115">-Name</span></span>
<span data-ttu-id="ac9b1-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ac9b1-116">The resource name.</span></span>

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

### <span data-ttu-id="ac9b1-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="ac9b1-117">-VpnConnectionId</span></span>
<span data-ttu-id="ac9b1-118">Vpn-kapcsolat Ida</span><span class="sxs-lookup"><span data-stu-id="ac9b1-118">Vpn Connection Ida</span></span>

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

### <span data-ttu-id="ac9b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac9b1-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac9b1-120">The resource group name.</span></span>

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

### <span data-ttu-id="ac9b1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac9b1-121">-ResourceId</span></span>
<span data-ttu-id="ac9b1-122">P2s Virtual network gateway resource Id</span><span class="sxs-lookup"><span data-stu-id="ac9b1-122">P2s Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="ac9b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9b1-123">CommonParameters</span></span>
<span data-ttu-id="ac9b1-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9b1-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9b1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9b1-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac9b1-126">INPUTS</span></span>

### <span data-ttu-id="ac9b1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ac9b1-127">System.String</span></span>

## <span data-ttu-id="ac9b1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac9b1-128">OUTPUTS</span></span>

### <span data-ttu-id="ac9b1-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ac9b1-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="ac9b1-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac9b1-130">NOTES</span></span>

## <span data-ttu-id="ac9b1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac9b1-131">RELATED LINKS</span></span>
