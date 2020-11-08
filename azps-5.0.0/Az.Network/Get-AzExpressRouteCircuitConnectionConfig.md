---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195574"
---
# <span data-ttu-id="7c300-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c300-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="7c300-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c300-102">SYNOPSIS</span></span>
<span data-ttu-id="7c300-103">ExpressRoute-áramköri kapcsolati konfigurációt kap, amely a ExpressRouteCircuit privát kinézetéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="7c300-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="7c300-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c300-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c300-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c300-105">DESCRIPTION</span></span>
<span data-ttu-id="7c300-106">A **Get-AzExpressRouteCircuitConnectionConfig** parancsmag kikeresi a magánjellegű kapcsolattal rendelkező ExpressRoute-áramkörhöz társított áramköri kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7c300-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7c300-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c300-107">EXAMPLES</span></span>

### <span data-ttu-id="7c300-108">Példa 1: ExpressRoute-áramkör áramkör-kapcsolati konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="7c300-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="7c300-109">2. példa: ExpressRoute-áramkörrel társított áramköri kapcsolati erőforrás csővezetékekkel való használata</span><span class="sxs-lookup"><span data-stu-id="7c300-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="7c300-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c300-110">PARAMETERS</span></span>

### <span data-ttu-id="7c300-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c300-111">-DefaultProfile</span></span>
<span data-ttu-id="7c300-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c300-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c300-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7c300-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7c300-114">Az áramköri kapcsolat konfigurációját tartalmazó ExpressRoute Circuit objektum.</span><span class="sxs-lookup"><span data-stu-id="7c300-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="7c300-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c300-115">-Name</span></span>
<span data-ttu-id="7c300-116">A lekérdezni kívánt áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="7c300-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="7c300-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c300-117">CommonParameters</span></span>
<span data-ttu-id="7c300-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c300-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c300-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c300-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c300-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c300-120">INPUTS</span></span>

### <span data-ttu-id="7c300-121">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7c300-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7c300-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c300-122">OUTPUTS</span></span>

### <span data-ttu-id="7c300-123">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="7c300-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="7c300-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c300-124">NOTES</span></span>

## <span data-ttu-id="7c300-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c300-125">RELATED LINKS</span></span>

[<span data-ttu-id="7c300-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7c300-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7c300-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c300-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7c300-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c300-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7c300-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c300-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7c300-130">Új – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c300-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)