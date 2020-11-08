---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 5c9a70399cc50b773e492410b951b7959e8ade60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011033"
---
# <span data-ttu-id="c2827-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c2827-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c2827-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2827-102">SYNOPSIS</span></span>
<span data-ttu-id="c2827-103">Bejövő NAT-készletet szúr be a terheléselosztó rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="c2827-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="c2827-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2827-104">SYNTAX</span></span>

### <span data-ttu-id="c2827-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2827-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2827-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2827-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2827-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2827-107">DESCRIPTION</span></span>
<span data-ttu-id="c2827-108">Az **Add-AzLoadBalancerInboundNatPoolConfig** parancsmag egy beérkező NAT-készletet szúr be a terheléselosztó bővítménybe.</span><span class="sxs-lookup"><span data-stu-id="c2827-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="c2827-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2827-109">EXAMPLES</span></span>

### <span data-ttu-id="c2827-110">1: Hozzáadás</span><span class="sxs-lookup"><span data-stu-id="c2827-110">1: Add</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="c2827-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2827-111">PARAMETERS</span></span>

### <span data-ttu-id="c2827-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c2827-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2827-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2827-113">-DefaultProfile</span></span>
<span data-ttu-id="c2827-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2827-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2827-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c2827-115">-EnableFloatingIP</span></span>
<span data-ttu-id="c2827-116">Beállítja a virtuális gép végpontját az SQL-AlwaysOn elérhetőségi csoportjának beállításához szükséges lebegő IP-kapacitáshoz.</span><span class="sxs-lookup"><span data-stu-id="c2827-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="c2827-117">Ez a beállítás akkor szükséges, ha az SQL Server-AlwaysOn elérhetőségi csoportjait használja.</span><span class="sxs-lookup"><span data-stu-id="c2827-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="c2827-118">A végpont létrehozása után ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="c2827-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="c2827-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c2827-119">-EnableTcpReset</span></span>
<span data-ttu-id="c2827-120">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="c2827-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c2827-121">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="c2827-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c2827-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2827-122">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2827-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c2827-123">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2827-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c2827-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2827-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="c2827-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2827-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c2827-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c2827-127">A TCP Idle-kapcsolat időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="c2827-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="c2827-128">Az érték 4 és 30 perc között állítható be.</span><span class="sxs-lookup"><span data-stu-id="c2827-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="c2827-129">Az alapértelmezett érték 4 perc.</span><span class="sxs-lookup"><span data-stu-id="c2827-129">The default value is 4 minutes.</span></span> <span data-ttu-id="c2827-130">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="c2827-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c2827-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2827-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="c2827-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2827-132">-Name</span></span>
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

### <span data-ttu-id="c2827-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c2827-133">-Protocol</span></span>
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

### <span data-ttu-id="c2827-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2827-134">-Confirm</span></span>
<span data-ttu-id="c2827-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2827-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2827-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2827-136">-WhatIf</span></span>
<span data-ttu-id="c2827-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c2827-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2827-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2827-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2827-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2827-139">CommonParameters</span></span>
<span data-ttu-id="c2827-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2827-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2827-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2827-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2827-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2827-142">INPUTS</span></span>

### <span data-ttu-id="c2827-143">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2827-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c2827-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c2827-144">System.String</span></span>

### <span data-ttu-id="c2827-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2827-145">System.Int32</span></span>

### <span data-ttu-id="c2827-146">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2827-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="c2827-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2827-147">OUTPUTS</span></span>

### <span data-ttu-id="c2827-148">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2827-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c2827-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2827-149">NOTES</span></span>

## <span data-ttu-id="c2827-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2827-150">RELATED LINKS</span></span>

[<span data-ttu-id="c2827-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c2827-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c2827-152">Új – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c2827-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c2827-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c2827-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c2827-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c2827-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
