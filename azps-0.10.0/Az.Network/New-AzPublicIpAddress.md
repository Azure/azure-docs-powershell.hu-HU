---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 308758942a160b95f1a5bea89a476c15a0dcf003
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841286"
---
# <span data-ttu-id="e7dfe-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e7dfe-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="e7dfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="e7dfe-103">Nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-103">Creates a public IP address.</span></span>

## <span data-ttu-id="e7dfe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7dfe-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7dfe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7dfe-105">DESCRIPTION</span></span>
<span data-ttu-id="e7dfe-106">A **New-AzPublicIpAddress** PARANCSMAG nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="e7dfe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e7dfe-107">EXAMPLES</span></span>

### <span data-ttu-id="e7dfe-108">1: új nyilvános IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7dfe-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="e7dfe-109">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e7dfe-110">A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="e7dfe-111">Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).</span><span class="sxs-lookup"><span data-stu-id="e7dfe-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="e7dfe-112">2: nyilvános IP-cím létrehozása fordított FQDN-vel</span><span class="sxs-lookup"><span data-stu-id="e7dfe-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="e7dfe-113">A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="e7dfe-114">A-ReverseFqdn paraméterrel az Azure létrehoz egy DNS-PTR rekordot (fordított) az erőforráshoz rendelt nyilvános IP-címhez, mutatva a parancsban megadott $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="e7dfe-115">Előfeltételként a $customFqdn (Say webapp.contoso.com) DNS-CNAME rekordot (címkeresési) kell mutatnia a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="e7dfe-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7dfe-116">PARAMETERS</span></span>

### <span data-ttu-id="e7dfe-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="e7dfe-117">-AllocationMethod</span></span>
<span data-ttu-id="e7dfe-118">Azt a módszert adja meg, amellyel a nyilvános IP-címet kioszthatja.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="e7dfe-119">A paraméter elfogadható értékei: static vagy Dynamic.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="e7dfe-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7dfe-120">-AsJob</span></span>
<span data-ttu-id="e7dfe-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e7dfe-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7dfe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7dfe-122">-DefaultProfile</span></span>
<span data-ttu-id="e7dfe-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7dfe-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="e7dfe-124">-DomainNameLabel</span></span>
<span data-ttu-id="e7dfe-125">Egy nyilvános IP-cím relatív DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="e7dfe-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e7dfe-126">-Force</span></span>
<span data-ttu-id="e7dfe-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7dfe-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e7dfe-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e7dfe-129">Az üresjárati időtúllépést adja meg percben kifejezve.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="e7dfe-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e7dfe-130">-IpAddressVersion</span></span>
<span data-ttu-id="e7dfe-131">Az IP-cím verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="e7dfe-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="e7dfe-132">-Location</span></span>
<span data-ttu-id="e7dfe-133">Azt a régiót adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="e7dfe-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7dfe-134">-Name</span></span>
<span data-ttu-id="e7dfe-135">Annak a nyilvános IP-címnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e7dfe-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7dfe-136">-ResourceGroupName</span></span>
<span data-ttu-id="e7dfe-137">Annak az erőforrás-csoportnak a nevét adja meg, amelybe nyilvános IP-címet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="e7dfe-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="e7dfe-138">-ReverseFqdn</span></span>
<span data-ttu-id="e7dfe-139">Egy teljesen minősített tartománynevet ad meg (FQDN).</span><span class="sxs-lookup"><span data-stu-id="e7dfe-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="e7dfe-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="e7dfe-140">-Sku</span></span>
<span data-ttu-id="e7dfe-141">A nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="e7dfe-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="e7dfe-142">-Tag</span></span>
<span data-ttu-id="e7dfe-143">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7dfe-144">Példa:</span><span class="sxs-lookup"><span data-stu-id="e7dfe-144">For example:</span></span>

<span data-ttu-id="e7dfe-145">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e7dfe-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e7dfe-146">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="e7dfe-146">-Zone</span></span>
<span data-ttu-id="e7dfe-147">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="e7dfe-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7dfe-148">-Confirm</span></span>
<span data-ttu-id="e7dfe-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7dfe-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7dfe-150">-WhatIf</span></span>
<span data-ttu-id="e7dfe-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7dfe-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7dfe-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7dfe-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7dfe-153">CommonParameters</span></span>
<span data-ttu-id="e7dfe-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7dfe-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7dfe-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7dfe-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7dfe-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7dfe-156">INPUTS</span></span>

## <span data-ttu-id="e7dfe-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7dfe-157">OUTPUTS</span></span>

### <span data-ttu-id="e7dfe-158">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e7dfe-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e7dfe-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7dfe-159">NOTES</span></span>

## <span data-ttu-id="e7dfe-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7dfe-160">RELATED LINKS</span></span>

[<span data-ttu-id="e7dfe-161">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e7dfe-161">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="e7dfe-162">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e7dfe-162">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="e7dfe-163">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e7dfe-163">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
