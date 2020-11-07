---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848701"
---
# <span data-ttu-id="836f3-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="836f3-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="836f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="836f3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="836f3-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="836f3-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="836f3-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="836f3-104">DESCRIPTION</span></span>

## <span data-ttu-id="836f3-105">Példák</span><span class="sxs-lookup"><span data-stu-id="836f3-105">EXAMPLES</span></span>

### <span data-ttu-id="836f3-106">1:</span><span class="sxs-lookup"><span data-stu-id="836f3-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="836f3-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="836f3-107">PARAMETERS</span></span>

### <span data-ttu-id="836f3-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836f3-108">-DefaultProfile</span></span>
<span data-ttu-id="836f3-109">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="836f3-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="836f3-110">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="836f3-110">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836f3-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="836f3-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="836f3-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="836f3-112">-Confirm</span></span>
<span data-ttu-id="836f3-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="836f3-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836f3-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="836f3-114">-WhatIf</span></span>
<span data-ttu-id="836f3-115">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="836f3-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="836f3-116">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="836f3-116">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836f3-117">CommonParameters</span></span>
<span data-ttu-id="836f3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="836f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836f3-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836f3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836f3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="836f3-120">INPUTS</span></span>

### <span data-ttu-id="836f3-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="836f3-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="836f3-122">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="836f3-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="836f3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="836f3-123">OUTPUTS</span></span>

### <span data-ttu-id="836f3-124">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="836f3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="836f3-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="836f3-125">NOTES</span></span>

## <span data-ttu-id="836f3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="836f3-126">RELATED LINKS</span></span>

