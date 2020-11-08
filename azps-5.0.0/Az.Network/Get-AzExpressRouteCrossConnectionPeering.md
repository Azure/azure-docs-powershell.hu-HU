---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188131"
---
# <span data-ttu-id="8e87a-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8e87a-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="8e87a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e87a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e87a-103">Egy ExpressRoute-kapcsolaton keresztüli kapcsolati konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="8e87a-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="8e87a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e87a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e87a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e87a-105">DESCRIPTION</span></span>
<span data-ttu-id="8e87a-106">A **Get-AzExpressRouteCrossConnectionPeering** parancsmag kikeresi a ExpressRoute közötti kapcsolatok beállítását.</span><span class="sxs-lookup"><span data-stu-id="8e87a-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="8e87a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e87a-107">EXAMPLES</span></span>

### <span data-ttu-id="8e87a-108">Példa 1: egy ExpressRoute-kapcsolat társközi konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="8e87a-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="8e87a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e87a-109">PARAMETERS</span></span>

### <span data-ttu-id="8e87a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e87a-110">-DefaultProfile</span></span>
<span data-ttu-id="8e87a-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e87a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e87a-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8e87a-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="8e87a-113">A ExpressRoute-kapcsolat objektuma, amely a társközi konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8e87a-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e87a-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e87a-114">-Name</span></span>
<span data-ttu-id="8e87a-115">A beolvasni kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="8e87a-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e87a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e87a-116">CommonParameters</span></span>
<span data-ttu-id="8e87a-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e87a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e87a-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8e87a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e87a-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e87a-119">INPUTS</span></span>

### <span data-ttu-id="8e87a-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8e87a-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="8e87a-121">A ' ExpressRouteCrossConnection ' paraméter az "PSExpressRouteCrossConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8e87a-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="8e87a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e87a-122">OUTPUTS</span></span>

### <span data-ttu-id="8e87a-123">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="8e87a-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="8e87a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e87a-124">NOTES</span></span>

## <span data-ttu-id="8e87a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e87a-125">RELATED LINKS</span></span>

[<span data-ttu-id="8e87a-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8e87a-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="8e87a-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8e87a-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="8e87a-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8e87a-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="8e87a-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8e87a-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)