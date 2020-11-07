---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: e37c8fdded8fa5e141138903e502e2e1b0f1a0f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670604"
---
# <span data-ttu-id="ca965-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca965-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="ca965-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca965-102">SYNOPSIS</span></span>
<span data-ttu-id="ca965-103">Azure ExpressRoute áramkört kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="ca965-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="ca965-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca965-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca965-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca965-105">DESCRIPTION</span></span>
<span data-ttu-id="ca965-106">A **Get-AzExpressRouteCircuit** parancsmag az ExpressRoute-áramköri objektumnak az előfizetésből való visszakeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ca965-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="ca965-107">A visszaadott áramkör-objektum a ExpressRoute-áramkörön működő többi parancsmaghoz is használható.</span><span class="sxs-lookup"><span data-stu-id="ca965-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="ca965-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ca965-108">EXAMPLES</span></span>

### <span data-ttu-id="ca965-109">Példa 1: a ExpressRoute áramkör beszerzése</span><span class="sxs-lookup"><span data-stu-id="ca965-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="ca965-110">A "testrg" és a ResourceGroupName "teszt" nevű ExpressRoute-áramkör beszerzése</span><span class="sxs-lookup"><span data-stu-id="ca965-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="ca965-111">2. példa: a ExpressRoute-áramkörök listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="ca965-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="ca965-112">Az összes olyan ExpressRoute-áramkört kapja, akinek a neve "teszt" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="ca965-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="ca965-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca965-113">PARAMETERS</span></span>

### <span data-ttu-id="ca965-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca965-114">-DefaultProfile</span></span>
<span data-ttu-id="ca965-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca965-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca965-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca965-116">-Name</span></span>
<span data-ttu-id="ca965-117">A ExpressRoute áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="ca965-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="ca965-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca965-118">-ResourceGroupName</span></span>
<span data-ttu-id="ca965-119">Annak az erőforráscsoportnek a neve, amely a ExpressRoute áramkört tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ca965-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="ca965-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca965-120">CommonParameters</span></span>
<span data-ttu-id="ca965-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca965-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca965-122">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ca965-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca965-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca965-123">INPUTS</span></span>

### <span data-ttu-id="ca965-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ca965-124">System.String</span></span>

## <span data-ttu-id="ca965-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca965-125">OUTPUTS</span></span>

### <span data-ttu-id="ca965-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca965-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ca965-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca965-127">NOTES</span></span>

## <span data-ttu-id="ca965-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca965-128">RELATED LINKS</span></span>

[<span data-ttu-id="ca965-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca965-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="ca965-130">Új – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca965-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="ca965-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca965-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="ca965-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca965-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
