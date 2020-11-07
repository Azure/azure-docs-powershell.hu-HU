---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850606"
---
# <span data-ttu-id="2dc31-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="2dc31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2dc31-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dc31-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2dc31-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc31-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="2dc31-104">DESCRIPTION</span></span>

## <span data-ttu-id="2dc31-105">Példák</span><span class="sxs-lookup"><span data-stu-id="2dc31-105">EXAMPLES</span></span>

### <span data-ttu-id="2dc31-106">1:</span><span class="sxs-lookup"><span data-stu-id="2dc31-106">1:</span></span>
```

```

## <span data-ttu-id="2dc31-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2dc31-107">PARAMETERS</span></span>

### <span data-ttu-id="2dc31-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dc31-108">-AsJob</span></span>
<span data-ttu-id="2dc31-109">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2dc31-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dc31-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc31-110">-DefaultProfile</span></span>
<span data-ttu-id="2dc31-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2dc31-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dc31-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="2dc31-112">-GatewayVip</span></span>
<span data-ttu-id="2dc31-113">Az átjáró VIP az adott átjáró alaphelyzetbe állításához (például Active-Active funkció engedélyezett átjárók esetén) Alapértelmezés szerint az átjáró elsődleges példánya alapértelmezés szerint vissza fog állítani, ha nem ad át értéket.</span><span class="sxs-lookup"><span data-stu-id="2dc31-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dc31-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dc31-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc31-115">CommonParameters</span></span>
<span data-ttu-id="2dc31-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2dc31-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc31-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc31-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc31-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dc31-118">INPUTS</span></span>

### <span data-ttu-id="2dc31-119">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="2dc31-119">String</span></span>
<span data-ttu-id="2dc31-120">A ' GatewayVip ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2dc31-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2dc31-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="2dc31-122">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2dc31-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="2dc31-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dc31-123">OUTPUTS</span></span>

### <span data-ttu-id="2dc31-124">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2dc31-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2dc31-125">NOTES</span></span>

## <span data-ttu-id="2dc31-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2dc31-126">RELATED LINKS</span></span>

[<span data-ttu-id="2dc31-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2dc31-128">Új – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2dc31-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2dc31-130">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2dc31-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2dc31-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


