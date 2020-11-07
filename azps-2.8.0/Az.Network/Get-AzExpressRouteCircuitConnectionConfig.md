---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 70badaebf0b6b8a35fd96cc20a54aab1ff316bef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837607"
---
# <span data-ttu-id="60acf-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60acf-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="60acf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60acf-102">SYNOPSIS</span></span>
<span data-ttu-id="60acf-103">ExpressRoute-áramköri kapcsolati konfigurációt kap, amely a ExpressRouteCircuit privát kinézetéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="60acf-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="60acf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60acf-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60acf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60acf-105">DESCRIPTION</span></span>
<span data-ttu-id="60acf-106">A **Get-AzExpressRouteCircuitConnectionConfig** parancsmag kikeresi a magánjellegű kapcsolattal rendelkező ExpressRoute-áramkörhöz társított áramköri kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="60acf-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="60acf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60acf-107">EXAMPLES</span></span>

### <span data-ttu-id="60acf-108">Példa 1: ExpressRoute-áramkör áramkör-kapcsolati konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="60acf-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="60acf-109">2. példa: ExpressRoute-áramkörrel társított áramköri kapcsolati erőforrás csővezetékekkel való használata</span><span class="sxs-lookup"><span data-stu-id="60acf-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="60acf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60acf-110">PARAMETERS</span></span>

### <span data-ttu-id="60acf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60acf-111">-DefaultProfile</span></span>
<span data-ttu-id="60acf-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60acf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60acf-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60acf-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="60acf-114">Az áramköri kapcsolat konfigurációját tartalmazó ExpressRoute Circuit objektum.</span><span class="sxs-lookup"><span data-stu-id="60acf-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="60acf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60acf-115">-Name</span></span>
<span data-ttu-id="60acf-116">A lekérdezni kívánt áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="60acf-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="60acf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60acf-117">CommonParameters</span></span>
<span data-ttu-id="60acf-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60acf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60acf-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="60acf-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60acf-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60acf-120">INPUTS</span></span>

### <span data-ttu-id="60acf-121">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60acf-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="60acf-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60acf-122">OUTPUTS</span></span>

### <span data-ttu-id="60acf-123">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="60acf-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="60acf-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60acf-124">NOTES</span></span>

## <span data-ttu-id="60acf-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60acf-125">RELATED LINKS</span></span>

[<span data-ttu-id="60acf-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60acf-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="60acf-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60acf-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60acf-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60acf-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60acf-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60acf-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60acf-130">Új – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60acf-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)