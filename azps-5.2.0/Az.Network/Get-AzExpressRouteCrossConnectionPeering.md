---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329753"
---
# <span data-ttu-id="7e3f7-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7e3f7-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="7e3f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3f7-103">ExpressRoute-kapcsolatközi társviszony-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="7e3f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e3f7-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e3f7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e3f7-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3f7-106">A **Get-AzExpressRouteCrossConnectionPeering** parancsmag beolvassa egy társviszony konfigurációját egy ExpressRoute-keresztkapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7e3f7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e3f7-107">EXAMPLES</span></span>

### <span data-ttu-id="7e3f7-108">1. példa: Az ExpressRoute-kapcsolat társviszony-konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="7e3f7-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="7e3f7-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e3f7-109">PARAMETERS</span></span>

### <span data-ttu-id="7e3f7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3f7-110">-DefaultProfile</span></span>
<span data-ttu-id="7e3f7-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e3f7-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e3f7-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7e3f7-113">Az ExpressRoute-kapcsolati objektum, amely a társviszony-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="7e3f7-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7e3f7-114">-Name</span></span>
<span data-ttu-id="7e3f7-115">A visszakeresni szükséges társviszony-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="7e3f7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3f7-116">CommonParameters</span></span>
<span data-ttu-id="7e3f7-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3f7-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e3f7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3f7-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e3f7-119">INPUTS</span></span>

### <span data-ttu-id="7e3f7-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e3f7-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="7e3f7-121">Az "ExpressRouteCrossConnection" paraméter a "PSExpressRouteCrossConnection" típusú értéket fogadja el a folyamatból.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="7e3f7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e3f7-122">OUTPUTS</span></span>

### <span data-ttu-id="7e3f7-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="7e3f7-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="7e3f7-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e3f7-124">NOTES</span></span>

## <span data-ttu-id="7e3f7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e3f7-125">RELATED LINKS</span></span>

[<span data-ttu-id="7e3f7-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7e3f7-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7e3f7-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7e3f7-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7e3f7-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e3f7-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="7e3f7-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e3f7-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
