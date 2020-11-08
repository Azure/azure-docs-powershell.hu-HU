---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181107"
---
# <span data-ttu-id="31071-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31071-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="31071-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31071-102">SYNOPSIS</span></span>
<span data-ttu-id="31071-103">Azure ExpressRoute áramkört kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="31071-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="31071-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31071-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31071-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31071-105">DESCRIPTION</span></span>
<span data-ttu-id="31071-106">A **Get-AzExpressRouteCircuit** parancsmag az ExpressRoute-áramköri objektumnak az előfizetésből való visszakeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="31071-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="31071-107">A visszaadott áramkör-objektum a ExpressRoute-áramkörön működő többi parancsmaghoz is használható.</span><span class="sxs-lookup"><span data-stu-id="31071-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="31071-108">Példák</span><span class="sxs-lookup"><span data-stu-id="31071-108">EXAMPLES</span></span>

### <span data-ttu-id="31071-109">Példa 1: a ExpressRoute áramkör beszerzése</span><span class="sxs-lookup"><span data-stu-id="31071-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="31071-110">A "testrg" és a ResourceGroupName "teszt" nevű ExpressRoute-áramkör beszerzése</span><span class="sxs-lookup"><span data-stu-id="31071-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="31071-111">2. példa: a ExpressRoute-áramkörök listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="31071-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="31071-112">Az összes olyan ExpressRoute-áramkört kapja, akinek a neve "teszt" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="31071-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="31071-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31071-113">PARAMETERS</span></span>

### <span data-ttu-id="31071-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31071-114">-DefaultProfile</span></span>
<span data-ttu-id="31071-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31071-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31071-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31071-116">-Name</span></span>
<span data-ttu-id="31071-117">A ExpressRoute áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="31071-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="31071-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31071-118">-ResourceGroupName</span></span>
<span data-ttu-id="31071-119">Annak az erőforráscsoportnek a neve, amely a ExpressRoute áramkört tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="31071-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="31071-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31071-120">CommonParameters</span></span>
<span data-ttu-id="31071-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31071-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31071-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31071-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31071-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31071-123">INPUTS</span></span>

### <span data-ttu-id="31071-124">System. String</span><span class="sxs-lookup"><span data-stu-id="31071-124">System.String</span></span>

## <span data-ttu-id="31071-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31071-125">OUTPUTS</span></span>

### <span data-ttu-id="31071-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31071-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="31071-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31071-127">NOTES</span></span>

## <span data-ttu-id="31071-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31071-128">RELATED LINKS</span></span>

[<span data-ttu-id="31071-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31071-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="31071-130">Új – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31071-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="31071-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31071-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="31071-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31071-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
