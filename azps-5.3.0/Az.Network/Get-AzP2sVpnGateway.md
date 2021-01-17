---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480355"
---
# <span data-ttu-id="baa66-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="baa66-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="baa66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa66-102">SYNOPSIS</span></span>
<span data-ttu-id="baa66-103">Egy meglévő P2SVpnGatewayt kap a VirtualHub alatt.</span><span class="sxs-lookup"><span data-stu-id="baa66-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="baa66-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="baa66-104">SYNTAX</span></span>

### <span data-ttu-id="baa66-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="baa66-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa66-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa66-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baa66-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="baa66-107">DESCRIPTION</span></span>
<span data-ttu-id="baa66-108">A **Get-AzP2sVpnGateway** parancsmag lehetővé teszi, hogy meglévő P2SVpnGatewayt kap a VirtualHub alatt.</span><span class="sxs-lookup"><span data-stu-id="baa66-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="baa66-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="baa66-109">EXAMPLES</span></span>

### <span data-ttu-id="baa66-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="baa66-110">Example 1</span></span>
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

<span data-ttu-id="baa66-111">A **Get-AzP2sVpnGateway** parancsmag lehetővé teszi egy meglévő P2SVpnGateway lekért beállítását a VirtualHub alatt, amely a Point to site connectivity funkcióval használható.</span><span class="sxs-lookup"><span data-stu-id="baa66-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="baa66-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baa66-112">PARAMETERS</span></span>

### <span data-ttu-id="baa66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa66-113">-DefaultProfile</span></span>
<span data-ttu-id="baa66-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="baa66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa66-115">-Name</span><span class="sxs-lookup"><span data-stu-id="baa66-115">-Name</span></span>
<span data-ttu-id="baa66-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="baa66-116">The resource name.</span></span>

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

### <span data-ttu-id="baa66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa66-117">-ResourceGroupName</span></span>
<span data-ttu-id="baa66-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="baa66-118">The resource group name.</span></span>

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

### <span data-ttu-id="baa66-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa66-119">CommonParameters</span></span>
<span data-ttu-id="baa66-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa66-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa66-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa66-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa66-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baa66-122">INPUTS</span></span>

### <span data-ttu-id="baa66-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="baa66-123">None</span></span>

## <span data-ttu-id="baa66-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baa66-124">OUTPUTS</span></span>

### <span data-ttu-id="baa66-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="baa66-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="baa66-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="baa66-126">NOTES</span></span>

## <span data-ttu-id="baa66-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baa66-127">RELATED LINKS</span></span>
