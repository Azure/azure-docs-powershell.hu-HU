---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181062"
---
# <span data-ttu-id="7eadf-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7eadf-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="7eadf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7eadf-102">SYNOPSIS</span></span>
<span data-ttu-id="7eadf-103">Az aktuális aggregared-pont a P2SVpnGateway-ról származó állapot-kapcsolatokra vonatkozó információkat kapja.</span><span class="sxs-lookup"><span data-stu-id="7eadf-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="7eadf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7eadf-104">SYNTAX</span></span>

### <span data-ttu-id="7eadf-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7eadf-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eadf-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7eadf-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7eadf-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7eadf-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eadf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7eadf-108">DESCRIPTION</span></span>
<span data-ttu-id="7eadf-109">A **Get-AzP2sVpnGatewayConnectionHealth** parancsmag lehetővé teszi, hogy az aktuális összesített állapotot kikapcsolja a P2SVpnGateway-ról a helyközi kapcsolatok pontra.</span><span class="sxs-lookup"><span data-stu-id="7eadf-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7eadf-110">Összesített állapot: a P2SVpnGateway-ra kapcsolt, a teljes behatolás és a kilépési bájtok számát jeleníti meg a P2SVpnGateway-on keresztül, és kiosztott IP-címeket továbbít a webhely ügyfeleinek.</span><span class="sxs-lookup"><span data-stu-id="7eadf-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="7eadf-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7eadf-111">EXAMPLES</span></span>

### <span data-ttu-id="7eadf-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7eadf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
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

<span data-ttu-id="7eadf-113">A **Get-AzP2sVpnGatewayConnectionHealth** parancsmag lehetővé teszi, hogy az aktuális összesített állapotot kikapcsolja a P2SVpnGateway-ról a helyközi kapcsolatok pontra.</span><span class="sxs-lookup"><span data-stu-id="7eadf-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7eadf-114">A fenti parancs lehetővé teszik, hogy a kimenet állapota beállítás szerint a P2SVpnGateway csatlakozó, a hely ügyfeleinek száma 2.</span><span class="sxs-lookup"><span data-stu-id="7eadf-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="7eadf-115">Az P2SVpnGateway-on átvitt teljes behatolási és kilépési bájtok száma 100, illetve 200.</span><span class="sxs-lookup"><span data-stu-id="7eadf-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="7eadf-116">A "192.168.2.1", "192.168.2.2" és a "" kiosztott IP-címek a kapcsolódási pontok számára a webhely ügyfeleinek</span><span class="sxs-lookup"><span data-stu-id="7eadf-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="7eadf-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7eadf-117">PARAMETERS</span></span>

### <span data-ttu-id="7eadf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eadf-118">-DefaultProfile</span></span>
<span data-ttu-id="7eadf-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7eadf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eadf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eadf-120">-InputObject</span></span>
<span data-ttu-id="7eadf-121">A módosítani kívánt p2s VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="7eadf-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eadf-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7eadf-122">-Name</span></span>
<span data-ttu-id="7eadf-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7eadf-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eadf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eadf-124">-ResourceGroupName</span></span>
<span data-ttu-id="7eadf-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7eadf-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eadf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eadf-126">-ResourceId</span></span>
<span data-ttu-id="7eadf-127">A módosítani kívánt P2SVpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="7eadf-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eadf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eadf-128">CommonParameters</span></span>
<span data-ttu-id="7eadf-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7eadf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eadf-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eadf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eadf-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eadf-131">INPUTS</span></span>

### <span data-ttu-id="7eadf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7eadf-132">System.String</span></span>
<span data-ttu-id="7eadf-133">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7eadf-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7eadf-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eadf-134">OUTPUTS</span></span>

### <span data-ttu-id="7eadf-135">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7eadf-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7eadf-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7eadf-136">NOTES</span></span>

## <span data-ttu-id="7eadf-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7eadf-137">RELATED LINKS</span></span>
