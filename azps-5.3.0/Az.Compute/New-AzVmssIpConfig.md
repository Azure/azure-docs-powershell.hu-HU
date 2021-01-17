---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480809"
---
# <span data-ttu-id="c28eb-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c28eb-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="c28eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c28eb-103">IP-konfigurációt hoz létre a VMSS hálózati felületének.</span><span class="sxs-lookup"><span data-stu-id="c28eb-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="c28eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c28eb-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c28eb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c28eb-105">DESCRIPTION</span></span>
<span data-ttu-id="c28eb-106">A **New-AzVmssIpConfig** parancsmag IP-konfigurációs objektumot hoz létre egy virtuálisgép-mérethalmaz (VMSS) hálózati felületének.</span><span class="sxs-lookup"><span data-stu-id="c28eb-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c28eb-107">Adja meg a parancsmag konfigurációját a Add-AzVmssNetworkInterfaceConfiguration *IPConfiguration* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="c28eb-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="c28eb-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c28eb-108">EXAMPLES</span></span>

### <span data-ttu-id="c28eb-109">1. példa: IP-konfigurációs objektum létrehozása VMSS-felülethez</span><span class="sxs-lookup"><span data-stu-id="c28eb-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="c28eb-110">Ez a parancs létrehoz egy ContosoVmssInterface02 nevű IP-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="c28eb-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="c28eb-111">A parancs egy korábban definiált alhálózati azonosítót használ, amely a $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="c28eb-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="c28eb-112">A parancs a konfigurációs beállításokat a $IPConfiguration változóban tárolja az **Add-AzVmssNetworkInterfaceConfiguration későbbi használatra.**</span><span class="sxs-lookup"><span data-stu-id="c28eb-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="c28eb-113">2. példa: NAT-készletbeállításokat tartalmazó IP-konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="c28eb-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="c28eb-114">Ez a parancs létrehoz egy ContosoVmssInterface03 nevű IP-konfigurációs objektumot, majd azt a $IPConfiguration változóban tárolja későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="c28eb-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="c28eb-115">A parancs egy korábban definiált alhálózati azonosítót használ, amely a $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="c28eb-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="c28eb-116">A parancs a konfigurációs beállításokat a $IPConfiguration későbbi használatra tárolja.</span><span class="sxs-lookup"><span data-stu-id="c28eb-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="c28eb-117">A parancs értékeket ad meg a *LoadBalancerInboundNatPoolsId* és *a LoadBalancerBackendAddressPoolsId paraméterhez.*</span><span class="sxs-lookup"><span data-stu-id="c28eb-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="c28eb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c28eb-118">PARAMETERS</span></span>

