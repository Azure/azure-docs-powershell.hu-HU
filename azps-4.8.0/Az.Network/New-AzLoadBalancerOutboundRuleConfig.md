---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025183"
---
# <span data-ttu-id="5dad8-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dad8-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="5dad8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5dad8-102">SYNOPSIS</span></span>
<span data-ttu-id="5dad8-103">Kimenő szabály konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="5dad8-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="5dad8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5dad8-104">SYNTAX</span></span>

### <span data-ttu-id="5dad8-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5dad8-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dad8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5dad8-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dad8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5dad8-107">DESCRIPTION</span></span>
<span data-ttu-id="5dad8-108">A **New-AzLoadBalancerOutboundRuleConfig** parancsmag létrehoz egy kimenő szabály-konfigurációt az Azure terheléselosztó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="5dad8-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5dad8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5dad8-109">EXAMPLES</span></span>

### <span data-ttu-id="5dad8-110">1. példa: Kimenő szabály konfigurációjának létrehozása terheléselosztó esetén</span><span class="sxs-lookup"><span data-stu-id="5dad8-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="5dad8-111">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-címet a MyResourceGroup nevű erőforráscsoport-csoportban, majd a $publicip változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5dad8-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="5dad8-112">A második parancs létrehozza a FrontendIpConfig01 nevű előtér-IP-konfigurációt a $publicip nyilvános IP-címével, majd a $frontend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5dad8-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="5dad8-113">A harmadik parancs létrehozza a BackendAddressPool01 nevű back-end Address Pool konfigurációt, majd a $backend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5dad8-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="5dad8-114">A negyedik parancs létrehozza a MyOutboundRule nevű Kimenő szabály konfigurációját a $frontend és a $backend előtér-és back-end objektumait használva.</span><span class="sxs-lookup"><span data-stu-id="5dad8-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="5dad8-115">A *protokoll* -, *FrontendIPConfiguration* -és *BackendAddressPool* -paraméterek minden szükségesek a Kimenő szabály konfigurációjának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5dad8-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="5dad8-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="5dad8-116">Example 2</span></span>

<span data-ttu-id="5dad8-117">Kimenő szabály konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="5dad8-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="5dad8-118">autogenerated</span><span class="sxs-lookup"><span data-stu-id="5dad8-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="5dad8-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5dad8-119">PARAMETERS</span></span>

### <span data-ttu-id="5dad8-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="5dad8-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="5dad8-121">A NAT-hoz használandó kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="5dad8-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="5dad8-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5dad8-122">-BackendAddressPool</span></span>
<span data-ttu-id="5dad8-123">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="5dad8-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="5dad8-124">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="5dad8-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="5dad8-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5dad8-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="5dad8-126">Egy DIPs-medence hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="5dad8-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="5dad8-127">A kimenő forgalom véletlenszerűen töltődik be az IP-k között a backend-IPs-ben.</span><span class="sxs-lookup"><span data-stu-id="5dad8-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="5dad8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dad8-128">-DefaultProfile</span></span>
<span data-ttu-id="5dad8-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5dad8-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dad8-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="5dad8-130">-EnableTcpReset</span></span>
<span data-ttu-id="5dad8-131">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="5dad8-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="5dad8-132">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="5dad8-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="5dad8-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dad8-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="5dad8-134">A terheléselosztó IP-címei.</span><span class="sxs-lookup"><span data-stu-id="5dad8-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dad8-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5dad8-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5dad8-136">A TCP üresjárati kapcsolat időtúllépése</span><span class="sxs-lookup"><span data-stu-id="5dad8-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="5dad8-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5dad8-137">-Name</span></span>
<span data-ttu-id="5dad8-138">A Kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="5dad8-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="5dad8-139">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5dad8-139">-Protocol</span></span>
<span data-ttu-id="5dad8-140">Protocol – TCP, UDP vagy mind</span><span class="sxs-lookup"><span data-stu-id="5dad8-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="5dad8-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5dad8-141">-Confirm</span></span>
<span data-ttu-id="5dad8-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5dad8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dad8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dad8-143">-WhatIf</span></span>
<span data-ttu-id="5dad8-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5dad8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dad8-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5dad8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dad8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dad8-146">CommonParameters</span></span>
<span data-ttu-id="5dad8-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5dad8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dad8-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dad8-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dad8-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dad8-149">INPUTS</span></span>

### <span data-ttu-id="5dad8-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5dad8-150">System.Int32</span></span>

### <span data-ttu-id="5dad8-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5dad8-151">System.String</span></span>

### <span data-ttu-id="5dad8-152">Microsoft. Azure. commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="5dad8-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="5dad8-153">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5dad8-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="5dad8-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dad8-154">OUTPUTS</span></span>

### <span data-ttu-id="5dad8-155">Microsoft. Azure. commands. Network. models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="5dad8-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="5dad8-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5dad8-156">NOTES</span></span>

## <span data-ttu-id="5dad8-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5dad8-157">RELATED LINKS</span></span>

[<span data-ttu-id="5dad8-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dad8-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="5dad8-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dad8-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="5dad8-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dad8-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="5dad8-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dad8-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
