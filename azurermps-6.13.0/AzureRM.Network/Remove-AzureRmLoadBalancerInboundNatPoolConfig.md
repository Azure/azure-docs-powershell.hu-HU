---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491910"
---
# <span data-ttu-id="a9eef-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a9eef-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="a9eef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9eef-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9eef-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9eef-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9eef-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9eef-104">DESCRIPTION</span></span>

## <span data-ttu-id="a9eef-105">Példák</span><span class="sxs-lookup"><span data-stu-id="a9eef-105">EXAMPLES</span></span>

### <span data-ttu-id="a9eef-106">1: eltávolítás</span><span class="sxs-lookup"><span data-stu-id="a9eef-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="a9eef-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9eef-107">PARAMETERS</span></span>

### <span data-ttu-id="a9eef-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9eef-108">-DefaultProfile</span></span>
<span data-ttu-id="a9eef-109">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9eef-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9eef-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9eef-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eef-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9eef-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eef-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9eef-112">-Confirm</span></span>
<span data-ttu-id="a9eef-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9eef-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eef-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9eef-114">-WhatIf</span></span>
<span data-ttu-id="a9eef-115">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9eef-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9eef-116">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9eef-116">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9eef-117">CommonParameters</span></span>
<span data-ttu-id="a9eef-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9eef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9eef-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9eef-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9eef-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9eef-120">INPUTS</span></span>

### <span data-ttu-id="a9eef-121">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9eef-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a9eef-122">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9eef-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a9eef-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9eef-123">OUTPUTS</span></span>

### <span data-ttu-id="a9eef-124">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9eef-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a9eef-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9eef-125">NOTES</span></span>

## <span data-ttu-id="a9eef-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9eef-126">RELATED LINKS</span></span>
