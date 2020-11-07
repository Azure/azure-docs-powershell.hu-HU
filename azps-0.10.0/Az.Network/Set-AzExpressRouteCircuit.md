---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843650"
---
# <span data-ttu-id="a638f-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a638f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a638f-102">SYNOPSIS</span></span>
<span data-ttu-id="a638f-103">Módosítja egy ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="a638f-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a638f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a638f-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a638f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a638f-105">DESCRIPTION</span></span>
<span data-ttu-id="a638f-106">A **set-AzExpressRouteCircuit** parancsmag a módosított ExpressRoute-áramkört az Azure-ra menti.</span><span class="sxs-lookup"><span data-stu-id="a638f-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="a638f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a638f-107">EXAMPLES</span></span>

### <span data-ttu-id="a638f-108">Példa 1: ExpressRoute-áramkör ServiceKey módosítása</span><span class="sxs-lookup"><span data-stu-id="a638f-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="a638f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a638f-109">PARAMETERS</span></span>

### <span data-ttu-id="a638f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a638f-110">-AsJob</span></span>
<span data-ttu-id="a638f-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a638f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a638f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a638f-112">-DefaultProfile</span></span>
<span data-ttu-id="a638f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a638f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a638f-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a638f-115">Azt a **ExpressRouteCircuit** objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="a638f-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a638f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a638f-116">CommonParameters</span></span>
<span data-ttu-id="a638f-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a638f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a638f-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a638f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a638f-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a638f-119">INPUTS</span></span>

### <span data-ttu-id="a638f-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="a638f-121">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a638f-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="a638f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a638f-122">OUTPUTS</span></span>

### <span data-ttu-id="a638f-123">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a638f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a638f-124">NOTES</span></span>

## <span data-ttu-id="a638f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a638f-125">RELATED LINKS</span></span>

[<span data-ttu-id="a638f-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a638f-127">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a638f-128">Új – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a638f-129">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a638f-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
