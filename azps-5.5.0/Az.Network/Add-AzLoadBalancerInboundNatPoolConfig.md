---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 993b1a3987427f096ecd061199663b35b6577b08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161202"
---
# <span data-ttu-id="18850-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="18850-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="18850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18850-102">SYNOPSIS</span></span>
<span data-ttu-id="18850-103">Bejövő NAT-készlet hozzáadása egy terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="18850-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="18850-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18850-104">SYNTAX</span></span>

### <span data-ttu-id="18850-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18850-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18850-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="18850-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18850-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18850-107">DESCRIPTION</span></span>
<span data-ttu-id="18850-108">Az **Add-AzLoadBalancerInboundNatPoolConfig** parancsmag egy bejövő NAT-készletet ad a terheléselegyenlítóhoz.</span><span class="sxs-lookup"><span data-stu-id="18850-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="18850-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18850-109">EXAMPLES</span></span>

### <span data-ttu-id="18850-110">1. példa: Hozzáadás</span><span class="sxs-lookup"><span data-stu-id="18850-110">Example 1: Add</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="18850-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18850-111">PARAMETERS</span></span>

### <span data-ttu-id="18850-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="18850-112">-BackendPort</span></span>
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

### <span data-ttu-id="18850-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18850-113">-DefaultProfile</span></span>
<span data-ttu-id="18850-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18850-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18850-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="18850-115">-EnableFloatingIP</span></span>
<span data-ttu-id="18850-116">Konfigurálja a virtuális gép végpontját az SQL AlwaysOn rendelkezésre állási csoport konfigurálához szükséges lebegő IP-képességhez.</span><span class="sxs-lookup"><span data-stu-id="18850-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="18850-117">Ez a beállítás az SQL AlwaysOn rendelkezésre állási csoportok SQL Serverben való használata esetén szükséges.</span><span class="sxs-lookup"><span data-stu-id="18850-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="18850-118">A végpont létrehozása után ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="18850-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="18850-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="18850-119">-EnableTcpReset</span></span>
<span data-ttu-id="18850-120">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="18850-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="18850-121">Ez az elem csak AKKOR használatos, ha a protokoll TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="18850-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="18850-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18850-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="18850-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="18850-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="18850-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="18850-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="18850-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="18850-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="18850-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="18850-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="18850-127">A TCP-inaktív kapcsolat időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="18850-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="18850-128">Az érték 4 és 30 perc között lehet.</span><span class="sxs-lookup"><span data-stu-id="18850-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="18850-129">Az alapértelmezett érték 4 perc.</span><span class="sxs-lookup"><span data-stu-id="18850-129">The default value is 4 minutes.</span></span> <span data-ttu-id="18850-130">Ez az elem csak AKKOR használatos, ha a protokoll TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="18850-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="18850-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18850-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="18850-132">-Name</span><span class="sxs-lookup"><span data-stu-id="18850-132">-Name</span></span>
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

### <span data-ttu-id="18850-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="18850-133">-Protocol</span></span>
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

### <span data-ttu-id="18850-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18850-134">-Confirm</span></span>
<span data-ttu-id="18850-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18850-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18850-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18850-136">-WhatIf</span></span>
<span data-ttu-id="18850-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="18850-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18850-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18850-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18850-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18850-139">CommonParameters</span></span>
<span data-ttu-id="18850-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18850-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18850-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18850-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18850-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18850-142">INPUTS</span></span>

### <span data-ttu-id="18850-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18850-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="18850-144">System.String</span><span class="sxs-lookup"><span data-stu-id="18850-144">System.String</span></span>

### <span data-ttu-id="18850-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="18850-145">System.Int32</span></span>

### <span data-ttu-id="18850-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="18850-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="18850-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18850-147">OUTPUTS</span></span>

### <span data-ttu-id="18850-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18850-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="18850-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18850-149">NOTES</span></span>

## <span data-ttu-id="18850-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18850-150">RELATED LINKS</span></span>

[<span data-ttu-id="18850-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="18850-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="18850-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="18850-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="18850-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="18850-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="18850-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="18850-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
