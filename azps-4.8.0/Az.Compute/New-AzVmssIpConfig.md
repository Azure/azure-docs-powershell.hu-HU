---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183110"
---
# <span data-ttu-id="824c1-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="824c1-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="824c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="824c1-102">SYNOPSIS</span></span>
<span data-ttu-id="824c1-103">IP-konfigurációt hoz létre egy VMSS hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="824c1-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="824c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="824c1-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="824c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="824c1-105">DESCRIPTION</span></span>
<span data-ttu-id="824c1-106">A **New-AzVmssIpConfig** parancsmag létrehoz egy IP-konfigurációs objektumot a virtuálisgép-készlet (VMSS) hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="824c1-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="824c1-107">Adja meg a parancsmag konfigurációját az Add-AzVmssNetworkInterfaceConfiguration parancsmag *IPConfiguration* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="824c1-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="824c1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="824c1-108">EXAMPLES</span></span>

### <span data-ttu-id="824c1-109">Példa 1: IP-konfigurációs objektum létrehozása VMSS-felülethez</span><span class="sxs-lookup"><span data-stu-id="824c1-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="824c1-110">Ez a parancs létrehoz egy ContosoVmssInterface02 nevű IP-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="824c1-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="824c1-111">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="824c1-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="824c1-112">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat az **Add-AzVmssNetworkInterfaceConfiguration** későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="824c1-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="824c1-113">2. példa: IP-konfigurációs objektum létrehozása a NAT-készlet beállításai között</span><span class="sxs-lookup"><span data-stu-id="824c1-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="824c1-114">Ez a parancs létrehoz egy ContosoVmssInterface03 nevű IP-konfigurációs objektumot, majd a $IPConfiguration változóban tárolja későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="824c1-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="824c1-115">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="824c1-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="824c1-116">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="824c1-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="824c1-117">A parancs a *LoadBalancerInboundNatPoolsId* és a *LoadBalancerBackendAddressPoolsId* paraméter értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="824c1-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="824c1-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="824c1-118">PARAMETERS</span></span>

### <span data-ttu-id="824c1-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="824c1-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="824c1-120">A backend-címekre mutató hivatkozásokat tartalmazó tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="824c1-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="824c1-121">A méretarány a backend-címkészletet egy nyilvános és egy belső terheléselosztó segítségével is hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="824c1-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="824c1-122">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="824c1-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="824c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824c1-123">-DefaultProfile</span></span>
<span data-ttu-id="824c1-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="824c1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="824c1-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="824c1-125">-DnsSetting</span></span>
<span data-ttu-id="824c1-126">A publicIP-címeken alkalmazandó DNS-beállítások.</span><span class="sxs-lookup"><span data-stu-id="824c1-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="824c1-127">A publicIP-címeken alkalmazandó DNS-beállítások tartománynév-címkéje.</span><span class="sxs-lookup"><span data-stu-id="824c1-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="824c1-128">A tartománynév-címke és a VM-index összefűzése a létrehozandó nyilvános IP-cím erőforrásainak tartománynév-címkéjén lesz.</span><span class="sxs-lookup"><span data-stu-id="824c1-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="824c1-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="824c1-129">-Id</span></span>
<span data-ttu-id="824c1-130">AZONOSÍTÓT ad meg.</span><span class="sxs-lookup"><span data-stu-id="824c1-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="824c1-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="824c1-131">-IpTag</span></span>
<span data-ttu-id="824c1-132">Az IP-címkézett objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="824c1-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="824c1-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="824c1-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="824c1-134">A betöltők beérkező hálózati címfordítási (NAT) medencéjére mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="824c1-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="824c1-135">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="824c1-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="824c1-136">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="824c1-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="824c1-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="824c1-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="824c1-138">A terheléselosztásban beérkező NAT-készletekre mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="824c1-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="824c1-139">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="824c1-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="824c1-140">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="824c1-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="824c1-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="824c1-141">-Name</span></span>
<span data-ttu-id="824c1-142">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="824c1-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="824c1-143">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="824c1-143">-Primary</span></span>
<span data-ttu-id="824c1-144">Az elsődleges IP-konfigurációt adja meg abban az esetben, ha a hálózati felület több IP-konfigurációval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="824c1-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="824c1-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="824c1-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="824c1-146">Adja meg a magánjellegű IP-cím IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="824c1-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="824c1-147">Az alapértelmezett érték az IPv4.</span><span class="sxs-lookup"><span data-stu-id="824c1-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="824c1-148">A lehetséges értékek a következők: "IPv4" és "IPv6".</span><span class="sxs-lookup"><span data-stu-id="824c1-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="824c1-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="824c1-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="824c1-150">A nyilvános IP-cím üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="824c1-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="824c1-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="824c1-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="824c1-152">Az publicIP név.</span><span class="sxs-lookup"><span data-stu-id="824c1-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="824c1-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="824c1-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="824c1-154">Adja meg a nyilvános IP-cím IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="824c1-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="824c1-155">Az alapértelmezett érték az IPv4.</span><span class="sxs-lookup"><span data-stu-id="824c1-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="824c1-156">A lehetséges értékek a következők: "IPv4" és "IPv6".</span><span class="sxs-lookup"><span data-stu-id="824c1-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="824c1-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="824c1-157">-PublicIPPrefix</span></span>
<span data-ttu-id="824c1-158">A nyilvános IP-előtag azonosítója</span><span class="sxs-lookup"><span data-stu-id="824c1-158">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="824c1-159">– NetI</span><span class="sxs-lookup"><span data-stu-id="824c1-159">-SubnetId</span></span>
<span data-ttu-id="824c1-160">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben a konfiguráció létrehozta a VMSS-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="824c1-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="824c1-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="824c1-161">-Confirm</span></span>
<span data-ttu-id="824c1-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="824c1-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824c1-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824c1-163">-WhatIf</span></span>
<span data-ttu-id="824c1-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="824c1-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="824c1-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="824c1-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824c1-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824c1-166">CommonParameters</span></span>
<span data-ttu-id="824c1-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="824c1-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824c1-168">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="824c1-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824c1-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="824c1-169">INPUTS</span></span>

### <span data-ttu-id="824c1-170">System. String</span><span class="sxs-lookup"><span data-stu-id="824c1-170">System.String</span></span>

### <span data-ttu-id="824c1-171">System. string []</span><span class="sxs-lookup"><span data-stu-id="824c1-171">System.String[]</span></span>

### <span data-ttu-id="824c1-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="824c1-172">System.Int32</span></span>

### <span data-ttu-id="824c1-173">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="824c1-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="824c1-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="824c1-174">OUTPUTS</span></span>

### <span data-ttu-id="824c1-175">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="824c1-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="824c1-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="824c1-176">NOTES</span></span>

## <span data-ttu-id="824c1-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="824c1-177">RELATED LINKS</span></span>

[<span data-ttu-id="824c1-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="824c1-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


