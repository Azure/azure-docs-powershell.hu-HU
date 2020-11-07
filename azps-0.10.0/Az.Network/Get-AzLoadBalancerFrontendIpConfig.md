---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a0b1acf49aa177d05be7361eedf644320b609797
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841637"
---
# <span data-ttu-id="65cc7-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="65cc7-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="65cc7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="65cc7-103">Beilleszti az előtér IP-konfigurációját egy terheléselosztó nézetben.</span><span class="sxs-lookup"><span data-stu-id="65cc7-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="65cc7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65cc7-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65cc7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="65cc7-106">A **Get-AzLoadBalancerFrontendIpConfig** parancsmag az előtér IP-konfigurációját, illetve az előtér IP-konfigurációinak listáját a terheléselosztásban kapja.</span><span class="sxs-lookup"><span data-stu-id="65cc7-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="65cc7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65cc7-107">EXAMPLES</span></span>

### <span data-ttu-id="65cc7-108">1. példa: az előtér IP-konfigurációjának beszerzése a terheléselosztó bővítményben</span><span class="sxs-lookup"><span data-stu-id="65cc7-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="65cc7-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="65cc7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="65cc7-110">A második parancs beilleszti az előtér-végponthoz társított IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="65cc7-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="65cc7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65cc7-111">PARAMETERS</span></span>

### <span data-ttu-id="65cc7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65cc7-112">-DefaultProfile</span></span>
<span data-ttu-id="65cc7-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65cc7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65cc7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65cc7-114">-LoadBalancer</span></span>
<span data-ttu-id="65cc7-115">Annak az IP-konfigurációnak a terheléselosztását adja meg, amely az előtér IP-konfigurációjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="65cc7-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65cc7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65cc7-116">-Name</span></span>
<span data-ttu-id="65cc7-117">Annak az IP-konfigurációnak a neve, amely az előtér IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="65cc7-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65cc7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65cc7-118">CommonParameters</span></span>
<span data-ttu-id="65cc7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65cc7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65cc7-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65cc7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65cc7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65cc7-121">INPUTS</span></span>

### <span data-ttu-id="65cc7-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65cc7-122">PSLoadBalancer</span></span>
<span data-ttu-id="65cc7-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="65cc7-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="65cc7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65cc7-124">OUTPUTS</span></span>

### <span data-ttu-id="65cc7-125">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65cc7-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="65cc7-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65cc7-126">NOTES</span></span>

## <span data-ttu-id="65cc7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65cc7-127">RELATED LINKS</span></span>

[<span data-ttu-id="65cc7-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="65cc7-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="65cc7-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65cc7-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="65cc7-130">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="65cc7-130">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="65cc7-131">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="65cc7-131">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="65cc7-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="65cc7-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


