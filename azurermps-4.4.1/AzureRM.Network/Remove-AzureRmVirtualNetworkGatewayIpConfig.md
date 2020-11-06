---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d721feb80598e343fc5757eceee90136bbc51ae9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505600"
---
# <span data-ttu-id="30227-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="30227-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="30227-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30227-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30227-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30227-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30227-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="30227-104">DESCRIPTION</span></span>

## <span data-ttu-id="30227-105">Példák</span><span class="sxs-lookup"><span data-stu-id="30227-105">EXAMPLES</span></span>

### <span data-ttu-id="30227-106">1:</span><span class="sxs-lookup"><span data-stu-id="30227-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="30227-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30227-107">PARAMETERS</span></span>

### <span data-ttu-id="30227-108">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30227-108">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30227-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30227-109">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="30227-110">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30227-110">-Confirm</span></span>
<span data-ttu-id="30227-111">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30227-111">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30227-112">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30227-112">-WhatIf</span></span>
<span data-ttu-id="30227-113">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30227-113">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30227-114">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30227-114">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30227-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30227-115">-DefaultProfile</span></span>
<span data-ttu-id="30227-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30227-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30227-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30227-117">CommonParameters</span></span>
<span data-ttu-id="30227-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30227-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30227-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30227-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30227-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30227-120">INPUTS</span></span>

### <span data-ttu-id="30227-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30227-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="30227-122">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="30227-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="30227-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30227-123">OUTPUTS</span></span>

### <span data-ttu-id="30227-124">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30227-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="30227-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30227-125">NOTES</span></span>

## <span data-ttu-id="30227-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30227-126">RELATED LINKS</span></span>

