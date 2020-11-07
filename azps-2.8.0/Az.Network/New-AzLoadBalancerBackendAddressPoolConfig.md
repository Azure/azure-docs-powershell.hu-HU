---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f2ee5f5c740ce8ffb1a791405e3713e269a1a54b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837202"
---
# <span data-ttu-id="7801a-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7801a-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="7801a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7801a-102">SYNOPSIS</span></span>
<span data-ttu-id="7801a-103">Létrehoz egy backend-címkészlet konfigurációját a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="7801a-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="7801a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7801a-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7801a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7801a-105">DESCRIPTION</span></span>
<span data-ttu-id="7801a-106">A **New-AzLoadBalancerBackendAddressPoolConfig** parancsmag a backend-címkészlet konfigurációját hozza létre az Azure terheléselosztásban.</span><span class="sxs-lookup"><span data-stu-id="7801a-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7801a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7801a-107">EXAMPLES</span></span>

### <span data-ttu-id="7801a-108">1. példa: a backend-címkészlet konfigurációjának létrehozása a terheléselosztó számára</span><span class="sxs-lookup"><span data-stu-id="7801a-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="7801a-109">Ez a parancs létrehoz egy BackendAddressPool02 nevű backend-címkészlet-konfigurációt egy terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="7801a-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="7801a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7801a-110">PARAMETERS</span></span>

### <span data-ttu-id="7801a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7801a-111">-DefaultProfile</span></span>
<span data-ttu-id="7801a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7801a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7801a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7801a-113">-Name</span></span>
<span data-ttu-id="7801a-114">A létrehozandó címkészlet-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7801a-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="7801a-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7801a-115">-Confirm</span></span>
<span data-ttu-id="7801a-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7801a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7801a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7801a-117">-WhatIf</span></span>
<span data-ttu-id="7801a-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7801a-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7801a-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7801a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7801a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7801a-120">CommonParameters</span></span>
<span data-ttu-id="7801a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7801a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7801a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7801a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7801a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7801a-123">INPUTS</span></span>

### <span data-ttu-id="7801a-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="7801a-124">None</span></span>

## <span data-ttu-id="7801a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7801a-125">OUTPUTS</span></span>

### <span data-ttu-id="7801a-126">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7801a-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="7801a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7801a-127">NOTES</span></span>

## <span data-ttu-id="7801a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7801a-128">RELATED LINKS</span></span>

[<span data-ttu-id="7801a-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7801a-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7801a-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7801a-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7801a-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7801a-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


