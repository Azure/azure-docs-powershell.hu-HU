---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: dd2c0064b92ff96fedd9e06c32b2f2f0f5a2c65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504340"
---
# <span data-ttu-id="29a67-101">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29a67-101">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="29a67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29a67-102">SYNOPSIS</span></span>
<span data-ttu-id="29a67-103">Kimenő szabály konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="29a67-103">Creates an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29a67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29a67-104">SYNTAX</span></span>

### <span data-ttu-id="29a67-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29a67-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29a67-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="29a67-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29a67-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29a67-107">DESCRIPTION</span></span>
<span data-ttu-id="29a67-108">A **New-AzureRmLoadBalancerOutboundRuleConfig** parancsmag létrehoz egy kimenő szabály-konfigurációt az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="29a67-108">The **New-AzureRmLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="29a67-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29a67-109">EXAMPLES</span></span>

### <span data-ttu-id="29a67-110">1. példa: Kimenő szabály konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="29a67-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzureRmLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="29a67-111">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="29a67-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="29a67-112">A második parancs létrehozza a FrontendIpConfig01 nevű előtér-IP-konfigurációt a $publicip nyilvános IP-címével, majd a $frontend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="29a67-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="29a67-113">A harmadik parancs létrehozza a BackendAddressPool01 nevű back-end Address Pool konfigurációt, majd a $backend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="29a67-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="29a67-114">A negyedik parancs létrehozza a MyOutboundRule nevű Kimenő szabály konfigurációját a $frontend és a $backend előtér-és back-end objektumait használva.</span><span class="sxs-lookup"><span data-stu-id="29a67-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="29a67-115">A *protokoll* -, *FrontendIPConfiguration* -és *BackendAddressPool* -paraméterek minden szükségesek a Kimenő szabály konfigurációjának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="29a67-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="29a67-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29a67-116">PARAMETERS</span></span>

### <span data-ttu-id="29a67-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="29a67-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="29a67-118">A NAT-hoz használandó kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="29a67-118">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a67-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="29a67-119">-BackendAddressPool</span></span>
<span data-ttu-id="29a67-120">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="29a67-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="29a67-121">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="29a67-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a67-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="29a67-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="29a67-123">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="29a67-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="29a67-124">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="29a67-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a67-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a67-125">-DefaultProfile</span></span>
<span data-ttu-id="29a67-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29a67-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29a67-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="29a67-127">-EnableTcpReset</span></span>
<span data-ttu-id="29a67-128">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="29a67-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="29a67-129">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="29a67-129">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a67-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a67-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="29a67-131">A terheléselosztó IP-címei.</span><span class="sxs-lookup"><span data-stu-id="29a67-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a67-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="29a67-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="29a67-133">A TCP üresjárati kapcsolat időtúllépése</span><span class="sxs-lookup"><span data-stu-id="29a67-133">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a67-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29a67-134">-Name</span></span>
<span data-ttu-id="29a67-135">A Kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="29a67-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="29a67-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="29a67-136">-Protocol</span></span>
<span data-ttu-id="29a67-137">Protocol – TCP, UDP vagy mind</span><span class="sxs-lookup"><span data-stu-id="29a67-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="29a67-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29a67-138">-Confirm</span></span>
<span data-ttu-id="29a67-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29a67-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29a67-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29a67-140">-WhatIf</span></span>
<span data-ttu-id="29a67-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29a67-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29a67-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29a67-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29a67-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a67-143">CommonParameters</span></span>
<span data-ttu-id="29a67-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29a67-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a67-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a67-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a67-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29a67-146">INPUTS</span></span>

### <span data-ttu-id="29a67-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="29a67-147">System.Int32</span></span>
<span data-ttu-id="29a67-148">System. String System. Collections. Generic. list \` 1 [[Microsoft. Azure. commands. Network. models. PSResourceId, Microsoft. Azure. commands. Network. Version = 6.5.0.0, Culture = semleges, PublicKeyToken = null]] Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="29a67-148">System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="29a67-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29a67-149">OUTPUTS</span></span>

### <span data-ttu-id="29a67-150">Microsoft. Azure. commands. Network. models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="29a67-150">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="29a67-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29a67-151">NOTES</span></span>

## <span data-ttu-id="29a67-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29a67-152">RELATED LINKS</span></span>
