---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: d893ec451c99bded8320e5949d052aeb856a5d56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494451"
---
# <span data-ttu-id="b39aa-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b39aa-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b39aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b39aa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b39aa-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b39aa-103">SYNTAX</span></span>

### <span data-ttu-id="b39aa-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b39aa-104">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b39aa-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b39aa-105">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b39aa-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b39aa-106">DESCRIPTION</span></span>

## <span data-ttu-id="b39aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b39aa-107">EXAMPLES</span></span>

### <span data-ttu-id="b39aa-108">1:</span><span class="sxs-lookup"><span data-stu-id="b39aa-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b39aa-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b39aa-109">PARAMETERS</span></span>

### <span data-ttu-id="b39aa-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b39aa-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39aa-111">-DefaultProfile</span></span>
<span data-ttu-id="b39aa-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b39aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b39aa-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b39aa-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39aa-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b39aa-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39aa-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="b39aa-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39aa-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="b39aa-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39aa-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b39aa-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="b39aa-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b39aa-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39aa-119">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b39aa-119">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39aa-120">CommonParameters</span></span>
<span data-ttu-id="b39aa-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b39aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39aa-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b39aa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39aa-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b39aa-123">INPUTS</span></span>

### <span data-ttu-id="b39aa-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b39aa-124">PSLoadBalancer</span></span>
<span data-ttu-id="b39aa-125">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b39aa-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b39aa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b39aa-126">OUTPUTS</span></span>

### <span data-ttu-id="b39aa-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b39aa-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b39aa-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b39aa-128">NOTES</span></span>

## <span data-ttu-id="b39aa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b39aa-129">RELATED LINKS</span></span>

[<span data-ttu-id="b39aa-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b39aa-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b39aa-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b39aa-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b39aa-132">Új – AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b39aa-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b39aa-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b39aa-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


