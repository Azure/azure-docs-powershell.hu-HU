---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: b223cf62b536479b4c39d5852974698f2f38becf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679970"
---
# <span data-ttu-id="fbfa8-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="fbfa8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbfa8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfa8-103">Módosítja egy ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="fbfa8-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbfa8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbfa8-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbfa8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbfa8-105">DESCRIPTION</span></span>
<span data-ttu-id="fbfa8-106">A **set-AzureRmExpressRouteCircuit** parancsmag a módosított ExpressRoute-áramkört az Azure-ra menti.</span><span class="sxs-lookup"><span data-stu-id="fbfa8-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="fbfa8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fbfa8-107">EXAMPLES</span></span>

### <span data-ttu-id="fbfa8-108">Példa 1: ExpressRoute-áramkör ServiceKey módosítása</span><span class="sxs-lookup"><span data-stu-id="fbfa8-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="fbfa8-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbfa8-109">PARAMETERS</span></span>

### <span data-ttu-id="fbfa8-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="fbfa8-111">Azt a **ExpressRouteCircuit** objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="fbfa8-111">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfa8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfa8-112">-DefaultProfile</span></span>
<span data-ttu-id="fbfa8-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbfa8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbfa8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfa8-114">CommonParameters</span></span>
<span data-ttu-id="fbfa8-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbfa8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfa8-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbfa8-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfa8-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbfa8-117">INPUTS</span></span>

### <span data-ttu-id="fbfa8-118">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-118">PSExpressRouteCircuit</span></span>
<span data-ttu-id="fbfa8-119">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fbfa8-119">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="fbfa8-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbfa8-120">OUTPUTS</span></span>

### <span data-ttu-id="fbfa8-121">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fbfa8-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbfa8-122">NOTES</span></span>

## <span data-ttu-id="fbfa8-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbfa8-123">RELATED LINKS</span></span>

[<span data-ttu-id="fbfa8-124">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-124">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fbfa8-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-125">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fbfa8-126">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-126">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fbfa8-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fbfa8-127">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
