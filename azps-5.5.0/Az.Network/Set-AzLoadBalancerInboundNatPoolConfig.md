---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: ac57c65f670734be6638e71179147490b41085f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160611"
---
# <span data-ttu-id="dcf00-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dcf00-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="dcf00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf00-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf00-103">Bejövő NAT-készlet konfigurációját állítja be egy terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="dcf00-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="dcf00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcf00-104">SYNTAX</span></span>

### <span data-ttu-id="dcf00-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dcf00-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf00-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf00-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf00-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcf00-107">DESCRIPTION</span></span>
<span data-ttu-id="dcf00-108">A **Set-AzLoadBalancerInboundNatPoolConfig** parancsmag bejövő NAT-készlet-konfigurációt állít be a terheléselegyenlők számára.</span><span class="sxs-lookup"><span data-stu-id="dcf00-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="dcf00-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcf00-109">EXAMPLES</span></span>

### <span data-ttu-id="dcf00-110">1. példa: Beállítás</span><span class="sxs-lookup"><span data-stu-id="dcf00-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="dcf00-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcf00-111">PARAMETERS</span></span>

### <span data-ttu-id="dcf00-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="dcf00-112">-BackendPort</span></span>
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

### <span data-ttu-id="dcf00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf00-113">-DefaultProfile</span></span>
<span data-ttu-id="dcf00-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcf00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcf00-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="dcf00-115">-EnableFloatingIP</span></span>
<span data-ttu-id="dcf00-116">Konfigurálja a virtuális gép végpontját az SQL AlwaysOn rendelkezésre állási csoport konfigurálához szükséges lebegő IP-képességhez.</span><span class="sxs-lookup"><span data-stu-id="dcf00-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="dcf00-117">Ez a beállítás az SQL AlwaysOn rendelkezésre állási csoportok SQL Serverben való használata esetén szükséges.</span><span class="sxs-lookup"><span data-stu-id="dcf00-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="dcf00-118">A végpont létrehozása után ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="dcf00-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="dcf00-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="dcf00-119">-EnableTcpReset</span></span>
<span data-ttu-id="dcf00-120">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="dcf00-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="dcf00-121">Ez az elem csak AKKOR használatos, ha a protokoll TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="dcf00-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="dcf00-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcf00-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="dcf00-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dcf00-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="dcf00-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="dcf00-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="dcf00-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="dcf00-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="dcf00-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dcf00-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="dcf00-127">A TCP-inaktív kapcsolat időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="dcf00-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="dcf00-128">Az érték 4 és 30 perc között lehet.</span><span class="sxs-lookup"><span data-stu-id="dcf00-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="dcf00-129">Az alapértelmezett érték 4 perc.</span><span class="sxs-lookup"><span data-stu-id="dcf00-129">The default value is 4 minutes.</span></span> <span data-ttu-id="dcf00-130">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="dcf00-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="dcf00-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcf00-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="dcf00-132">-Name</span><span class="sxs-lookup"><span data-stu-id="dcf00-132">-Name</span></span>
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

### <span data-ttu-id="dcf00-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="dcf00-133">-Protocol</span></span>
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

### <span data-ttu-id="dcf00-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcf00-134">-Confirm</span></span>
<span data-ttu-id="dcf00-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dcf00-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf00-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf00-136">-WhatIf</span></span>
<span data-ttu-id="dcf00-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dcf00-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcf00-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcf00-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf00-139">CommonParameters</span></span>
<span data-ttu-id="dcf00-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf00-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf00-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf00-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcf00-142">INPUTS</span></span>

### <span data-ttu-id="dcf00-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcf00-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="dcf00-144">System.String</span><span class="sxs-lookup"><span data-stu-id="dcf00-144">System.String</span></span>

### <span data-ttu-id="dcf00-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="dcf00-145">System.Int32</span></span>

### <span data-ttu-id="dcf00-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcf00-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="dcf00-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcf00-147">OUTPUTS</span></span>

### <span data-ttu-id="dcf00-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcf00-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dcf00-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcf00-149">NOTES</span></span>

## <span data-ttu-id="dcf00-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcf00-150">RELATED LINKS</span></span>

[<span data-ttu-id="dcf00-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dcf00-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dcf00-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dcf00-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dcf00-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dcf00-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dcf00-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dcf00-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
