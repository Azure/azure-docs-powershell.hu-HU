---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 08ee19176c05e348f6af5b9c87aeeef8781336a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926514"
---
# <span data-ttu-id="af88c-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af88c-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="af88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af88c-102">SYNOPSIS</span></span>
<span data-ttu-id="af88c-103">Bejövő NAT-készlet-konfigurációt hoz létre a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="af88c-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="af88c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="af88c-104">SYNTAX</span></span>

### <span data-ttu-id="af88c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af88c-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af88c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af88c-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af88c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="af88c-107">DESCRIPTION</span></span>
<span data-ttu-id="af88c-108">A **New-AzLoadBalancerInboundNatPoolConfig** parancsmag létrehoz egy bejövő NAT-készlet-konfigurációt egy terheléselegyenlő számára.</span><span class="sxs-lookup"><span data-stu-id="af88c-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="af88c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="af88c-109">EXAMPLES</span></span>

### <span data-ttu-id="af88c-110">1. példa: Új</span><span class="sxs-lookup"><span data-stu-id="af88c-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="af88c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af88c-111">PARAMETERS</span></span>

### <span data-ttu-id="af88c-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="af88c-112">-BackendPort</span></span>
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

### <span data-ttu-id="af88c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af88c-113">-DefaultProfile</span></span>
<span data-ttu-id="af88c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af88c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af88c-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="af88c-115">-EnableFloatingIP</span></span>
<span data-ttu-id="af88c-116">Konfigurálja a virtuális gép végpontját az SQL AlwaysOn rendelkezésre állási csoport konfigurálához szükséges lebegő IP-képességhez.</span><span class="sxs-lookup"><span data-stu-id="af88c-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="af88c-117">Ez a beállítás az SQL AlwaysOn rendelkezésre állási csoportok SQL Serverben való használata esetén szükséges.</span><span class="sxs-lookup"><span data-stu-id="af88c-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="af88c-118">A végpont létrehozása után ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="af88c-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="af88c-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="af88c-119">-EnableTcpReset</span></span>
<span data-ttu-id="af88c-120">Kétirányú TCP-visszaállítás fogadása a TCP-forgalom üresjárati időkorlátjakor vagy a kapcsolat váratlan megszűnése esetén.</span><span class="sxs-lookup"><span data-stu-id="af88c-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="af88c-121">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="af88c-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="af88c-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="af88c-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="af88c-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="af88c-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="af88c-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="af88c-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="af88c-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="af88c-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="af88c-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="af88c-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="af88c-127">A TCP-inaktív kapcsolat időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="af88c-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="af88c-128">Az érték 4 és 30 perc között lehet.</span><span class="sxs-lookup"><span data-stu-id="af88c-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="af88c-129">Az alapértelmezett érték 4 perc.</span><span class="sxs-lookup"><span data-stu-id="af88c-129">The default value is 4 minutes.</span></span> <span data-ttu-id="af88c-130">Ezt az elemet csak AKKOR használja a protokoll, ha TCP-re van állítva.</span><span class="sxs-lookup"><span data-stu-id="af88c-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="af88c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="af88c-131">-Name</span></span>
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

### <span data-ttu-id="af88c-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="af88c-132">-Protocol</span></span>
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

### <span data-ttu-id="af88c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af88c-133">-Confirm</span></span>
<span data-ttu-id="af88c-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="af88c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af88c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af88c-135">-WhatIf</span></span>
<span data-ttu-id="af88c-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="af88c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af88c-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af88c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af88c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af88c-138">CommonParameters</span></span>
<span data-ttu-id="af88c-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af88c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af88c-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af88c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af88c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af88c-141">INPUTS</span></span>

### <span data-ttu-id="af88c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="af88c-142">System.String</span></span>

### <span data-ttu-id="af88c-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="af88c-143">System.Int32</span></span>

### <span data-ttu-id="af88c-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af88c-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="af88c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af88c-145">OUTPUTS</span></span>

### <span data-ttu-id="af88c-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="af88c-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="af88c-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="af88c-147">NOTES</span></span>

## <span data-ttu-id="af88c-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af88c-148">RELATED LINKS</span></span>

[<span data-ttu-id="af88c-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af88c-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="af88c-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af88c-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="af88c-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af88c-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="af88c-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af88c-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
