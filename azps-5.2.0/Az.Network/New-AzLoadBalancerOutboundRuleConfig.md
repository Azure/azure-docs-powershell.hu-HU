---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362472"
---
# <span data-ttu-id="9a423-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a423-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="9a423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a423-102">SYNOPSIS</span></span>
<span data-ttu-id="9a423-103">Kimenő szabálykonfigurációt hoz létre a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="9a423-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="9a423-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a423-104">SYNTAX</span></span>

### <span data-ttu-id="9a423-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a423-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a423-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a423-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a423-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a423-107">DESCRIPTION</span></span>
<span data-ttu-id="9a423-108">A **New-AzLoadBalancerOutboundRuleConfig** parancsmag kimenő szabálykonfigurációt hoz létre egy Azure terheléselegyenlő számára.</span><span class="sxs-lookup"><span data-stu-id="9a423-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9a423-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a423-109">EXAMPLES</span></span>

### <span data-ttu-id="9a423-110">1. példa: Kimenő szabálykonfiguráció létrehozása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="9a423-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="9a423-111">Az első parancs létrehoz egy MyPublicIP nevű nyilvános IP-címet a MyResourceGroup nevű erőforráscsoportban, majd tárolja azt a $publicip változóban.</span><span class="sxs-lookup"><span data-stu-id="9a423-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="9a423-112">A második parancs létrehoz egy FrontendIpConfig01 nevű előlapi IP-konfigurációt az $publicip nyilvános IP-címével, majd a $frontend változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9a423-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="9a423-113">A harmadik parancs létrehoz egy BackendAddressPool01 nevű háttércímkészlet-konfigurációt, majd azt a $backend tárolja.</span><span class="sxs-lookup"><span data-stu-id="9a423-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="9a423-114">A negyedik parancs létrehoz egy MyOutboundRule nevű kimenő szabálykonfigurációt a $frontend és a $backend.</span><span class="sxs-lookup"><span data-stu-id="9a423-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="9a423-115">Kimenő szabálykonfiguráció létrehozásához a Protocol, *a FrontendIPConfiguration* és a *BackendAddressPool* paraméterre van szükség.</span><span class="sxs-lookup"><span data-stu-id="9a423-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="9a423-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="9a423-116">Example 2</span></span>

<span data-ttu-id="9a423-117">Kimenő szabálykonfigurációt hoz létre a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="9a423-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="9a423-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="9a423-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="9a423-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a423-119">PARAMETERS</span></span>

### <span data-ttu-id="9a423-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="9a423-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="9a423-121">A NAT-hoz használt kimenő portok száma.</span><span class="sxs-lookup"><span data-stu-id="9a423-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="9a423-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9a423-122">-BackendAddressPool</span></span>
<span data-ttu-id="9a423-123">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="9a423-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="9a423-124">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="9a423-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="9a423-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9a423-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="9a423-126">Hivatkozás dip-eket készletre.</span><span class="sxs-lookup"><span data-stu-id="9a423-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="9a423-127">A kimenő forgalom véletlenszerűen terheléselosztást biztosít a háttér-IP-k IP-i között.</span><span class="sxs-lookup"><span data-stu-id="9a423-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="9a423-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a423-128">-DefaultProfile</span></span>
<span data-ttu-id="9a423-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a423-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a423-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9a423-130">-EnableTcpReset</span></span>
<span data-ttu-id="9a423-131">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="9a423-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="9a423-132">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="9a423-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9a423-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a423-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9a423-134">A terheléselosztás előlapi IP-címei.</span><span class="sxs-lookup"><span data-stu-id="9a423-134">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="9a423-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9a423-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9a423-136">A TCP-inaktív kapcsolat időkorlátja</span><span class="sxs-lookup"><span data-stu-id="9a423-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="9a423-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9a423-137">-Name</span></span>
<span data-ttu-id="9a423-138">A kimenő szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9a423-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="9a423-139">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9a423-139">-Protocol</span></span>
<span data-ttu-id="9a423-140">Protocol - TCP, UDP vagy All</span><span class="sxs-lookup"><span data-stu-id="9a423-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="9a423-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a423-141">-Confirm</span></span>
<span data-ttu-id="9a423-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a423-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a423-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a423-143">-WhatIf</span></span>
<span data-ttu-id="9a423-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a423-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a423-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a423-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a423-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a423-146">CommonParameters</span></span>
<span data-ttu-id="9a423-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a423-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a423-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a423-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a423-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a423-149">INPUTS</span></span>

### <span data-ttu-id="9a423-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9a423-150">System.Int32</span></span>

### <span data-ttu-id="9a423-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9a423-151">System.String</span></span>

### <span data-ttu-id="9a423-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="9a423-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="9a423-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9a423-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9a423-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a423-154">OUTPUTS</span></span>

### <span data-ttu-id="9a423-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="9a423-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="9a423-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a423-156">NOTES</span></span>

## <span data-ttu-id="9a423-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a423-157">RELATED LINKS</span></span>

[<span data-ttu-id="9a423-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a423-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9a423-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a423-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9a423-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a423-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9a423-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a423-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
