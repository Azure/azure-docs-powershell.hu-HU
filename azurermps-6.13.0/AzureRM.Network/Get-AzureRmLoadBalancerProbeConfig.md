---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 87722e7f639e3a9e2ca135196bceff75c61abddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680809"
---
# <span data-ttu-id="02808-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="02808-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="02808-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02808-102">SYNOPSIS</span></span>
<span data-ttu-id="02808-103">Kinyeri a szonda konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="02808-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02808-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02808-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02808-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02808-105">DESCRIPTION</span></span>
<span data-ttu-id="02808-106">A **Get-AzureRmLoadBalancerProbeConfig** parancsmag egy vagy több szonda-konfigurációt kap a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="02808-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="02808-107">Példák</span><span class="sxs-lookup"><span data-stu-id="02808-107">EXAMPLES</span></span>

### <span data-ttu-id="02808-108">1. példa: a terheléselosztó szonda-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="02808-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="02808-109">Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.</span><span class="sxs-lookup"><span data-stu-id="02808-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="02808-110">A második parancs beolvassa a MyProbe nevű társított szonda-konfigurációt a $slb terheléselosztó listájából.</span><span class="sxs-lookup"><span data-stu-id="02808-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="02808-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02808-111">PARAMETERS</span></span>

### <span data-ttu-id="02808-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02808-112">-DefaultProfile</span></span>
<span data-ttu-id="02808-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02808-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02808-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02808-114">-LoadBalancer</span></span>
<span data-ttu-id="02808-115">A szonda konfigurációjának megfelelő terheléselosztást adja meg.</span><span class="sxs-lookup"><span data-stu-id="02808-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="02808-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02808-116">-Name</span></span>
<span data-ttu-id="02808-117">A beszerzéshez használandó szonda-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02808-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="02808-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02808-118">CommonParameters</span></span>
<span data-ttu-id="02808-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02808-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02808-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02808-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02808-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02808-121">INPUTS</span></span>

### <span data-ttu-id="02808-122">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02808-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="02808-123">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02808-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="02808-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02808-124">OUTPUTS</span></span>

### <span data-ttu-id="02808-125">Microsoft. Azure. commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="02808-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="02808-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02808-126">NOTES</span></span>

## <span data-ttu-id="02808-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02808-127">RELATED LINKS</span></span>

[<span data-ttu-id="02808-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="02808-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="02808-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02808-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="02808-130">Új – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="02808-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="02808-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="02808-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="02808-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="02808-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


