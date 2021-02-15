---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151498"
---
# <span data-ttu-id="0f767-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="0f767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f767-102">SYNOPSIS</span></span>
<span data-ttu-id="0f767-103">A virtuális hálózati átjáró alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="0f767-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="0f767-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f767-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f767-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f767-105">DESCRIPTION</span></span>
<span data-ttu-id="0f767-106">A virtuális hálózati átjáró alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="0f767-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="0f767-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f767-107">EXAMPLES</span></span>

### <span data-ttu-id="0f767-108">1. példa:</span><span class="sxs-lookup"><span data-stu-id="0f767-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="0f767-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f767-109">PARAMETERS</span></span>

### <span data-ttu-id="0f767-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f767-110">-AsJob</span></span>
<span data-ttu-id="0f767-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f767-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f767-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f767-112">-DefaultProfile</span></span>
<span data-ttu-id="0f767-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f767-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f767-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="0f767-114">-GatewayVip</span></span>
<span data-ttu-id="0f767-115">Az átjáróhoz való különleges átjárópéldány alaphelyzetbe állítása érdekében (például egy szolgáltatás által engedélyezett átjárók Active-Active esetén).) Alapértelmezés szerint az átjáró elsődleges példánya alaphelyzetbe áll, ha nem ad át értéket.</span><span class="sxs-lookup"><span data-stu-id="0f767-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="0f767-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="0f767-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f767-117">CommonParameters</span></span>
<span data-ttu-id="0f767-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f767-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f767-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f767-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f767-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f767-120">INPUTS</span></span>

### <span data-ttu-id="0f767-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="0f767-122">System.String</span><span class="sxs-lookup"><span data-stu-id="0f767-122">System.String</span></span>

## <span data-ttu-id="0f767-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f767-123">OUTPUTS</span></span>

### <span data-ttu-id="0f767-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0f767-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f767-125">NOTES</span></span>

## <span data-ttu-id="0f767-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f767-126">RELATED LINKS</span></span>

[<span data-ttu-id="0f767-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f767-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f767-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f767-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f767-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f767-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
