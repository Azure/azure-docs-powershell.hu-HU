---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a5cd44d1b4b7ac1a1494047affa721dd21d85919
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841829"
---
# <span data-ttu-id="6b58b-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6b58b-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="6b58b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b58b-102">SYNOPSIS</span></span>

## <span data-ttu-id="6b58b-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b58b-103">SYNTAX</span></span>

### <span data-ttu-id="6b58b-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b58b-104">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b58b-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6b58b-105">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b58b-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b58b-106">DESCRIPTION</span></span>

## <span data-ttu-id="6b58b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6b58b-107">EXAMPLES</span></span>

### <span data-ttu-id="6b58b-108">1:</span><span class="sxs-lookup"><span data-stu-id="6b58b-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="6b58b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b58b-109">PARAMETERS</span></span>

### <span data-ttu-id="6b58b-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6b58b-110">-BackendPort</span></span>
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

### <span data-ttu-id="6b58b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b58b-111">-DefaultProfile</span></span>
<span data-ttu-id="6b58b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b58b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b58b-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b58b-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="6b58b-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6b58b-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="6b58b-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="6b58b-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="6b58b-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="6b58b-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="6b58b-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6b58b-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="6b58b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b58b-118">-Name</span></span>
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

### <span data-ttu-id="6b58b-119">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6b58b-119">-Protocol</span></span>
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

### <span data-ttu-id="6b58b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b58b-120">CommonParameters</span></span>
<span data-ttu-id="6b58b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b58b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b58b-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b58b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b58b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b58b-123">INPUTS</span></span>

### <span data-ttu-id="6b58b-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6b58b-124">PSLoadBalancer</span></span>
<span data-ttu-id="6b58b-125">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6b58b-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6b58b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b58b-126">OUTPUTS</span></span>

### <span data-ttu-id="6b58b-127">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6b58b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6b58b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b58b-128">NOTES</span></span>

## <span data-ttu-id="6b58b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b58b-129">RELATED LINKS</span></span>

