---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841153"
---
# <span data-ttu-id="1f746-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f746-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="1f746-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f746-102">SYNOPSIS</span></span>
<span data-ttu-id="1f746-103">Az előtér IP-konfigurációjának eltávolítása a terheléselosztásból.</span><span class="sxs-lookup"><span data-stu-id="1f746-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="1f746-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f746-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f746-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f746-105">DESCRIPTION</span></span>
<span data-ttu-id="1f746-106">A **Remove-AzLoadBalancerFrontendIpConfig** parancsmag az Azure Loader-ből eltávolítja az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1f746-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="1f746-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f746-107">EXAMPLES</span></span>

### <span data-ttu-id="1f746-108">1. példa: az előtér IP-konfigurációjának eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="1f746-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="1f746-109">Az első parancs megkapja az eltávolítani kívánt előtér-IP-konfigurációhoz társított terheléselosztó bővítményt, majd a $loadbalancer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1f746-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="1f746-110">A második parancs eltávolítja a kapcsolódó felületet az IP-konfigurációból $loadbalancer a terheléselosztó webhelyről.</span><span class="sxs-lookup"><span data-stu-id="1f746-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="1f746-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f746-111">PARAMETERS</span></span>

### <span data-ttu-id="1f746-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f746-112">-DefaultProfile</span></span>
<span data-ttu-id="1f746-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f746-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f746-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f746-114">-LoadBalancer</span></span>
<span data-ttu-id="1f746-115">Megadja az eltávolítandó előtér IP-konfigurációját tartalmazó terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="1f746-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="1f746-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f746-116">-Name</span></span>
<span data-ttu-id="1f746-117">Az eltávolítandó IP-cím konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f746-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="1f746-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f746-118">CommonParameters</span></span>
<span data-ttu-id="1f746-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f746-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f746-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f746-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f746-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f746-121">INPUTS</span></span>

### <span data-ttu-id="1f746-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f746-122">PSLoadBalancer</span></span>
<span data-ttu-id="1f746-123">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1f746-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1f746-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f746-124">OUTPUTS</span></span>

### <span data-ttu-id="1f746-125">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f746-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1f746-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f746-126">NOTES</span></span>

## <span data-ttu-id="1f746-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f746-127">RELATED LINKS</span></span>

[<span data-ttu-id="1f746-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f746-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f746-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f746-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1f746-130">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f746-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f746-131">Új – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f746-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f746-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f746-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


