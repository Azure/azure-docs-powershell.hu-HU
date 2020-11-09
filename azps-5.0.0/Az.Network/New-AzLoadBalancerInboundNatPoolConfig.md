---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301967"
---
# <span data-ttu-id="81a18-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="81a18-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="81a18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81a18-102">SYNOPSIS</span></span>
<span data-ttu-id="81a18-103">Bejövő NAT-készlet konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="81a18-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="81a18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81a18-104">SYNTAX</span></span>

### <span data-ttu-id="81a18-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81a18-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81a18-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81a18-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81a18-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81a18-107">DESCRIPTION</span></span>
<span data-ttu-id="81a18-108">A **New-AzLoadBalancerInboundNatPoolConfig** parancsmag egy bejövő NAT-készlet konfigurációját hozza létre a terheléselosztó számára.</span><span class="sxs-lookup"><span data-stu-id="81a18-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="81a18-109">Példák</span><span class="sxs-lookup"><span data-stu-id="81a18-109">EXAMPLES</span></span>

### <span data-ttu-id="81a18-110">1. példa: új</span><span class="sxs-lookup"><span data-stu-id="81a18-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="81a18-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81a18-111">PARAMETERS</span></span>

### <span data-ttu-id="81a18-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="81a18-112">-BackendPort</span></span>
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

### <span data-ttu-id="81a18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a18-113">-DefaultProfile</span></span>
<span data-ttu-id="81a18-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81a18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a18-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="81a18-115">-EnableFloatingIP</span></span>
<span data-ttu-id="81a18-116">Beállítja a virtuális gép végpontját az SQL-AlwaysOn elérhetőségi csoportjának beállításához szükséges lebegő IP-kapacitáshoz.</span><span class="sxs-lookup"><span data-stu-id="81a18-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="81a18-117">Ez a beállítás akkor szükséges, ha az SQL Server-AlwaysOn elérhetőségi csoportjait használja.</span><span class="sxs-lookup"><span data-stu-id="81a18-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="81a18-118">A végpont létrehozása után ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="81a18-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="81a18-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="81a18-119">-EnableTcpReset</span></span>
<span data-ttu-id="81a18-120">A TCP-forgalom üresjárati időkorlátjának vagy a kapcsolati állapotának folyamatos megszüntetése a kétirányú TCP-forgalomban</span><span class="sxs-lookup"><span data-stu-id="81a18-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="81a18-121">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="81a18-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="81a18-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="81a18-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="81a18-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="81a18-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="81a18-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="81a18-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="81a18-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="81a18-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="81a18-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="81a18-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="81a18-127">A TCP Idle-kapcsolat időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="81a18-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="81a18-128">Az érték 4 és 30 perc között állítható be.</span><span class="sxs-lookup"><span data-stu-id="81a18-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="81a18-129">Az alapértelmezett érték 4 perc.</span><span class="sxs-lookup"><span data-stu-id="81a18-129">The default value is 4 minutes.</span></span> <span data-ttu-id="81a18-130">Ez az elem csak akkor használatos, ha a protokoll TCP-értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="81a18-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="81a18-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81a18-131">-Name</span></span>
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

### <span data-ttu-id="81a18-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="81a18-132">-Protocol</span></span>
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

### <span data-ttu-id="81a18-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81a18-133">-Confirm</span></span>
<span data-ttu-id="81a18-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81a18-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a18-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a18-135">-WhatIf</span></span>
<span data-ttu-id="81a18-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81a18-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81a18-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81a18-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a18-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a18-138">CommonParameters</span></span>
<span data-ttu-id="81a18-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81a18-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a18-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a18-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a18-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81a18-141">INPUTS</span></span>

### <span data-ttu-id="81a18-142">System. String</span><span class="sxs-lookup"><span data-stu-id="81a18-142">System.String</span></span>

### <span data-ttu-id="81a18-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="81a18-143">System.Int32</span></span>

### <span data-ttu-id="81a18-144">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81a18-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="81a18-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81a18-145">OUTPUTS</span></span>

### <span data-ttu-id="81a18-146">Microsoft. Azure. commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="81a18-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="81a18-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81a18-147">NOTES</span></span>

## <span data-ttu-id="81a18-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81a18-148">RELATED LINKS</span></span>

[<span data-ttu-id="81a18-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="81a18-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="81a18-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="81a18-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="81a18-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="81a18-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="81a18-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="81a18-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
