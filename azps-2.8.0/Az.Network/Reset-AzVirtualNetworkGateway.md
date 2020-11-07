---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 59f4a96c324a9743c876cf987e1347bbe0c8d946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837058"
---
# <span data-ttu-id="3d640-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="3d640-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d640-102">SYNOPSIS</span></span>
<span data-ttu-id="3d640-103">A virtuális hálózat átjárójának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="3d640-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="3d640-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d640-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d640-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d640-105">DESCRIPTION</span></span>
<span data-ttu-id="3d640-106">A virtuális hálózat átjárójának alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="3d640-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="3d640-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3d640-107">EXAMPLES</span></span>

### <span data-ttu-id="3d640-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="3d640-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="3d640-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d640-109">PARAMETERS</span></span>

### <span data-ttu-id="3d640-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d640-110">-AsJob</span></span>
<span data-ttu-id="3d640-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3d640-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d640-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d640-112">-DefaultProfile</span></span>
<span data-ttu-id="3d640-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d640-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d640-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="3d640-114">-GatewayVip</span></span>
<span data-ttu-id="3d640-115">Az átjáró VIP az adott átjáró alaphelyzetbe állításához (például Active-Active funkció engedélyezett átjárók esetén) Alapértelmezés szerint az átjáró elsődleges példánya alapértelmezés szerint vissza fog állítani, ha nem ad át értéket.</span><span class="sxs-lookup"><span data-stu-id="3d640-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="3d640-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="3d640-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d640-117">CommonParameters</span></span>
<span data-ttu-id="3d640-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d640-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d640-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d640-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d640-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d640-120">INPUTS</span></span>

### <span data-ttu-id="3d640-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="3d640-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3d640-122">System.String</span></span>

## <span data-ttu-id="3d640-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d640-123">OUTPUTS</span></span>

### <span data-ttu-id="3d640-124">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3d640-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d640-125">NOTES</span></span>

## <span data-ttu-id="3d640-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d640-126">RELATED LINKS</span></span>

[<span data-ttu-id="3d640-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3d640-128">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3d640-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3d640-130">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3d640-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d640-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
