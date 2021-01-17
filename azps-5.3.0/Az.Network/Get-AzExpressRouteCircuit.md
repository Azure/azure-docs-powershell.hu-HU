---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467369"
---
# <span data-ttu-id="987ca-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="987ca-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="987ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="987ca-102">SYNOPSIS</span></span>
<span data-ttu-id="987ca-103">Azure ExpressRoute-áramkört kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="987ca-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="987ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="987ca-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="987ca-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="987ca-105">DESCRIPTION</span></span>
<span data-ttu-id="987ca-106">A **Get-AzExpressRouteCircuit** parancsmaggal lekérhető egy ExpressRoute-áramköri objektum az előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="987ca-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="987ca-107">A visszaadott áramköri objektum használható az ExpressRoute-áramkörön működő más parancsmagok bemeneteként.</span><span class="sxs-lookup"><span data-stu-id="987ca-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="987ca-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="987ca-108">EXAMPLES</span></span>

### <span data-ttu-id="987ca-109">1. példa: Az ExpressRoute-áramkör lekérte</span><span class="sxs-lookup"><span data-stu-id="987ca-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="987ca-110">Adott ExpressRoute-áramkör létrehozása "testrg" névvel és ResourceGroupName "teszt" névvel</span><span class="sxs-lookup"><span data-stu-id="987ca-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="987ca-111">2. példa: Az ExpressRoute-áramkörök felsorolása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="987ca-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="987ca-112">Szerezze be az összes Olyan ExpressRoute-áramkört, amelynek a neve "teszt" névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="987ca-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="987ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="987ca-113">PARAMETERS</span></span>

### <span data-ttu-id="987ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987ca-114">-DefaultProfile</span></span>
<span data-ttu-id="987ca-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="987ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="987ca-116">-Name</span><span class="sxs-lookup"><span data-stu-id="987ca-116">-Name</span></span>
<span data-ttu-id="987ca-117">Az ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="987ca-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="987ca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="987ca-118">-ResourceGroupName</span></span>
<span data-ttu-id="987ca-119">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="987ca-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="987ca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987ca-120">CommonParameters</span></span>
<span data-ttu-id="987ca-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987ca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987ca-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="987ca-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987ca-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="987ca-123">INPUTS</span></span>

### <span data-ttu-id="987ca-124">System.String</span><span class="sxs-lookup"><span data-stu-id="987ca-124">System.String</span></span>

## <span data-ttu-id="987ca-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="987ca-125">OUTPUTS</span></span>

### <span data-ttu-id="987ca-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="987ca-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="987ca-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="987ca-127">NOTES</span></span>

## <span data-ttu-id="987ca-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="987ca-128">RELATED LINKS</span></span>

[<span data-ttu-id="987ca-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="987ca-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="987ca-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="987ca-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="987ca-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="987ca-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="987ca-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="987ca-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
