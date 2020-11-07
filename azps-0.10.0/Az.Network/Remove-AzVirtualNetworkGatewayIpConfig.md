---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843745"
---
# <span data-ttu-id="97650-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="97650-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="97650-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97650-102">SYNOPSIS</span></span>

## <span data-ttu-id="97650-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97650-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97650-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="97650-104">DESCRIPTION</span></span>

## <span data-ttu-id="97650-105">Példák</span><span class="sxs-lookup"><span data-stu-id="97650-105">EXAMPLES</span></span>

### <span data-ttu-id="97650-106">1:</span><span class="sxs-lookup"><span data-stu-id="97650-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="97650-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97650-107">PARAMETERS</span></span>

### <span data-ttu-id="97650-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97650-108">-DefaultProfile</span></span>
<span data-ttu-id="97650-109">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97650-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97650-110">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97650-110">-Name</span></span>
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

### <span data-ttu-id="97650-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="97650-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="97650-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97650-112">-Confirm</span></span>
<span data-ttu-id="97650-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97650-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97650-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97650-114">-WhatIf</span></span>
<span data-ttu-id="97650-115">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97650-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97650-116">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97650-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97650-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97650-117">CommonParameters</span></span>
<span data-ttu-id="97650-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97650-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97650-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97650-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97650-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97650-120">INPUTS</span></span>

### <span data-ttu-id="97650-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="97650-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="97650-122">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="97650-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="97650-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97650-123">OUTPUTS</span></span>

### <span data-ttu-id="97650-124">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="97650-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="97650-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97650-125">NOTES</span></span>

## <span data-ttu-id="97650-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97650-126">RELATED LINKS</span></span>

