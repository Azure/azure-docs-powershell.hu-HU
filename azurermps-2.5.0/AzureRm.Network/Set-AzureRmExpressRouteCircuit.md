---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: a37502abcee157e9666a49ea5db5d2afe206aa8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850333"
---
# <span data-ttu-id="cb15d-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="cb15d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb15d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb15d-103">Módosítja egy ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="cb15d-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb15d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb15d-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb15d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb15d-105">DESCRIPTION</span></span>
<span data-ttu-id="cb15d-106">A **set-AzureRmExpressRouteCircuit** parancsmag a módosított ExpressRoute-áramkört az Azure-ra menti.</span><span class="sxs-lookup"><span data-stu-id="cb15d-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="cb15d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cb15d-107">EXAMPLES</span></span>

### <span data-ttu-id="cb15d-108">Példa 1: ExpressRoute-áramkör ServiceKey módosítása</span><span class="sxs-lookup"><span data-stu-id="cb15d-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="cb15d-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb15d-109">PARAMETERS</span></span>

### <span data-ttu-id="cb15d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb15d-110">-AsJob</span></span>
<span data-ttu-id="cb15d-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cb15d-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb15d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb15d-112">-DefaultProfile</span></span>
<span data-ttu-id="cb15d-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb15d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb15d-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cb15d-115">Azt a **ExpressRouteCircuit** objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="cb15d-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb15d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb15d-116">CommonParameters</span></span>
<span data-ttu-id="cb15d-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb15d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb15d-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb15d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb15d-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb15d-119">INPUTS</span></span>

### <span data-ttu-id="cb15d-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="cb15d-121">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cb15d-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="cb15d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb15d-122">OUTPUTS</span></span>

### <span data-ttu-id="cb15d-123">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cb15d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb15d-124">NOTES</span></span>

## <span data-ttu-id="cb15d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb15d-125">RELATED LINKS</span></span>

[<span data-ttu-id="cb15d-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="cb15d-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="cb15d-128">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="cb15d-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb15d-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
