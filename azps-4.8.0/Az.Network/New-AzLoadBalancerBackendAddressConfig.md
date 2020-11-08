---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184833"
---
# <span data-ttu-id="83e85-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="83e85-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="83e85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83e85-102">SYNOPSIS</span></span>
<span data-ttu-id="83e85-103">A terheléselosztó backend-cím konfigurációját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="83e85-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="83e85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83e85-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e85-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83e85-105">DESCRIPTION</span></span>
<span data-ttu-id="83e85-106">A terheléselosztó backend-cím konfigurációját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="83e85-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="83e85-107">Példák</span><span class="sxs-lookup"><span data-stu-id="83e85-107">EXAMPLES</span></span>

### <span data-ttu-id="83e85-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83e85-108">Example 1</span></span>
### <span data-ttu-id="83e85-109">2. példa: új loadbalancer-cím, virtuális hálózati hivatkozással</span><span class="sxs-lookup"><span data-stu-id="83e85-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="83e85-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83e85-110">PARAMETERS</span></span>

### <span data-ttu-id="83e85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e85-111">-DefaultProfile</span></span>
<span data-ttu-id="83e85-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83e85-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e85-113">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="83e85-113">-IpAddress</span></span>
<span data-ttu-id="83e85-114">A backend-gyűjtőhöz hozzáadni kívánt Ip_cím</span><span class="sxs-lookup"><span data-stu-id="83e85-114">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e85-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83e85-115">-Name</span></span>
<span data-ttu-id="83e85-116">A backend-cím konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="83e85-116">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e85-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="83e85-117">-VirtualNetworkId</span></span>
<span data-ttu-id="83e85-118">A backend Address config társított virtuális hálózat</span><span class="sxs-lookup"><span data-stu-id="83e85-118">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e85-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83e85-119">-Confirm</span></span>
<span data-ttu-id="83e85-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83e85-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e85-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e85-121">-WhatIf</span></span>
<span data-ttu-id="83e85-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83e85-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83e85-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83e85-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e85-124">CommonParameters</span></span>
<span data-ttu-id="83e85-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83e85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e85-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83e85-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e85-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83e85-127">INPUTS</span></span>

### <span data-ttu-id="83e85-128">System. String</span><span class="sxs-lookup"><span data-stu-id="83e85-128">System.String</span></span>

### <span data-ttu-id="83e85-129">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="83e85-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="83e85-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83e85-130">OUTPUTS</span></span>

### <span data-ttu-id="83e85-131">Microsoft. Azure. commands. Network. models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="83e85-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="83e85-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83e85-132">NOTES</span></span>

## <span data-ttu-id="83e85-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83e85-133">RELATED LINKS</span></span>
