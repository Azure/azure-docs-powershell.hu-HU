---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0ef2870592411ce64847f8a4a58dabdebcc8235f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414713"
---
# <span data-ttu-id="23f3a-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="23f3a-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="23f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="23f3a-103">ExpressRoute-kapcsolati konfigurációt kap, amely az ExpressRouteCircuit privát társviszony-létesítésében van társítva.</span><span class="sxs-lookup"><span data-stu-id="23f3a-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="23f3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23f3a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23f3a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="23f3a-106">A **Get-AzExpressRouteCircuitConnectionConfig** parancsmag beolvassa egy ExpressRoute-kapcsolat magánjellegű társviszony-létesítéshez társított kapcsolati kapcsolatának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="23f3a-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="23f3a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="23f3a-108">1. példa: ExpressRoute-kapcsolat kapcsolatkonfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="23f3a-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="23f3a-109">2. példa: Az ExpressRoute-áramkörhöz társított kapcsolati erőforrás lekérte a kapcsolatcsoportot egy pipával</span><span class="sxs-lookup"><span data-stu-id="23f3a-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="23f3a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23f3a-110">PARAMETERS</span></span>

### <span data-ttu-id="23f3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f3a-111">-DefaultProfile</span></span>
<span data-ttu-id="23f3a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23f3a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f3a-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23f3a-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="23f3a-114">Az ExpressRoute-áramkör objektuma, amely az áramkör-kapcsolat konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="23f3a-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23f3a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="23f3a-115">-Name</span></span>
<span data-ttu-id="23f3a-116">A lekérni szükséges kapcsolati kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="23f3a-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f3a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f3a-117">CommonParameters</span></span>
<span data-ttu-id="23f3a-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f3a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f3a-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23f3a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f3a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23f3a-120">INPUTS</span></span>

### <span data-ttu-id="23f3a-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23f3a-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="23f3a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23f3a-122">OUTPUTS</span></span>

### <span data-ttu-id="23f3a-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="23f3a-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="23f3a-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23f3a-124">NOTES</span></span>

## <span data-ttu-id="23f3a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23f3a-125">RELATED LINKS</span></span>

[<span data-ttu-id="23f3a-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23f3a-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="23f3a-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="23f3a-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="23f3a-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="23f3a-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="23f3a-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="23f3a-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)


