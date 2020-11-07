---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 3ea89cf0450a5cf24c4299f7eb9c5183195a9663
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837776"
---
# <span data-ttu-id="4d1e6-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d1e6-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="4d1e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1e6-103">Bejövő NAT-készlet konfigurációját állítja be a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="4d1e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d1e6-104">SYNTAX</span></span>

### <span data-ttu-id="4d1e6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d1e6-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d1e6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d1e6-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d1e6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d1e6-107">DESCRIPTION</span></span>
<span data-ttu-id="4d1e6-108">A **set-AzLoadBalancerInboundNatPoolConfig** parancsmag a bejövő NAT-készlet konfigurációját állítja be a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="4d1e6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4d1e6-109">EXAMPLES</span></span>

### <span data-ttu-id="4d1e6-110">1: set</span><span class="sxs-lookup"><span data-stu-id="4d1e6-110">1: Set</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
```

## <span data-ttu-id="4d1e6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d1e6-111">PARAMETERS</span></span>

### <span data-ttu-id="4d1e6-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4d1e6-112">-BackendPort</span></span>
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

### <span data-ttu-id="4d1e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1e6-113">-DefaultProfile</span></span>
<span data-ttu-id="4d1e6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d1e6-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4d1e6-115">-EnableFloatingIP</span></span>
<span data-ttu-id="4d1e6-116">Beállítja a virtuális gép végpontját az SQL-AlwaysOn elérhetőségi csoportjának beállításához szükséges lebegő IP-kapacitáshoz.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="4d1e6-117">Ez a beállítás akkor szükséges, ha az SQL Server-AlwaysOn elérhetőségi csoportjait használja.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="4d1e6-118">A végpont létrehozása után ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="4d1e6-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4d1e6-119">-EnableTcpReset</span></span>
<span data-ttu-id="4d1e6-120">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="4d1e6-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4d1e6-121">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4d1e6-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1e6-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="4d1e6-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4d1e6-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="4d1e6-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="4d1e6-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="4d1e6-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="4d1e6-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="4d1e6-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4d1e6-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4d1e6-127">A TCP Idle-kapcsolat időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="4d1e6-128">Az érték 4 és 30 perc között állítható be.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="4d1e6-129">Az alapértelmezett érték 4 perc.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-129">The default value is 4 minutes.</span></span> <span data-ttu-id="4d1e6-130">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4d1e6-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d1e6-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="4d1e6-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d1e6-132">-Name</span></span>
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

### <span data-ttu-id="4d1e6-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4d1e6-133">-Protocol</span></span>
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

### <span data-ttu-id="4d1e6-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d1e6-134">-Confirm</span></span>
<span data-ttu-id="4d1e6-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1e6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1e6-136">-WhatIf</span></span>
<span data-ttu-id="4d1e6-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d1e6-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1e6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1e6-139">CommonParameters</span></span>
<span data-ttu-id="4d1e6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d1e6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1e6-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1e6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1e6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d1e6-142">INPUTS</span></span>

### <span data-ttu-id="4d1e6-143">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d1e6-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="4d1e6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4d1e6-144">System.String</span></span>

### <span data-ttu-id="4d1e6-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4d1e6-145">System.Int32</span></span>

### <span data-ttu-id="4d1e6-146">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1e6-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="4d1e6-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d1e6-147">OUTPUTS</span></span>

### <span data-ttu-id="4d1e6-148">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d1e6-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4d1e6-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d1e6-149">NOTES</span></span>

## <span data-ttu-id="4d1e6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d1e6-150">RELATED LINKS</span></span>

[<span data-ttu-id="4d1e6-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d1e6-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="4d1e6-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d1e6-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="4d1e6-153">Új – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d1e6-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="4d1e6-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d1e6-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
