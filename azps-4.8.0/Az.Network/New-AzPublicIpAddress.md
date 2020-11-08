---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 3bfed7f4c980ab246f4e38d500860ccd4e2ef09f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024607"
---
# <span data-ttu-id="fe6da-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fe6da-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="fe6da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe6da-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6da-103">Nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fe6da-103">Creates a public IP address.</span></span>

## <span data-ttu-id="fe6da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe6da-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe6da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe6da-105">DESCRIPTION</span></span>
<span data-ttu-id="fe6da-106">A **New-AzPublicIpAddress** PARANCSMAG nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fe6da-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="fe6da-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fe6da-107">EXAMPLES</span></span>

### <span data-ttu-id="fe6da-108">Példa 1: új nyilvános IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe6da-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="fe6da-109">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="fe6da-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="fe6da-110">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="fe6da-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="fe6da-111">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="fe6da-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="fe6da-112">2. példa: nyilvános IP-cím létrehozása fordított FQDN-vel</span><span class="sxs-lookup"><span data-stu-id="fe6da-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="fe6da-113">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="fe6da-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="fe6da-114">A-ReverseFqdn paraméterrel az Azure létrehoz egy DNS-PTR rekordot (fordított) az erőforráshoz rendelt nyilvános IP-címhez, mutatva a parancsban megadott $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="fe6da-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="fe6da-115">Előfeltételként a $customFqdn (Say webapp.contoso.com) DNS-CNAME rekordot (címkeresési) kell mutatnia a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="fe6da-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="fe6da-116">3. példa: új nyilvános IP-cím létrehozása a IpTag</span><span class="sxs-lookup"><span data-stu-id="fe6da-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="fe6da-117">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="fe6da-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="fe6da-118">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="fe6da-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="fe6da-119">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="fe6da-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="fe6da-120">A Iptag az erőforráshoz társított címkéket használja.</span><span class="sxs-lookup"><span data-stu-id="fe6da-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="fe6da-121">A Iptag megadható New-AzPublicIpTag és átadva a-IpTags.</span><span class="sxs-lookup"><span data-stu-id="fe6da-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="fe6da-122">Példa 4: új nyilvános IP-cím létrehozása előtagból</span><span class="sxs-lookup"><span data-stu-id="fe6da-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="fe6da-123">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="fe6da-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="fe6da-124">Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="fe6da-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="fe6da-125">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz a megadott publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="fe6da-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="fe6da-126">Ezt a lehetőséget csak a "standard" SKU és a "Static" AllocationMethod támogatja.</span><span class="sxs-lookup"><span data-stu-id="fe6da-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="fe6da-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe6da-127">PARAMETERS</span></span>

### <span data-ttu-id="fe6da-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="fe6da-128">-AllocationMethod</span></span>
<span data-ttu-id="fe6da-129">Azt a módszert adja meg, amellyel a nyilvános IP-címet kioszthatja.</span><span class="sxs-lookup"><span data-stu-id="fe6da-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="fe6da-130">A paraméter elfogadható értékei: static vagy Dynamic.</span><span class="sxs-lookup"><span data-stu-id="fe6da-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="fe6da-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe6da-131">-AsJob</span></span>
<span data-ttu-id="fe6da-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fe6da-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe6da-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6da-133">-DefaultProfile</span></span>
<span data-ttu-id="fe6da-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe6da-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe6da-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="fe6da-135">-DomainNameLabel</span></span>
<span data-ttu-id="fe6da-136">Egy nyilvános IP-cím relatív DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6da-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="fe6da-137">-Force</span><span class="sxs-lookup"><span data-stu-id="fe6da-137">-Force</span></span>
<span data-ttu-id="fe6da-138">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fe6da-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe6da-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fe6da-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fe6da-140">Az üresjárati időtúllépést adja meg percben kifejezve.</span><span class="sxs-lookup"><span data-stu-id="fe6da-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="fe6da-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="fe6da-141">-IpAddressVersion</span></span>
<span data-ttu-id="fe6da-142">Az IP-cím verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6da-142">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="fe6da-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="fe6da-143">-IpTag</span></span>
<span data-ttu-id="fe6da-144">IpTag lista.</span><span class="sxs-lookup"><span data-stu-id="fe6da-144">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6da-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="fe6da-145">-Location</span></span>
<span data-ttu-id="fe6da-146">Azt a régiót adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="fe6da-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="fe6da-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe6da-147">-Name</span></span>
<span data-ttu-id="fe6da-148">Annak a nyilvános IP-címnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fe6da-148">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe6da-149">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fe6da-149">-PublicIpPrefix</span></span>
<span data-ttu-id="fe6da-150">Azt a PSPublicIpPrefix adja meg, amelyből a nyilvános IP-címet le szeretné foglalni.</span><span class="sxs-lookup"><span data-stu-id="fe6da-150">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="fe6da-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6da-151">-ResourceGroupName</span></span>
<span data-ttu-id="fe6da-152">Annak az erőforrás-csoportnak a nevét adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="fe6da-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="fe6da-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="fe6da-153">-ReverseFqdn</span></span>
<span data-ttu-id="fe6da-154">Egy teljesen minősített tartománynevet ad meg (FQDN).</span><span class="sxs-lookup"><span data-stu-id="fe6da-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="fe6da-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe6da-155">-Sku</span></span>
<span data-ttu-id="fe6da-156">A nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="fe6da-156">The public IP Sku name.</span></span>

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

### <span data-ttu-id="fe6da-157">-Címke</span><span class="sxs-lookup"><span data-stu-id="fe6da-157">-Tag</span></span>
<span data-ttu-id="fe6da-158">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fe6da-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe6da-159">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fe6da-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fe6da-160">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="fe6da-160">-Zone</span></span>
<span data-ttu-id="fe6da-161">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="fe6da-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6da-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe6da-162">-Confirm</span></span>
<span data-ttu-id="fe6da-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe6da-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe6da-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe6da-164">-WhatIf</span></span>
<span data-ttu-id="fe6da-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe6da-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe6da-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe6da-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe6da-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6da-167">CommonParameters</span></span>
<span data-ttu-id="fe6da-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe6da-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6da-169">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6da-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6da-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6da-170">INPUTS</span></span>

### <span data-ttu-id="fe6da-171">System. String</span><span class="sxs-lookup"><span data-stu-id="fe6da-171">System.String</span></span>

### <span data-ttu-id="fe6da-172">Microsoft. Azure. commands. Network. models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="fe6da-172">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="fe6da-173">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fe6da-173">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="fe6da-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fe6da-174">System.Int32</span></span>

### <span data-ttu-id="fe6da-175">System. string []</span><span class="sxs-lookup"><span data-stu-id="fe6da-175">System.String[]</span></span>

### <span data-ttu-id="fe6da-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe6da-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fe6da-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6da-177">OUTPUTS</span></span>

### <span data-ttu-id="fe6da-178">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fe6da-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fe6da-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe6da-179">NOTES</span></span>

## <span data-ttu-id="fe6da-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe6da-180">RELATED LINKS</span></span>

[<span data-ttu-id="fe6da-181">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fe6da-181">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="fe6da-182">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fe6da-182">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="fe6da-183">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fe6da-183">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
