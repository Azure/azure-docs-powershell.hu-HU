---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 070680c1dc1c9fd091b311888867cda3f844ce4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495936"
---
# <span data-ttu-id="69dc2-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69dc2-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="69dc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="69dc2-103">Beilleszti az előtér IP-konfigurációját egy terheléselosztó nézetben.</span><span class="sxs-lookup"><span data-stu-id="69dc2-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69dc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69dc2-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69dc2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="69dc2-106">A **Get-AzureRmLoadBalancerFrontendIpConfig** parancsmag az előtér IP-konfigurációját, illetve az előtér IP-konfigurációinak listáját a terheléselosztásban kapja.</span><span class="sxs-lookup"><span data-stu-id="69dc2-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="69dc2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69dc2-107">EXAMPLES</span></span>

### <span data-ttu-id="69dc2-108">1. példa: az előtér IP-konfigurációjának beszerzése a terheléselosztó bővítményben</span><span class="sxs-lookup"><span data-stu-id="69dc2-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="69dc2-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="69dc2-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="69dc2-110">A második parancs beilleszti az előtér-végponthoz társított IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="69dc2-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="69dc2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69dc2-111">PARAMETERS</span></span>

### <span data-ttu-id="69dc2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dc2-112">-DefaultProfile</span></span>
<span data-ttu-id="69dc2-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69dc2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69dc2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69dc2-114">-LoadBalancer</span></span>
<span data-ttu-id="69dc2-115">Annak az IP-konfigurációnak a terheléselosztását adja meg, amely az előtér IP-konfigurációjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="69dc2-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="69dc2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69dc2-116">-Name</span></span>
<span data-ttu-id="69dc2-117">Annak az IP-konfigurációnak a neve, amely az előtér IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="69dc2-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="69dc2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dc2-118">CommonParameters</span></span>
<span data-ttu-id="69dc2-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69dc2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dc2-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69dc2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dc2-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69dc2-121">INPUTS</span></span>

### <span data-ttu-id="69dc2-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69dc2-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="69dc2-123">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69dc2-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="69dc2-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69dc2-124">OUTPUTS</span></span>

### <span data-ttu-id="69dc2-125">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="69dc2-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="69dc2-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69dc2-126">NOTES</span></span>

## <span data-ttu-id="69dc2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69dc2-127">RELATED LINKS</span></span>

[<span data-ttu-id="69dc2-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69dc2-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="69dc2-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69dc2-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="69dc2-130">Új – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69dc2-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="69dc2-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69dc2-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="69dc2-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69dc2-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


