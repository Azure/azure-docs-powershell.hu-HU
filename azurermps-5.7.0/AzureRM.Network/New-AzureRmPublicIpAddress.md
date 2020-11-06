---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503727"
---
# <span data-ttu-id="3bd6f-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3bd6f-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="3bd6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bd6f-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd6f-103">Nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bd6f-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bd6f-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd6f-106">A **New-AzureRmPublicIpAddress** PARANCSMAG nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="3bd6f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3bd6f-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd6f-108">1: új nyilvános IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="3bd6f-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="3bd6f-109">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="3bd6f-110">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="3bd6f-111">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="3bd6f-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="3bd6f-112">2: nyilvános IP-cím létrehozása fordított FQDN-vel</span><span class="sxs-lookup"><span data-stu-id="3bd6f-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="3bd6f-113">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="3bd6f-114">A-ReverseFqdn paraméterrel az Azure létrehoz egy DNS-PTR rekordot (fordított) az erőforráshoz rendelt nyilvános IP-címhez, mutatva a parancsban megadott $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="3bd6f-115">Előfeltételként a $customFqdn (Say webapp.contoso.com) DNS-CNAME rekordot (címkeresési) kell mutatnia a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="3bd6f-116">3: új nyilvános IP-cím létrehozása a IpTag</span><span class="sxs-lookup"><span data-stu-id="3bd6f-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="3bd6f-117">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="3bd6f-118">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="3bd6f-119">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="3bd6f-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="3bd6f-120">A Iptag az erőforráshoz társított címkéket használja.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="3bd6f-121">A Iptag megadható New-AzureRmPublicIpTag és átadva a-IpTags.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="3bd6f-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bd6f-122">PARAMETERS</span></span>

### <span data-ttu-id="3bd6f-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="3bd6f-123">-AllocationMethod</span></span>
<span data-ttu-id="3bd6f-124">Azt a módszert adja meg, amellyel a nyilvános IP-címet kioszthatja.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="3bd6f-125">A paraméter elfogadható értékei: static vagy Dynamic.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bd6f-126">-AsJob</span></span>
<span data-ttu-id="3bd6f-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3bd6f-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3bd6f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd6f-128">-DefaultProfile</span></span>
<span data-ttu-id="3bd6f-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bd6f-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3bd6f-130">-DomainNameLabel</span></span>
<span data-ttu-id="3bd6f-131">Egy nyilvános IP-cím relatív DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-131">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="3bd6f-132">-Force</span><span class="sxs-lookup"><span data-stu-id="3bd6f-132">-Force</span></span>
<span data-ttu-id="3bd6f-133">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3bd6f-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3bd6f-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3bd6f-135">Az üresjárati időtúllépést adja meg percben kifejezve.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-135">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="3bd6f-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3bd6f-136">-IpAddressVersion</span></span>
<span data-ttu-id="3bd6f-137">Az IP-cím verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-138">-IpTag</span><span class="sxs-lookup"><span data-stu-id="3bd6f-138">-IpTag</span></span>
<span data-ttu-id="3bd6f-139">IpTag lista.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-139">IpTag List.</span></span>

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

### <span data-ttu-id="3bd6f-140">-Hely</span><span class="sxs-lookup"><span data-stu-id="3bd6f-140">-Location</span></span>
<span data-ttu-id="3bd6f-141">Azt a régiót adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-141">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="3bd6f-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3bd6f-142">-Name</span></span>
<span data-ttu-id="3bd6f-143">Annak a nyilvános IP-címnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd6f-144">-ResourceGroupName</span></span>
<span data-ttu-id="3bd6f-145">Annak az erőforrás-csoportnak a nevét adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-146">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="3bd6f-146">-ReverseFqdn</span></span>
<span data-ttu-id="3bd6f-147">Egy teljesen minősített tartománynevet ad meg (FQDN).</span><span class="sxs-lookup"><span data-stu-id="3bd6f-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="3bd6f-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="3bd6f-148">-Sku</span></span>
<span data-ttu-id="3bd6f-149">A nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="3bd6f-150">-Tag</span></span>
<span data-ttu-id="3bd6f-151">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3bd6f-152">Példa:</span><span class="sxs-lookup"><span data-stu-id="3bd6f-152">For example:</span></span>

<span data-ttu-id="3bd6f-153">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3bd6f-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-154">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="3bd6f-154">-Zone</span></span>
<span data-ttu-id="3bd6f-155">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="3bd6f-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3bd6f-156">-Confirm</span></span>
<span data-ttu-id="3bd6f-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd6f-158">-WhatIf</span></span>
<span data-ttu-id="3bd6f-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd6f-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd6f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd6f-161">CommonParameters</span></span>
<span data-ttu-id="3bd6f-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bd6f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd6f-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd6f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd6f-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bd6f-164">INPUTS</span></span>

### <span data-ttu-id="3bd6f-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="3bd6f-165">None</span></span>
<span data-ttu-id="3bd6f-166">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3bd6f-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bd6f-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bd6f-167">OUTPUTS</span></span>

### <span data-ttu-id="3bd6f-168">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3bd6f-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="3bd6f-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bd6f-169">NOTES</span></span>

## <span data-ttu-id="3bd6f-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bd6f-170">RELATED LINKS</span></span>

[<span data-ttu-id="3bd6f-171">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3bd6f-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3bd6f-172">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3bd6f-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3bd6f-173">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3bd6f-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
