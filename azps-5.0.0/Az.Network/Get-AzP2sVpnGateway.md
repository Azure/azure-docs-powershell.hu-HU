---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195201"
---
# <span data-ttu-id="b4bc5-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b4bc5-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="b4bc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bc5-103">Létező P2SVpnGateway kap a VirtualHub csoportban.</span><span class="sxs-lookup"><span data-stu-id="b4bc5-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="b4bc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4bc5-104">SYNTAX</span></span>

### <span data-ttu-id="b4bc5-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4bc5-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bc5-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bc5-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4bc5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4bc5-107">DESCRIPTION</span></span>
<span data-ttu-id="b4bc5-108">A **Get-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy egy meglévő P2SVpnGateway beszerezzen a VirtualHub csoportban.</span><span class="sxs-lookup"><span data-stu-id="b4bc5-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="b4bc5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b4bc5-109">EXAMPLES</span></span>

### <span data-ttu-id="b4bc5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4bc5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

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
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="b4bc5-111">A **Get-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy egy meglévő P2SVpnGateway a VirtualHub, amely a webhely-összekapcsolási ponthoz használatos.</span><span class="sxs-lookup"><span data-stu-id="b4bc5-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="b4bc5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4bc5-112">PARAMETERS</span></span>

### <span data-ttu-id="b4bc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bc5-113">-DefaultProfile</span></span>
<span data-ttu-id="b4bc5-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4bc5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4bc5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4bc5-115">-Name</span></span>
<span data-ttu-id="b4bc5-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b4bc5-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, P2SVpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bc5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bc5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4bc5-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b4bc5-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bc5-119">CommonParameters</span></span>
<span data-ttu-id="b4bc5-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4bc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bc5-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bc5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bc5-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4bc5-122">INPUTS</span></span>

### <span data-ttu-id="b4bc5-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b4bc5-123">None</span></span>

## <span data-ttu-id="b4bc5-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4bc5-124">OUTPUTS</span></span>

### <span data-ttu-id="b4bc5-125">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b4bc5-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="b4bc5-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4bc5-126">NOTES</span></span>

## <span data-ttu-id="b4bc5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4bc5-127">RELATED LINKS</span></span>
