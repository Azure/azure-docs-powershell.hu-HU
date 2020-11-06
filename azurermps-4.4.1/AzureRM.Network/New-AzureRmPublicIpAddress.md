---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 8437c6037b52fd274415a59bea6ee66a2f9c0588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494839"
---
# <span data-ttu-id="f4437-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4437-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="f4437-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4437-102">SYNOPSIS</span></span>
<span data-ttu-id="f4437-103">Nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4437-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4437-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4437-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4437-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4437-105">DESCRIPTION</span></span>
<span data-ttu-id="f4437-106">A **New-AzureRmPublicIpAddress** PARANCSMAG nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4437-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="f4437-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4437-107">EXAMPLES</span></span>

### <span data-ttu-id="f4437-108">1: új nyilvános IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4437-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="f4437-109">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="f4437-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f4437-110">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="f4437-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="f4437-111">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="f4437-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="f4437-112">2: nyilvános IP-cím létrehozása fordított FQDN-vel</span><span class="sxs-lookup"><span data-stu-id="f4437-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="f4437-113">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f4437-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="f4437-114">A-ReverseFqdn paraméterrel az Azure létrehoz egy DNS-PTR rekordot (fordított) az erőforráshoz rendelt nyilvános IP-címhez, mutatva a parancsban megadott $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="f4437-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="f4437-115">Előfeltételként a $customFqdn (Say webapp.contoso.com) DNS-CNAME rekordot (címkeresési) kell mutatnia a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="f4437-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="f4437-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4437-116">PARAMETERS</span></span>

### <span data-ttu-id="f4437-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="f4437-117">-AllocationMethod</span></span>
<span data-ttu-id="f4437-118">Azt a módszert adja meg, amellyel a nyilvános IP-címet kioszthatja.</span><span class="sxs-lookup"><span data-stu-id="f4437-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="f4437-119">A paraméter elfogadható értékei: static vagy Dynamic.</span><span class="sxs-lookup"><span data-stu-id="f4437-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="f4437-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4437-120">-DefaultProfile</span></span>
<span data-ttu-id="f4437-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4437-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4437-122">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f4437-122">-DomainNameLabel</span></span>
<span data-ttu-id="f4437-123">Egy nyilvános IP-cím relatív DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4437-123">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="f4437-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f4437-124">-Force</span></span>
<span data-ttu-id="f4437-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f4437-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4437-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f4437-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f4437-127">Az üresjárati időtúllépést adja meg percben kifejezve.</span><span class="sxs-lookup"><span data-stu-id="f4437-127">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="f4437-128">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f4437-128">-IpAddressVersion</span></span>
<span data-ttu-id="f4437-129">Az IP-cím verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4437-129">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="f4437-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="f4437-130">-Location</span></span>
<span data-ttu-id="f4437-131">Azt a régiót adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="f4437-131">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="f4437-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4437-132">-Name</span></span>
<span data-ttu-id="f4437-133">Annak a nyilvános IP-címnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4437-133">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f4437-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4437-134">-ResourceGroupName</span></span>
<span data-ttu-id="f4437-135">Annak az erőforrás-csoportnak a nevét adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="f4437-135">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="f4437-136">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="f4437-136">-ReverseFqdn</span></span>
<span data-ttu-id="f4437-137">Egy teljesen minősített tartománynevet ad meg (FQDN).</span><span class="sxs-lookup"><span data-stu-id="f4437-137">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="f4437-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="f4437-138">-Sku</span></span>
<span data-ttu-id="f4437-139">A nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="f4437-139">The public IP Sku name.</span></span>

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

### <span data-ttu-id="f4437-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="f4437-140">-Tag</span></span>
<span data-ttu-id="f4437-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="f4437-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f4437-142">Példa:</span><span class="sxs-lookup"><span data-stu-id="f4437-142">For example:</span></span>

<span data-ttu-id="f4437-143">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="f4437-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f4437-144">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="f4437-144">-Zone</span></span>
<span data-ttu-id="f4437-145">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="f4437-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f4437-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4437-146">-Confirm</span></span>
<span data-ttu-id="f4437-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4437-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4437-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4437-148">-WhatIf</span></span>
<span data-ttu-id="f4437-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4437-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4437-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4437-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4437-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4437-151">CommonParameters</span></span>
<span data-ttu-id="f4437-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4437-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4437-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4437-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4437-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4437-154">INPUTS</span></span>

## <span data-ttu-id="f4437-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4437-155">OUTPUTS</span></span>

### <span data-ttu-id="f4437-156">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4437-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f4437-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4437-157">NOTES</span></span>

## <span data-ttu-id="f4437-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4437-158">RELATED LINKS</span></span>

[<span data-ttu-id="f4437-159">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4437-159">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f4437-160">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4437-160">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f4437-161">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4437-161">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
