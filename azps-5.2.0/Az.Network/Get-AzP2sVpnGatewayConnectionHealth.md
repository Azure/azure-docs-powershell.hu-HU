---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354906"
---
# <span data-ttu-id="7c337-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7c337-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="7c337-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c337-102">SYNOPSIS</span></span>
<span data-ttu-id="7c337-103">A P2SVpnGatewaytől a webhelykapcsolatok állapotinformációira vonatkozó aktuális aggregared pontot kapja.</span><span class="sxs-lookup"><span data-stu-id="7c337-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="7c337-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c337-104">SYNTAX</span></span>

### <span data-ttu-id="7c337-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c337-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c337-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7c337-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c337-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7c337-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c337-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c337-108">DESCRIPTION</span></span>
<span data-ttu-id="7c337-109">A **Get-AzP2sVpnGatewayConnectionHealth** parancsmag lehetővé teszi a P2SVpnGatewayből a webhelykapcsolatok aktuális összesített állapotát.</span><span class="sxs-lookup"><span data-stu-id="7c337-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7c337-110">Az összesített állapot a P2SVpnGatewayhez csatlakozó webhely ügyfeleire vonatkozó pontokat, a P2SVpnGatewayen keresztül átvitt összes bejövő és bejövő bájtot, valamint a webhely ügyfeleihez csatlakoztatott ponthoz kiosztott IP-címeket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7c337-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="7c337-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c337-111">EXAMPLES</span></span>

### <span data-ttu-id="7c337-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="7c337-112">Example 1</span></span>
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

<span data-ttu-id="7c337-113">A **Get-AzP2sVpnGatewayConnectionHealth** parancsmag lehetővé teszi a P2SVpnGatewayből a webhelykapcsolatok aktuális összesített állapotát.</span><span class="sxs-lookup"><span data-stu-id="7c337-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7c337-114">Above command let output health shows that number to site clients connected to P2SVpnGateway are 2.</span><span class="sxs-lookup"><span data-stu-id="7c337-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="7c337-115">A P2SVpnGatewayen keresztül átvitt összes bejövő és bejövő bájt 100, illetve 200.</span><span class="sxs-lookup"><span data-stu-id="7c337-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="7c337-116">A helyhez kapcsolt ügyfelek ip-címei a következőek: "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="7c337-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="7c337-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c337-117">PARAMETERS</span></span>

### <span data-ttu-id="7c337-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c337-118">-DefaultProfile</span></span>
<span data-ttu-id="7c337-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c337-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c337-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c337-120">-InputObject</span></span>
<span data-ttu-id="7c337-121">A módosítható p2s vpn átjáróobjektum</span><span class="sxs-lookup"><span data-stu-id="7c337-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="7c337-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7c337-122">-Name</span></span>
<span data-ttu-id="7c337-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7c337-123">The resource name.</span></span>

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

### <span data-ttu-id="7c337-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c337-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c337-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c337-125">The resource group name.</span></span>

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

### <span data-ttu-id="7c337-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c337-126">-ResourceId</span></span>
<span data-ttu-id="7c337-127">A módosítható P2SVpnGateway Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="7c337-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="7c337-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c337-128">CommonParameters</span></span>
<span data-ttu-id="7c337-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c337-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c337-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c337-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c337-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c337-131">INPUTS</span></span>

### <span data-ttu-id="7c337-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7c337-132">System.String</span></span>
<span data-ttu-id="7c337-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7c337-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7c337-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c337-134">OUTPUTS</span></span>

### <span data-ttu-id="7c337-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7c337-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7c337-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c337-136">NOTES</span></span>

## <span data-ttu-id="7c337-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c337-137">RELATED LINKS</span></span>
