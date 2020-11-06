---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504367"
---
# <span data-ttu-id="5fd2e-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fd2e-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="5fd2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fd2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd2e-103">ExpressRoute-áramköri kapcsolati konfigurációt kap, amely a ExpressRouteCircuit privát kinézetéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fd2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fd2e-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fd2e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fd2e-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd2e-106">A **Get-AzureRmExpressRouteCircuitConnectionConfig** parancsmag kikeresi a magánjellegű kapcsolattal rendelkező ExpressRoute-áramkörhöz társított áramköri kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="5fd2e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5fd2e-107">EXAMPLES</span></span>

### <span data-ttu-id="5fd2e-108">Példa 1: ExpressRoute-áramkör áramkör-kapcsolati konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="5fd2e-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5fd2e-109">2. példa: ExpressRoute-áramkörrel társított áramköri kapcsolati erőforrás csővezetékekkel való használata</span><span class="sxs-lookup"><span data-stu-id="5fd2e-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="5fd2e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fd2e-110">PARAMETERS</span></span>

### <span data-ttu-id="5fd2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd2e-111">-DefaultProfile</span></span>
<span data-ttu-id="5fd2e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd2e-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5fd2e-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5fd2e-114">Az áramköri kapcsolat konfigurációját tartalmazó ExpressRoute Circuit objektum.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="5fd2e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fd2e-115">-Name</span></span>
<span data-ttu-id="5fd2e-116">A lekérdezni kívánt áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd2e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd2e-117">CommonParameters</span></span>
<span data-ttu-id="5fd2e-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fd2e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd2e-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd2e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd2e-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fd2e-120">INPUTS</span></span>

### <span data-ttu-id="5fd2e-121">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5fd2e-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="5fd2e-122">Paraméterek: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5fd2e-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="5fd2e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fd2e-123">OUTPUTS</span></span>

### <span data-ttu-id="5fd2e-124">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="5fd2e-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="5fd2e-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fd2e-125">NOTES</span></span>

## <span data-ttu-id="5fd2e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fd2e-126">RELATED LINKS</span></span>

[<span data-ttu-id="5fd2e-127">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5fd2e-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5fd2e-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fd2e-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5fd2e-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fd2e-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5fd2e-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fd2e-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5fd2e-131">Új – AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fd2e-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
