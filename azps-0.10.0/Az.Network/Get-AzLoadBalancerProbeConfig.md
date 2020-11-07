---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: bf106b9fbe4c8f069f2d7b5b1b2a9beae95cd51b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841610"
---
# <span data-ttu-id="54b24-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54b24-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="54b24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54b24-102">SYNOPSIS</span></span>
<span data-ttu-id="54b24-103">Kinyeri a szonda konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="54b24-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="54b24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54b24-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54b24-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54b24-105">DESCRIPTION</span></span>
<span data-ttu-id="54b24-106">A **Get-AzLoadBalancerProbeConfig** parancsmag egy vagy több szonda-konfigurációt kap a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="54b24-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="54b24-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54b24-107">EXAMPLES</span></span>

### <span data-ttu-id="54b24-108">1. példa: a terheléselosztó szonda-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="54b24-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="54b24-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="54b24-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="54b24-110">A második parancs beolvassa a MyProbe nevű társított szonda-konfigurációt a $slb terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="54b24-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="54b24-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54b24-111">PARAMETERS</span></span>

### <span data-ttu-id="54b24-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b24-112">-DefaultProfile</span></span>
<span data-ttu-id="54b24-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54b24-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54b24-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54b24-114">-LoadBalancer</span></span>
<span data-ttu-id="54b24-115">A szonda konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="54b24-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="54b24-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54b24-116">-Name</span></span>
<span data-ttu-id="54b24-117">A beszerzéshez használandó szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54b24-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="54b24-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b24-118">CommonParameters</span></span>
<span data-ttu-id="54b24-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54b24-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b24-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b24-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b24-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54b24-121">INPUTS</span></span>

### <span data-ttu-id="54b24-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54b24-122">PSLoadBalancer</span></span>
<span data-ttu-id="54b24-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="54b24-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="54b24-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54b24-124">OUTPUTS</span></span>

### <span data-ttu-id="54b24-125">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="54b24-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="54b24-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54b24-126">NOTES</span></span>

## <span data-ttu-id="54b24-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54b24-127">RELATED LINKS</span></span>

[<span data-ttu-id="54b24-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54b24-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="54b24-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54b24-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="54b24-130">Új – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54b24-130">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="54b24-131">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54b24-131">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="54b24-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54b24-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


