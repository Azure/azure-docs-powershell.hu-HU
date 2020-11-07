---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 247470ee878a37968cd690d27f8e5e16047febbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849126"
---
# <span data-ttu-id="0d3ce-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0d3ce-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="0d3ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d3ce-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d3ce-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d3ce-103">SYNTAX</span></span>

### <span data-ttu-id="0d3ce-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d3ce-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d3ce-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0d3ce-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d3ce-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d3ce-106">DESCRIPTION</span></span>

## <span data-ttu-id="0d3ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0d3ce-107">EXAMPLES</span></span>

### <span data-ttu-id="0d3ce-108">1:</span><span class="sxs-lookup"><span data-stu-id="0d3ce-108">1:</span></span>
```

```

## <span data-ttu-id="0d3ce-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d3ce-109">PARAMETERS</span></span>

### <span data-ttu-id="0d3ce-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0d3ce-110">-BackendPort</span></span>
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

### <span data-ttu-id="0d3ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d3ce-111">-DefaultProfile</span></span>
<span data-ttu-id="0d3ce-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d3ce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d3ce-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d3ce-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="0d3ce-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0d3ce-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="0d3ce-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="0d3ce-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="0d3ce-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="0d3ce-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="0d3ce-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d3ce-117">-Name</span></span>
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

### <span data-ttu-id="0d3ce-118">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0d3ce-118">-Protocol</span></span>
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

### <span data-ttu-id="0d3ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3ce-119">CommonParameters</span></span>
<span data-ttu-id="0d3ce-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d3ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3ce-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d3ce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3ce-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d3ce-122">INPUTS</span></span>

## <span data-ttu-id="0d3ce-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d3ce-123">OUTPUTS</span></span>

### <span data-ttu-id="0d3ce-124">Microsoft. Azure. commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="0d3ce-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="0d3ce-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d3ce-125">NOTES</span></span>

## <span data-ttu-id="0d3ce-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d3ce-126">RELATED LINKS</span></span>

