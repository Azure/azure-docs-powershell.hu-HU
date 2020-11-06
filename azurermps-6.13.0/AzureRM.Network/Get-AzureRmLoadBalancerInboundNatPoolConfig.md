---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dbd49a948108d23c0f824adaea2e06105152a36b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498331"
---
# <span data-ttu-id="5b952-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5b952-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="5b952-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b952-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b952-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b952-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b952-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b952-104">DESCRIPTION</span></span>

## <span data-ttu-id="5b952-105">Példák</span><span class="sxs-lookup"><span data-stu-id="5b952-105">EXAMPLES</span></span>

### <span data-ttu-id="5b952-106">1: Get</span><span class="sxs-lookup"><span data-stu-id="5b952-106">1: Get</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzureRmLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="5b952-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b952-107">PARAMETERS</span></span>

### <span data-ttu-id="5b952-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b952-108">-DefaultProfile</span></span>
<span data-ttu-id="5b952-109">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b952-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b952-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b952-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="5b952-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b952-111">-Name</span></span>
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

### <span data-ttu-id="5b952-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b952-112">CommonParameters</span></span>
<span data-ttu-id="5b952-113">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b952-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b952-114">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b952-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b952-115">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b952-115">INPUTS</span></span>

### <span data-ttu-id="5b952-116">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b952-116">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="5b952-117">Paraméterek: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b952-117">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="5b952-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b952-118">OUTPUTS</span></span>

### <span data-ttu-id="5b952-119">Microsoft. Azure. commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="5b952-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="5b952-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b952-120">NOTES</span></span>

## <span data-ttu-id="5b952-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b952-121">RELATED LINKS</span></span>
