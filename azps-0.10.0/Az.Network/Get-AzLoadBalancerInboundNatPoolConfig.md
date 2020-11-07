---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: d3dcdabc84eca5efa7e52e61f4beafd23eb67b05
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841634"
---
# <span data-ttu-id="d6068-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d6068-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d6068-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6068-102">SYNOPSIS</span></span>

## <span data-ttu-id="d6068-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6068-103">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6068-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6068-104">DESCRIPTION</span></span>

## <span data-ttu-id="d6068-105">Példák</span><span class="sxs-lookup"><span data-stu-id="d6068-105">EXAMPLES</span></span>

### <span data-ttu-id="d6068-106">1:</span><span class="sxs-lookup"><span data-stu-id="d6068-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d6068-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6068-107">PARAMETERS</span></span>

### <span data-ttu-id="d6068-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6068-108">-DefaultProfile</span></span>
<span data-ttu-id="d6068-109">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6068-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6068-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6068-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="d6068-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6068-111">-Name</span></span>
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

### <span data-ttu-id="d6068-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6068-112">CommonParameters</span></span>
<span data-ttu-id="d6068-113">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6068-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6068-114">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6068-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6068-115">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6068-115">INPUTS</span></span>

### <span data-ttu-id="d6068-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6068-116">PSLoadBalancer</span></span>
<span data-ttu-id="d6068-117">A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d6068-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d6068-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6068-118">OUTPUTS</span></span>

### <span data-ttu-id="d6068-119">Microsoft. Azure. commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="d6068-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="d6068-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6068-120">NOTES</span></span>

## <span data-ttu-id="d6068-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6068-121">RELATED LINKS</span></span>

