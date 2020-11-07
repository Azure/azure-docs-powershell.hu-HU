---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 41b176d5952e9a33d0d0868b97fc71a14d6b43d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844449"
---
# <span data-ttu-id="822c7-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="822c7-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="822c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="822c7-102">SYNOPSIS</span></span>
<span data-ttu-id="822c7-103">IP-konfigurációt hoz létre egy VMSS hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="822c7-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="822c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="822c7-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="822c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="822c7-105">DESCRIPTION</span></span>
<span data-ttu-id="822c7-106">A **New-AzVmssIpConfig** parancsmag létrehoz egy IP-konfigurációs objektumot a virtuálisgép-készlet (VMSS) hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="822c7-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="822c7-107">Adja meg a parancsmag konfigurációját az Add-AzVmssNetworkInterfaceConfiguration parancsmag *IPConfiguration* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="822c7-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="822c7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="822c7-108">EXAMPLES</span></span>

### <span data-ttu-id="822c7-109">Példa 1: IP-konfigurációs objektum létrehozása VMSS-felülethez</span><span class="sxs-lookup"><span data-stu-id="822c7-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="822c7-110">Ez a parancs létrehoz egy ContosoVmssInterface02 nevű IP-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="822c7-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="822c7-111">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="822c7-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="822c7-112">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat az **Add-AzVmssNetworkInterfaceConfiguration** későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="822c7-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="822c7-113">2. példa: IP-konfigurációs objektum létrehozása a NAT-készlet beállításai között</span><span class="sxs-lookup"><span data-stu-id="822c7-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="822c7-114">Ez a parancs létrehoz egy ContosoVmssInterface03 nevű IP-konfigurációs objektumot, majd a $IPConfiguration változóban tárolja későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="822c7-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="822c7-115">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="822c7-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="822c7-116">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="822c7-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="822c7-117">A parancs a *LoadBalancerInboundNatPoolsId* és a *LoadBalancerBackendAddressPoolsId* paraméter értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="822c7-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="822c7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="822c7-118">PARAMETERS</span></span>

### <span data-ttu-id="822c7-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="822c7-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="822c7-120">A backend-címekre mutató hivatkozásokat tartalmazó tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="822c7-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="822c7-121">A méretarány a backend-címkészletet egy nyilvános és egy belső terheléselosztó segítségével is hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="822c7-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="822c7-122">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="822c7-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822c7-123">-DefaultProfile</span></span>
<span data-ttu-id="822c7-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="822c7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="822c7-125">-DnsSetting</span></span>
<span data-ttu-id="822c7-126">A publicIP-címeken alkalmazandó DNS-beállítások.</span><span class="sxs-lookup"><span data-stu-id="822c7-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="822c7-127">A publicIP-címeken alkalmazandó DNS-beállítások tartománynév-címkéje.</span><span class="sxs-lookup"><span data-stu-id="822c7-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="822c7-128">A tartománynév-címke és a VM-index összefűzése a létrehozandó nyilvános IP-cím erőforrásainak tartománynév-címkéjén lesz.</span><span class="sxs-lookup"><span data-stu-id="822c7-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="822c7-129">-Id</span></span>
<span data-ttu-id="822c7-130">AZONOSÍTÓT ad meg.</span><span class="sxs-lookup"><span data-stu-id="822c7-130">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="822c7-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="822c7-132">A betöltők beérkező hálózati címfordítási (NAT) medencéjére mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="822c7-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="822c7-133">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="822c7-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="822c7-134">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="822c7-134">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="822c7-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="822c7-136">A terheléselosztásban beérkező NAT-készletekre mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="822c7-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="822c7-137">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="822c7-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="822c7-138">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="822c7-138">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="822c7-139">-Name</span></span>
<span data-ttu-id="822c7-140">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="822c7-140">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-141">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="822c7-141">-Primary</span></span>
<span data-ttu-id="822c7-142">Az elsődleges IP-konfigurációt adja meg abban az esetben, ha a hálózati felület több IP-konfigurációval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="822c7-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="822c7-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="822c7-144">Adja meg, hogy az IP-konfiguráció IPv4 vagy IPv6 legyen-e.</span><span class="sxs-lookup"><span data-stu-id="822c7-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="822c7-145">Az alapértelmezett érték az IPv4.</span><span class="sxs-lookup"><span data-stu-id="822c7-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="822c7-146">A lehetséges értékek a következők: "IPv4" és "IPv6".</span><span class="sxs-lookup"><span data-stu-id="822c7-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="822c7-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="822c7-148">A nyilvános IP-cím üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="822c7-148">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="822c7-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="822c7-150">Az publicIP név.</span><span class="sxs-lookup"><span data-stu-id="822c7-150">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-151">– NetI</span><span class="sxs-lookup"><span data-stu-id="822c7-151">-SubnetId</span></span>
<span data-ttu-id="822c7-152">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben a konfiguráció létrehozta a VMSS-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="822c7-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="822c7-153">-Confirm</span></span>
<span data-ttu-id="822c7-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="822c7-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822c7-155">-WhatIf</span></span>
<span data-ttu-id="822c7-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="822c7-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="822c7-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="822c7-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822c7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822c7-158">CommonParameters</span></span>
<span data-ttu-id="822c7-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="822c7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822c7-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822c7-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822c7-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="822c7-161">INPUTS</span></span>

### <span data-ttu-id="822c7-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="822c7-162">None</span></span>
<span data-ttu-id="822c7-163">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="822c7-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="822c7-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="822c7-164">OUTPUTS</span></span>

### <span data-ttu-id="822c7-165">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="822c7-165">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="822c7-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="822c7-166">NOTES</span></span>

## <span data-ttu-id="822c7-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="822c7-167">RELATED LINKS</span></span>

[<span data-ttu-id="822c7-168">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="822c7-168">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


