---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013935"
---
# <span data-ttu-id="d4c96-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d4c96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4c96-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c96-103">A virtuális hálózat átjárójának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="d4c96-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="d4c96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4c96-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4c96-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4c96-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c96-106">A virtuális hálózat átjárójának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="d4c96-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="d4c96-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d4c96-107">EXAMPLES</span></span>

### <span data-ttu-id="d4c96-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="d4c96-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="d4c96-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4c96-109">PARAMETERS</span></span>

### <span data-ttu-id="d4c96-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4c96-110">-AsJob</span></span>
<span data-ttu-id="d4c96-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d4c96-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c96-112">-DefaultProfile</span></span>
<span data-ttu-id="d4c96-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4c96-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c96-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="d4c96-114">-GatewayVip</span></span>
<span data-ttu-id="d4c96-115">Az átjáró VIP az adott átjáró alaphelyzetbe állításához (például Active-Active funkció engedélyezett átjárók esetén) Alapértelmezés szerint az átjáró elsődleges példánya alapértelmezés szerint vissza fog állítani, ha nem ad át értéket.</span><span class="sxs-lookup"><span data-stu-id="d4c96-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="d4c96-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="d4c96-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c96-117">CommonParameters</span></span>
<span data-ttu-id="d4c96-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4c96-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c96-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c96-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c96-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4c96-120">INPUTS</span></span>

### <span data-ttu-id="d4c96-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d4c96-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d4c96-122">System.String</span></span>

## <span data-ttu-id="d4c96-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4c96-123">OUTPUTS</span></span>

### <span data-ttu-id="d4c96-124">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d4c96-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4c96-125">NOTES</span></span>

## <span data-ttu-id="d4c96-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4c96-126">RELATED LINKS</span></span>

[<span data-ttu-id="d4c96-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d4c96-128">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d4c96-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d4c96-130">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d4c96-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4c96-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
