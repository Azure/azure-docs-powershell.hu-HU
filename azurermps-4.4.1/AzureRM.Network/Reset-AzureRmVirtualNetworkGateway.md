---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679977"
---
# <span data-ttu-id="e1a53-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="e1a53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1a53-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a53-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1a53-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1a53-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1a53-104">DESCRIPTION</span></span>

## <span data-ttu-id="e1a53-105">Példák</span><span class="sxs-lookup"><span data-stu-id="e1a53-105">EXAMPLES</span></span>

## <span data-ttu-id="e1a53-106">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1a53-106">PARAMETERS</span></span>

### <span data-ttu-id="e1a53-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="e1a53-107">-GatewayVip</span></span>
<span data-ttu-id="e1a53-108">Az átjáró VIP az adott átjáró alaphelyzetbe állításához (például Active-Active funkció engedélyezett átjárók esetén) Alapértelmezés szerint az átjáró elsődleges példánya alapértelmezés szerint vissza fog állítani, ha nem ad át értéket.</span><span class="sxs-lookup"><span data-stu-id="e1a53-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a53-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a53-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a53-110">-DefaultProfile</span></span>
<span data-ttu-id="e1a53-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1a53-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1a53-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a53-112">CommonParameters</span></span>
<span data-ttu-id="e1a53-113">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1a53-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a53-114">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a53-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a53-115">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a53-115">INPUTS</span></span>

### <span data-ttu-id="e1a53-116">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e1a53-116">String</span></span>
<span data-ttu-id="e1a53-117">A ' GatewayVip ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e1a53-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e1a53-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="e1a53-119">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e1a53-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="e1a53-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a53-120">OUTPUTS</span></span>

### <span data-ttu-id="e1a53-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e1a53-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1a53-122">NOTES</span></span>

## <span data-ttu-id="e1a53-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1a53-123">RELATED LINKS</span></span>

[<span data-ttu-id="e1a53-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e1a53-125">Új – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e1a53-126">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e1a53-127">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e1a53-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1a53-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


