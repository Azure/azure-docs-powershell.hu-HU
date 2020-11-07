---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
ms.openlocfilehash: 82c27b6f8f926d273948bdfcb519a10ee1e0a3c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850106"
---
# <span data-ttu-id="e1df6-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1df6-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="e1df6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1df6-102">SYNOPSIS</span></span>
<span data-ttu-id="e1df6-103">IP-konfigurációt hoz létre egy VMSS hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="e1df6-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1df6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1df6-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1df6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1df6-105">DESCRIPTION</span></span>
<span data-ttu-id="e1df6-106">A **New-AzureRmVmssIpConfig** parancsmag létrehoz egy IP-konfigurációs objektumot a virtuálisgép-készlet (VMSS) hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="e1df6-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e1df6-107">Adja meg a parancsmag konfigurációját az Add-AzureRmVmssNetworkInterfaceConfiguration parancsmag *IPConfiguration* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="e1df6-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="e1df6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e1df6-108">EXAMPLES</span></span>

### <span data-ttu-id="e1df6-109">Példa 1: IP-konfigurációs objektum létrehozása VMSS-felülethez</span><span class="sxs-lookup"><span data-stu-id="e1df6-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="e1df6-110">Ez a parancs létrehoz egy ContosoVmssInterface02 nevű IP-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="e1df6-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="e1df6-111">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="e1df6-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="e1df6-112">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat az **Add-AzureRmVmssNetworkInterfaceConfiguration** későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="e1df6-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="e1df6-113">2. példa: IP-konfigurációs objektum létrehozása a NAT-készlet beállításai között</span><span class="sxs-lookup"><span data-stu-id="e1df6-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="e1df6-114">Ez a parancs létrehoz egy ContosoVmssInterface03 nevű IP-konfigurációs objektumot, majd a $IPConfiguration változóban tárolja későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="e1df6-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="e1df6-115">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="e1df6-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="e1df6-116">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="e1df6-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="e1df6-117">A parancs a *LoadBalancerInboundNatPoolsId* és a *LoadBalancerBackendAddressPoolsId* paraméter értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1df6-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="e1df6-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1df6-118">PARAMETERS</span></span>

### <span data-ttu-id="e1df6-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="e1df6-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="e1df6-120">A backend-címekre mutató hivatkozásokat tartalmazó tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e1df6-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="e1df6-121">A méretarány a backend-címkészletet egy nyilvános és egy belső terheléselosztó segítségével is hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="e1df6-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e1df6-122">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="e1df6-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="e1df6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1df6-123">-DefaultProfile</span></span>
<span data-ttu-id="e1df6-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1df6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1df6-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e1df6-125">-DnsSetting</span></span>
<span data-ttu-id="e1df6-126">A publicIP-címeken alkalmazandó DNS-beállítások.</span><span class="sxs-lookup"><span data-stu-id="e1df6-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="e1df6-127">A publicIP-címeken alkalmazandó DNS-beállítások tartománynév-címkéje.</span><span class="sxs-lookup"><span data-stu-id="e1df6-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="e1df6-128">A tartománynév-címke és a VM-index összefűzése a létrehozandó nyilvános IP-cím erőforrásainak tartománynév-címkéjén lesz.</span><span class="sxs-lookup"><span data-stu-id="e1df6-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="e1df6-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e1df6-129">-Id</span></span>
<span data-ttu-id="e1df6-130">AZONOSÍTÓT ad meg.</span><span class="sxs-lookup"><span data-stu-id="e1df6-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="e1df6-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="e1df6-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="e1df6-132">A betöltők beérkező hálózati címfordítási (NAT) medencéjére mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1df6-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="e1df6-133">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="e1df6-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e1df6-134">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="e1df6-134">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="e1df6-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="e1df6-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="e1df6-136">A terheléselosztásban beérkező NAT-készletekre mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1df6-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="e1df6-137">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="e1df6-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e1df6-138">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="e1df6-138">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="e1df6-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1df6-139">-Name</span></span>
<span data-ttu-id="e1df6-140">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1df6-140">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="e1df6-141">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="e1df6-141">-Primary</span></span>
<span data-ttu-id="e1df6-142">Az elsődleges IP-konfigurációt adja meg abban az esetben, ha a hálózati felület több IP-konfigurációval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e1df6-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="e1df6-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e1df6-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="e1df6-144">Adja meg, hogy az IP-konfiguráció IPv4 vagy IPv6 legyen-e.</span><span class="sxs-lookup"><span data-stu-id="e1df6-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="e1df6-145">Az alapértelmezett érték az IPv4.</span><span class="sxs-lookup"><span data-stu-id="e1df6-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="e1df6-146">A lehetséges értékek a következők: "IPv4" és "IPv6".</span><span class="sxs-lookup"><span data-stu-id="e1df6-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="e1df6-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e1df6-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="e1df6-148">A nyilvános IP-cím üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="e1df6-148">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="e1df6-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e1df6-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="e1df6-150">Az publicIP név.</span><span class="sxs-lookup"><span data-stu-id="e1df6-150">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="e1df6-151">– NetI</span><span class="sxs-lookup"><span data-stu-id="e1df6-151">-SubnetId</span></span>
<span data-ttu-id="e1df6-152">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben a konfiguráció létrehozta a VMSS-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="e1df6-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="e1df6-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1df6-153">-Confirm</span></span>
<span data-ttu-id="e1df6-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1df6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1df6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1df6-155">-WhatIf</span></span>
<span data-ttu-id="e1df6-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1df6-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1df6-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1df6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1df6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1df6-158">CommonParameters</span></span>
<span data-ttu-id="e1df6-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1df6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1df6-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1df6-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1df6-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1df6-161">INPUTS</span></span>

### <span data-ttu-id="e1df6-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1df6-162">None</span></span>
<span data-ttu-id="e1df6-163">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e1df6-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1df6-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1df6-164">OUTPUTS</span></span>

### <span data-ttu-id="e1df6-165">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1df6-165">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="e1df6-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1df6-166">NOTES</span></span>

## <span data-ttu-id="e1df6-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1df6-167">RELATED LINKS</span></span>

[<span data-ttu-id="e1df6-168">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1df6-168">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


