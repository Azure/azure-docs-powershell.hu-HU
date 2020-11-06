---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503487"
---
# <span data-ttu-id="6e4be-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="6e4be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e4be-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4be-103">A virtuális hálózat átjárójának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="6e4be-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e4be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e4be-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e4be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e4be-105">DESCRIPTION</span></span>
<span data-ttu-id="6e4be-106">A virtuális hálózat átjárójának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="6e4be-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="6e4be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e4be-107">EXAMPLES</span></span>

### <span data-ttu-id="6e4be-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="6e4be-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="6e4be-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e4be-109">PARAMETERS</span></span>

### <span data-ttu-id="6e4be-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e4be-110">-AsJob</span></span>
<span data-ttu-id="6e4be-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6e4be-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e4be-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4be-112">-DefaultProfile</span></span>
<span data-ttu-id="6e4be-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e4be-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e4be-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="6e4be-114">-GatewayVip</span></span>
<span data-ttu-id="6e4be-115">Az átjáró VIP az adott átjáró alaphelyzetbe állításához (például Active-Active funkció engedélyezett átjárók esetén) Alapértelmezés szerint az átjáró elsődleges példánya alapértelmezés szerint vissza fog állítani, ha nem ad át értéket.</span><span class="sxs-lookup"><span data-stu-id="6e4be-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="6e4be-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="6e4be-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4be-117">CommonParameters</span></span>
<span data-ttu-id="6e4be-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e4be-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4be-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e4be-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4be-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e4be-120">INPUTS</span></span>

### <span data-ttu-id="6e4be-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="6e4be-122">Paraméterek: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e4be-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="6e4be-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4be-123">System.String</span></span>
<span data-ttu-id="6e4be-124">Paraméterek: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e4be-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="6e4be-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e4be-125">OUTPUTS</span></span>

### <span data-ttu-id="6e4be-126">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6e4be-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e4be-127">NOTES</span></span>

## <span data-ttu-id="6e4be-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e4be-128">RELATED LINKS</span></span>

[<span data-ttu-id="6e4be-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6e4be-130">Új – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6e4be-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6e4be-132">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6e4be-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e4be-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


