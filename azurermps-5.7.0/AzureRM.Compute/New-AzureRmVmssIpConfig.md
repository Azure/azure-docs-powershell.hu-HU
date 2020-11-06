---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495442"
---
# <span data-ttu-id="a85f4-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="a85f4-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="a85f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a85f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a85f4-103">IP-konfigurációt hoz létre egy VMSS hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="a85f4-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a85f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a85f4-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a85f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a85f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a85f4-106">A **New-AzureRmVmssIpConfig** parancsmag létrehoz egy IP-konfigurációs objektumot a virtuálisgép-készlet (VMSS) hálózati felületéhez.</span><span class="sxs-lookup"><span data-stu-id="a85f4-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a85f4-107">Adja meg a parancsmag konfigurációját az Add-AzureRmVmssNetworkInterfaceConfiguration parancsmag *IPConfiguration* paramétereként.</span><span class="sxs-lookup"><span data-stu-id="a85f4-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="a85f4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a85f4-108">EXAMPLES</span></span>

### <span data-ttu-id="a85f4-109">Példa 1: IP-konfigurációs objektum létrehozása VMSS-felülethez</span><span class="sxs-lookup"><span data-stu-id="a85f4-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="a85f4-110">Ez a parancs létrehoz egy ContosoVmssInterface02 nevű IP-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="a85f4-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="a85f4-111">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="a85f4-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="a85f4-112">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat az **Add-AzureRmVmssNetworkInterfaceConfiguration** későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="a85f4-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="a85f4-113">2. példa: IP-konfigurációs objektum létrehozása a NAT-készlet beállításai között</span><span class="sxs-lookup"><span data-stu-id="a85f4-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="a85f4-114">Ez a parancs létrehoz egy ContosoVmssInterface03 nevű IP-konfigurációs objektumot, majd a $IPConfiguration változóban tárolja későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="a85f4-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="a85f4-115">A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="a85f4-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="a85f4-116">A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat későbbi használat céljából menti.</span><span class="sxs-lookup"><span data-stu-id="a85f4-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="a85f4-117">A parancs a *LoadBalancerInboundNatPoolsId* és a *LoadBalancerBackendAddressPoolsId* paraméter értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a85f4-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="a85f4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a85f4-118">PARAMETERS</span></span>

### <span data-ttu-id="a85f4-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="a85f4-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="a85f4-120">A backend-címekre mutató hivatkozásokat tartalmazó tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="a85f4-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="a85f4-121">A méretarány a backend-címkészletet egy nyilvános és egy belső terheléselosztó segítségével is hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="a85f4-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a85f4-122">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="a85f4-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a85f4-123">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="a85f4-123">-DnsSetting</span></span>
<span data-ttu-id="a85f4-124">A publicIP-címeken alkalmazandó DNS-beállítások.</span><span class="sxs-lookup"><span data-stu-id="a85f4-124">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="a85f4-125">A publicIP-címeken alkalmazandó DNS-beállítások tartománynév-címkéje.</span><span class="sxs-lookup"><span data-stu-id="a85f4-125">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="a85f4-126">A tartománynév-címke és a VM-index összefűzése a létrehozandó nyilvános IP-cím erőforrásainak tartománynév-címkéjén lesz.</span><span class="sxs-lookup"><span data-stu-id="a85f4-126">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="a85f4-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a85f4-127">-Id</span></span>
<span data-ttu-id="a85f4-128">AZONOSÍTÓT ad meg.</span><span class="sxs-lookup"><span data-stu-id="a85f4-128">Specifies an ID.</span></span>

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

### <span data-ttu-id="a85f4-129">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="a85f4-129">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="a85f4-130">A betöltők beérkező hálózati címfordítási (NAT) medencéjére mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a85f4-130">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="a85f4-131">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="a85f4-131">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a85f4-132">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="a85f4-132">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a85f4-133">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="a85f4-133">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="a85f4-134">A terheléselosztásban beérkező NAT-készletekre mutató hivatkozások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a85f4-134">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="a85f4-135">A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.</span><span class="sxs-lookup"><span data-stu-id="a85f4-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a85f4-136">Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.</span><span class="sxs-lookup"><span data-stu-id="a85f4-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a85f4-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a85f4-137">-Name</span></span>
<span data-ttu-id="a85f4-138">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a85f4-138">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="a85f4-139">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a85f4-139">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="a85f4-140">Adja meg, hogy az IP-konfiguráció IPv4 vagy IPv6 legyen-e.</span><span class="sxs-lookup"><span data-stu-id="a85f4-140">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="a85f4-141">Az alapértelmezett érték az IPv4.</span><span class="sxs-lookup"><span data-stu-id="a85f4-141">Default is taken as IPv4.</span></span>  <span data-ttu-id="a85f4-142">A lehetséges értékek a következők: "IPv4" és "IPv6".</span><span class="sxs-lookup"><span data-stu-id="a85f4-142">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="a85f4-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a85f4-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="a85f4-144">A nyilvános IP-cím üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="a85f4-144">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a85f4-145">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a85f4-145">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="a85f4-146">Az publicIP név.</span><span class="sxs-lookup"><span data-stu-id="a85f4-146">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="a85f4-147">– NetI</span><span class="sxs-lookup"><span data-stu-id="a85f4-147">-SubnetId</span></span>
<span data-ttu-id="a85f4-148">Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben a konfiguráció létrehozta a VMSS-hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="a85f4-148">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="a85f4-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a85f4-149">-Confirm</span></span>
<span data-ttu-id="a85f4-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a85f4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85f4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85f4-151">-WhatIf</span></span>
<span data-ttu-id="a85f4-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a85f4-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a85f4-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a85f4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85f4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85f4-154">CommonParameters</span></span>
<span data-ttu-id="a85f4-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a85f4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85f4-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a85f4-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85f4-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a85f4-157">INPUTS</span></span>

### <span data-ttu-id="a85f4-158">Nincs</span><span class="sxs-lookup"><span data-stu-id="a85f4-158">None</span></span>
<span data-ttu-id="a85f4-159">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a85f4-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a85f4-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a85f4-160">OUTPUTS</span></span>

## <span data-ttu-id="a85f4-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a85f4-161">NOTES</span></span>

## <span data-ttu-id="a85f4-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a85f4-162">RELATED LINKS</span></span>

[<span data-ttu-id="a85f4-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a85f4-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