### <span data-ttu-id="c28eb-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="c28eb-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="c28eb-120">A terhelésegyenleg-kiegyenlítők háttércímkészletére mutató hivatkozások tömbje.</span><span class="sxs-lookup"><span data-stu-id="c28eb-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="c28eb-121">A méretaránykészletek hivatkozhatnak egy nyilvános és egy belső terheléselosztási készlet háttércímkészletére.</span><span class="sxs-lookup"><span data-stu-id="c28eb-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="c28eb-122">Több méretarány-készlet nem használhatja ugyanazt a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="c28eb-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28eb-123">-DefaultProfile</span></span>
<span data-ttu-id="c28eb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c28eb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c28eb-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="c28eb-125">-DnsSetting</span></span>
<span data-ttu-id="c28eb-126">A publicIP-címekre alkalmazandó DNS-beállítások.</span><span class="sxs-lookup"><span data-stu-id="c28eb-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="c28eb-127">A publicIP-címeken alkalmazandó DNS-beállítások tartománynévfelirata.</span><span class="sxs-lookup"><span data-stu-id="c28eb-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="c28eb-128">A tartománynévfelirat és a vm-index össze concatenatione a létrehoz majd a nyilvános IP-cím típusú erőforrások tartománynevének címkéi lesznek.</span><span class="sxs-lookup"><span data-stu-id="c28eb-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-129">-Id</span><span class="sxs-lookup"><span data-stu-id="c28eb-129">-Id</span></span>
<span data-ttu-id="c28eb-130">Egy azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="c28eb-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="c28eb-131">-IpTag</span></span>
<span data-ttu-id="c28eb-132">Ip Tag-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="c28eb-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="c28eb-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="c28eb-134">A bejövő hálózati címfordítási (NAT) készletekre mutató hivatkozásokat tartalmazó tömböt ad meg a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c28eb-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="c28eb-135">A méretaránykészletek hivatkozhatnak egy nyilvános és egy belső terheléselosztási rendszer bejövő NAT-készletére.</span><span class="sxs-lookup"><span data-stu-id="c28eb-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="c28eb-136">Több méretarány-készlet nem használhatja ugyanazt a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="c28eb-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="c28eb-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="c28eb-138">A terhelésegyenleg-elosztás bejövő NAT-készletére mutató hivatkozások tömbje.</span><span class="sxs-lookup"><span data-stu-id="c28eb-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="c28eb-139">A méretaránykészletek hivatkozhatnak egy nyilvános és egy belső terheléselosztási rendszer bejövő NAT-készletére.</span><span class="sxs-lookup"><span data-stu-id="c28eb-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="c28eb-140">Több méretarány-készlet nem használhatja ugyanazt a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="c28eb-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-141">-Name</span><span class="sxs-lookup"><span data-stu-id="c28eb-141">-Name</span></span>
<span data-ttu-id="c28eb-142">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c28eb-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-143">-Primary</span><span class="sxs-lookup"><span data-stu-id="c28eb-143">-Primary</span></span>
<span data-ttu-id="c28eb-144">Megadja az elsődleges IP-konfigurációt abban az esetben, ha a hálózati felület több IP-konfigurációval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c28eb-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="c28eb-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="c28eb-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="c28eb-146">Adja meg a privát IP-cím IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c28eb-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="c28eb-147">Az alapértelmezett érték IPv4.</span><span class="sxs-lookup"><span data-stu-id="c28eb-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="c28eb-148">Lehetséges értékek: "IPv4" és "IPv6".</span><span class="sxs-lookup"><span data-stu-id="c28eb-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c28eb-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="c28eb-150">A nyilvános IP-cím üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="c28eb-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c28eb-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="c28eb-152">A publicIP-cím konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c28eb-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="c28eb-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="c28eb-154">Adja meg a nyilvános IP-cím IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c28eb-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="c28eb-155">Az alapértelmezett érték IPv4.</span><span class="sxs-lookup"><span data-stu-id="c28eb-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="c28eb-156">Lehetséges értékek: "IPv4" és "IPv6".</span><span class="sxs-lookup"><span data-stu-id="c28eb-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="c28eb-157">-PublicIPPrefix</span></span>
<span data-ttu-id="c28eb-158">A nyilvános IP-előtag azonosítója</span><span class="sxs-lookup"><span data-stu-id="c28eb-158">The ID of Public IP Prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c28eb-159">-SubnetId</span></span>
<span data-ttu-id="c28eb-160">Megadja azt az alhálózati azonosítót, amelyben a konfiguráció létrehozza a VMSS hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="c28eb-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c28eb-161">-Confirm</span></span>
<span data-ttu-id="c28eb-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c28eb-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28eb-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28eb-163">-WhatIf</span></span>
<span data-ttu-id="c28eb-164">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c28eb-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c28eb-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c28eb-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28eb-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28eb-166">CommonParameters</span></span>
<span data-ttu-id="c28eb-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28eb-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28eb-168">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c28eb-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28eb-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c28eb-169">INPUTS</span></span>

### <span data-ttu-id="c28eb-170">System.String</span><span class="sxs-lookup"><span data-stu-id="c28eb-170">System.String</span></span>

### <span data-ttu-id="c28eb-171">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c28eb-171">System.String[]</span></span>

### <span data-ttu-id="c28eb-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c28eb-172">System.Int32</span></span>

### <span data-ttu-id="c28eb-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span><span class="sxs-lookup"><span data-stu-id="c28eb-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="c28eb-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c28eb-174">OUTPUTS</span></span>

### <span data-ttu-id="c28eb-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c28eb-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="c28eb-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c28eb-176">NOTES</span></span>

## <span data-ttu-id="c28eb-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c28eb-177">RELATED LINKS</span></span>

[<span data-ttu-id="c28eb-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c28eb-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


