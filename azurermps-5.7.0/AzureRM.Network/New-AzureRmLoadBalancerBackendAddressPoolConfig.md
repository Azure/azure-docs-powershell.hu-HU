---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: cbac48c8f9f79dc74453222c162fee105cce2fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499744"
---
# <span data-ttu-id="db072-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="db072-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="db072-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db072-102">SYNOPSIS</span></span>
<span data-ttu-id="db072-103">Létrehoz egy backend-címkészlet konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="db072-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db072-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db072-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db072-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db072-105">DESCRIPTION</span></span>
<span data-ttu-id="db072-106">A **New-AzureRmLoadBalancerBackendAddressPoolConfig** parancsmag a backend-címkészlet konfigurációját hozza létre az Azure terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="db072-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="db072-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db072-107">EXAMPLES</span></span>

### <span data-ttu-id="db072-108">1. példa: a backend-címkészlet konfigurációjának létrehozása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="db072-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="db072-109">Ez a parancs létrehoz egy BackendAddressPool02 nevű backend-címkészlet-konfigurációt egy terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="db072-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="db072-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db072-110">PARAMETERS</span></span>

### <span data-ttu-id="db072-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db072-111">-DefaultProfile</span></span>
<span data-ttu-id="db072-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db072-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db072-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db072-113">-Name</span></span>
<span data-ttu-id="db072-114">A létrehozandó címkészlet-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db072-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="db072-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db072-115">CommonParameters</span></span>
<span data-ttu-id="db072-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db072-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db072-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db072-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db072-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db072-118">INPUTS</span></span>

### <span data-ttu-id="db072-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="db072-119">None</span></span>
<span data-ttu-id="db072-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="db072-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db072-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db072-121">OUTPUTS</span></span>

### <span data-ttu-id="db072-122">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="db072-122">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="db072-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db072-123">NOTES</span></span>

## <span data-ttu-id="db072-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db072-124">RELATED LINKS</span></span>

[<span data-ttu-id="db072-125">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="db072-125">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="db072-126">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="db072-126">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="db072-127">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="db072-127">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


