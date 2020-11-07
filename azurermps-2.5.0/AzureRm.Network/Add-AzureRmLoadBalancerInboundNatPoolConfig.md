---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: b53b6ed8ba5b4a79ee1913040ef58e236c22c44d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850806"
---
# <span data-ttu-id="36d40-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="36d40-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="36d40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36d40-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d40-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36d40-103">SYNTAX</span></span>

### <span data-ttu-id="36d40-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36d40-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36d40-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="36d40-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36d40-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="36d40-106">DESCRIPTION</span></span>

## <span data-ttu-id="36d40-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36d40-107">EXAMPLES</span></span>

### <span data-ttu-id="36d40-108">1:</span><span class="sxs-lookup"><span data-stu-id="36d40-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="36d40-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36d40-109">PARAMETERS</span></span>

### <span data-ttu-id="36d40-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="36d40-110">-BackendPort</span></span>
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

### <span data-ttu-id="36d40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d40-111">-DefaultProfile</span></span>
<span data-ttu-id="36d40-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36d40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d40-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="36d40-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="36d40-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="36d40-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="36d40-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="36d40-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="36d40-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="36d40-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="36d40-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36d40-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="36d40-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36d40-118">-Name</span></span>
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

### <span data-ttu-id="36d40-119">-Protocol</span><span class="sxs-lookup"><span data-stu-id="36d40-119">-Protocol</span></span>
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

### <span data-ttu-id="36d40-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d40-120">CommonParameters</span></span>
<span data-ttu-id="36d40-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36d40-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d40-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d40-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d40-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d40-123">INPUTS</span></span>

### <span data-ttu-id="36d40-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36d40-124">PSLoadBalancer</span></span>
<span data-ttu-id="36d40-125">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="36d40-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="36d40-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d40-126">OUTPUTS</span></span>

### <span data-ttu-id="36d40-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36d40-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="36d40-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36d40-128">NOTES</span></span>

## <span data-ttu-id="36d40-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36d40-129">RELATED LINKS</span></span>

