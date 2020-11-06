---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 7ef0d3ce20868c4240abc43278cdc38a33efa5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505316"
---
# <span data-ttu-id="94f7b-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="94f7b-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="94f7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="94f7b-103">Nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="94f7b-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94f7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94f7b-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-PublicIpPrefix <Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix>]
 [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f7b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="94f7b-106">A **New-AzureRmPublicIpAddress** PARANCSMAG nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="94f7b-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="94f7b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="94f7b-108">1: új nyilvános IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="94f7b-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="94f7b-109">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="94f7b-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="94f7b-110">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="94f7b-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="94f7b-111">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="94f7b-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="94f7b-112">2: nyilvános IP-cím létrehozása fordított FQDN-vel</span><span class="sxs-lookup"><span data-stu-id="94f7b-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="94f7b-113">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="94f7b-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="94f7b-114">A-ReverseFqdn paraméterrel az Azure létrehoz egy DNS-PTR rekordot (fordított) az erőforráshoz rendelt nyilvános IP-címhez, mutatva a parancsban megadott $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="94f7b-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="94f7b-115">Előfeltételként a $customFqdn (Say webapp.contoso.com) DNS-CNAME rekordot (címkeresési) kell mutatnia a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="94f7b-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="94f7b-116">3: új nyilvános IP-cím létrehozása a IpTag</span><span class="sxs-lookup"><span data-stu-id="94f7b-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="94f7b-117">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="94f7b-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="94f7b-118">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="94f7b-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="94f7b-119">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="94f7b-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="94f7b-120">A Iptag az erőforráshoz társított címkéket használja.</span><span class="sxs-lookup"><span data-stu-id="94f7b-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="94f7b-121">A Iptag megadható New-AzureRmPublicIpTag és átadva a-IpTags.</span><span class="sxs-lookup"><span data-stu-id="94f7b-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="94f7b-122">4: új nyilvános IP-cím létrehozása előtagból</span><span class="sxs-lookup"><span data-stu-id="94f7b-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="94f7b-123">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="94f7b-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="94f7b-124">Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="94f7b-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="94f7b-125">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz a megadott publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="94f7b-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="94f7b-126">Ezt a lehetőséget csak a "standard" SKU és a "Static" AllocationMethod támogatja.</span><span class="sxs-lookup"><span data-stu-id="94f7b-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="94f7b-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94f7b-127">PARAMETERS</span></span>

### <span data-ttu-id="94f7b-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="94f7b-128">-AllocationMethod</span></span>
<span data-ttu-id="94f7b-129">Azt a módszert adja meg, amellyel a nyilvános IP-címet kioszthatja.</span><span class="sxs-lookup"><span data-stu-id="94f7b-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="94f7b-130">A paraméter elfogadható értékei: static vagy Dynamic.</span><span class="sxs-lookup"><span data-stu-id="94f7b-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94f7b-131">-AsJob</span></span>
<span data-ttu-id="94f7b-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="94f7b-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f7b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f7b-133">-DefaultProfile</span></span>
<span data-ttu-id="94f7b-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94f7b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="94f7b-135">-DomainNameLabel</span></span>
<span data-ttu-id="94f7b-136">Egy nyilvános IP-cím relatív DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94f7b-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="94f7b-137">-Force</span><span class="sxs-lookup"><span data-stu-id="94f7b-137">-Force</span></span>
<span data-ttu-id="94f7b-138">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="94f7b-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94f7b-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="94f7b-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="94f7b-140">Az üresjárati időtúllépést adja meg percben kifejezve.</span><span class="sxs-lookup"><span data-stu-id="94f7b-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="94f7b-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="94f7b-141">-IpAddressVersion</span></span>
<span data-ttu-id="94f7b-142">Az IP-cím verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="94f7b-142">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="94f7b-143">-IpTag</span></span>
<span data-ttu-id="94f7b-144">IpTag lista.</span><span class="sxs-lookup"><span data-stu-id="94f7b-144">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="94f7b-145">-Location</span></span>
<span data-ttu-id="94f7b-146">Azt a régiót adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="94f7b-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="94f7b-147">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="94f7b-147">-PublicIpPrefix</span></span>
<span data-ttu-id="94f7b-148">Azt a PSPublicIpPrefix adja meg, amelyből a nyilvános IP-címet le szeretné foglalni.</span><span class="sxs-lookup"><span data-stu-id="94f7b-148">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94f7b-149">-Name</span></span>
<span data-ttu-id="94f7b-150">Annak a nyilvános IP-címnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="94f7b-150">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f7b-151">-ResourceGroupName</span></span>
<span data-ttu-id="94f7b-152">Annak az erőforrás-csoportnak a nevét adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="94f7b-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="94f7b-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="94f7b-153">-ReverseFqdn</span></span>
<span data-ttu-id="94f7b-154">Egy teljesen minősített tartománynevet ad meg (FQDN).</span><span class="sxs-lookup"><span data-stu-id="94f7b-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="94f7b-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="94f7b-155">-Sku</span></span>
<span data-ttu-id="94f7b-156">A nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="94f7b-156">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-157">-Címke</span><span class="sxs-lookup"><span data-stu-id="94f7b-157">-Tag</span></span>
<span data-ttu-id="94f7b-158">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="94f7b-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="94f7b-159">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="94f7b-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-160">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="94f7b-160">-Zone</span></span>
<span data-ttu-id="94f7b-161">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="94f7b-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94f7b-162">-Confirm</span></span>
<span data-ttu-id="94f7b-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94f7b-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f7b-164">-WhatIf</span></span>
<span data-ttu-id="94f7b-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94f7b-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f7b-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94f7b-166">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f7b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f7b-167">CommonParameters</span></span>
<span data-ttu-id="94f7b-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94f7b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f7b-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f7b-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f7b-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94f7b-170">INPUTS</span></span>

### <span data-ttu-id="94f7b-171">System. String</span><span class="sxs-lookup"><span data-stu-id="94f7b-171">System.String</span></span>

### <span data-ttu-id="94f7b-172">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSPublicIpTag, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="94f7b-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="94f7b-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="94f7b-173">System.Int32</span></span>

### <span data-ttu-id="94f7b-174">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="94f7b-174">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="94f7b-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="94f7b-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94f7b-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94f7b-176">OUTPUTS</span></span>

### <span data-ttu-id="94f7b-177">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="94f7b-177">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="94f7b-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94f7b-178">NOTES</span></span>

## <span data-ttu-id="94f7b-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94f7b-179">RELATED LINKS</span></span>

[<span data-ttu-id="94f7b-180">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="94f7b-180">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="94f7b-181">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="94f7b-181">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="94f7b-182">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="94f7b-182">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
