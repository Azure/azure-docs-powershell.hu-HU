---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: e0999a5dc61574d600daf113e1641483c8a8bd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504067"
---
# <span data-ttu-id="9023c-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9023c-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="9023c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9023c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9023c-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9023c-103">SYNTAX</span></span>

### <span data-ttu-id="9023c-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9023c-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9023c-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9023c-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9023c-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="9023c-106">DESCRIPTION</span></span>

## <span data-ttu-id="9023c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9023c-107">EXAMPLES</span></span>

### <span data-ttu-id="9023c-108">1:</span><span class="sxs-lookup"><span data-stu-id="9023c-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9023c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9023c-109">PARAMETERS</span></span>

### <span data-ttu-id="9023c-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9023c-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-111">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9023c-111">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-112">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9023c-112">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-113">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="9023c-113">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-114">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="9023c-114">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9023c-115">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9023c-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9023c-117">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9023c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9023c-118">-DefaultProfile</span></span>
<span data-ttu-id="9023c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9023c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9023c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9023c-120">CommonParameters</span></span>
<span data-ttu-id="9023c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9023c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9023c-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9023c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9023c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9023c-123">INPUTS</span></span>

### <span data-ttu-id="9023c-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9023c-124">PSLoadBalancer</span></span>
<span data-ttu-id="9023c-125">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9023c-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9023c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9023c-126">OUTPUTS</span></span>

### <span data-ttu-id="9023c-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9023c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9023c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9023c-128">NOTES</span></span>

## <span data-ttu-id="9023c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9023c-129">RELATED LINKS</span></span>

