---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 815f7d3fdc0f058f2abfce5687b129054814adab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680134"
---
# <span data-ttu-id="f7b6f-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="f7b6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7b6f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7b6f-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7b6f-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7b6f-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7b6f-104">DESCRIPTION</span></span>

## <span data-ttu-id="f7b6f-105">Példák</span><span class="sxs-lookup"><span data-stu-id="f7b6f-105">EXAMPLES</span></span>

## <span data-ttu-id="f7b6f-106">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7b6f-106">PARAMETERS</span></span>

### <span data-ttu-id="f7b6f-107">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7b6f-107">-AsJob</span></span>
<span data-ttu-id="f7b6f-108">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f7b6f-108">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7b6f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b6f-109">-DefaultProfile</span></span>
<span data-ttu-id="f7b6f-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7b6f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7b6f-111">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="f7b6f-111">-GatewayVip</span></span>
<span data-ttu-id="f7b6f-112">Az átjáró VIP az adott átjáró alaphelyzetbe állításához (például Active-Active funkció engedélyezett átjárók esetén) Alapértelmezés szerint az átjáró elsődleges példánya alapértelmezés szerint vissza fog állítani, ha nem ad át értéket.</span><span class="sxs-lookup"><span data-stu-id="f7b6f-112">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="f7b6f-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="f7b6f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b6f-114">CommonParameters</span></span>
<span data-ttu-id="f7b6f-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7b6f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b6f-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b6f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b6f-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b6f-117">INPUTS</span></span>

### <span data-ttu-id="f7b6f-118">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f7b6f-118">String</span></span>
<span data-ttu-id="f7b6f-119">A ' GatewayVip ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f7b6f-119">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="f7b6f-120">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-120">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f7b6f-121">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f7b6f-121">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="f7b6f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b6f-122">OUTPUTS</span></span>

### <span data-ttu-id="f7b6f-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f7b6f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7b6f-124">NOTES</span></span>

## <span data-ttu-id="f7b6f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7b6f-125">RELATED LINKS</span></span>

[<span data-ttu-id="f7b6f-126">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-126">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f7b6f-127">Új – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-127">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f7b6f-128">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-128">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f7b6f-129">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-129">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f7b6f-130">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7b6f-130">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


