---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466749"
---
# <span data-ttu-id="b7c78-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7c78-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="b7c78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7c78-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c78-103">Nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b7c78-103">Creates a public IP address.</span></span>

## <span data-ttu-id="b7c78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7c78-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c78-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7c78-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c78-106">A **New-AzPublicIpAddress** parancsmag létrehoz egy nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="b7c78-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="b7c78-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7c78-107">EXAMPLES</span></span>

### <span data-ttu-id="b7c78-108">1. példa: Új nyilvános IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7c78-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="b7c78-109">Ez a parancs új nyilvános IP-címforrást hoz létre. Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat.</span><span class="sxs-lookup"><span data-stu-id="b7c78-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="b7c78-110">A rendszer azonnal hozzárendel egy nyilvános IP-címet ehhez az erőforráshoz, mivel a -AllocationMethod "Static" (Statikus) értékként van megadva.</span><span class="sxs-lookup"><span data-stu-id="b7c78-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="b7c78-111">Ha a "Dinamikus" érték van megadva, akkor a nyilvános IP-címeket csak akkor kapja meg a rendszer, amikor elindítja (vagy létrehozza) a társított erőforrást (például vm vagy load balancer).</span><span class="sxs-lookup"><span data-stu-id="b7c78-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="b7c78-112">2. példa: Nyilvános IP-cím létrehozása fordított FQDN-sel</span><span class="sxs-lookup"><span data-stu-id="b7c78-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="b7c78-113">Ez a parancs új nyilvános IP-címforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b7c78-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="b7c78-114">A -ReverseFqdn paraméterrel az Azure létrehoz egy DNS PTR-rekordot (visszakeresés) az erőforráshoz hozzárendelt nyilvános IP-címhez, amely a $customFqdn megadott rekordra mutat.</span><span class="sxs-lookup"><span data-stu-id="b7c78-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="b7c78-115">Előfeltételeként a $customFqdn (például webapp.contoso.com) dns CNAME rekordnak (forward-lookup) kell lennie, amely a $dnsPrefix.$location.cloudapp.azure.com címre mutat.</span><span class="sxs-lookup"><span data-stu-id="b7c78-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="b7c78-116">3. példa: Új nyilvános IP-cím létrehozása iptaggal</span><span class="sxs-lookup"><span data-stu-id="b7c78-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="b7c78-117">Ez a parancs új nyilvános IP-címforrást hoz létre. Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat.</span><span class="sxs-lookup"><span data-stu-id="b7c78-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="b7c78-118">A rendszer azonnal hozzárendel egy nyilvános IP-címet ehhez az erőforráshoz, mivel a -AllocationMethod "Static" (Statikus) értékként van megadva.</span><span class="sxs-lookup"><span data-stu-id="b7c78-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="b7c78-119">Ha a "Dinamikus" érték van megadva, akkor a nyilvános IP-címeket csak akkor kapja meg a rendszer, amikor elindítja (vagy létrehozza) a társított erőforrást (például vm vagy load balancer).</span><span class="sxs-lookup"><span data-stu-id="b7c78-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="b7c78-120">Az Ip-címke az erőforráshoz társított címkékhez használatos.</span><span class="sxs-lookup"><span data-stu-id="b7c78-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="b7c78-121">Az IP-cím megadva a New-AzPublicIpTag és az -IpTags protokollon keresztül bemenetként is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="b7c78-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="b7c78-122">4. példa: Új nyilvános IP-cím létrehozása előtagból</span><span class="sxs-lookup"><span data-stu-id="b7c78-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="b7c78-123">Ez a parancs új nyilvános IP-címforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b7c78-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="b7c78-124">Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat.</span><span class="sxs-lookup"><span data-stu-id="b7c78-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="b7c78-125">A rendszer azonnal hozzárendel egy nyilvános IP-címet ehhez az erőforráshoz a megadott publicIpPrefix értékből.</span><span class="sxs-lookup"><span data-stu-id="b7c78-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="b7c78-126">Ez a lehetőség csak a "Standard" termékváltozat és a "Statikus" AllocationMethod esetén támogatott.</span><span class="sxs-lookup"><span data-stu-id="b7c78-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="b7c78-127">5. példa: Új globális nyilvános IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7c78-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="b7c78-128">Ez a parancs egy új globális nyilvános IP-címforrást hoz létre. Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat.</span><span class="sxs-lookup"><span data-stu-id="b7c78-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="b7c78-129">Az erőforráshoz azonnal hozzárendel egy globális nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="b7c78-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="b7c78-130">Ez a lehetőség csak a "Standard" termékváltozat és a "Statikus" AllocationMethod esetén támogatott.</span><span class="sxs-lookup"><span data-stu-id="b7c78-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="b7c78-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7c78-131">PARAMETERS</span></span>

### <span data-ttu-id="b7c78-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="b7c78-132">-AllocationMethod</span></span>
<span data-ttu-id="b7c78-133">Megadja, hogy milyen módszerrel osztja ki a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="b7c78-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="b7c78-134">A paraméter elfogadható értékei a következőek: Statikus vagy dinamikus.</span><span class="sxs-lookup"><span data-stu-id="b7c78-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="b7c78-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7c78-135">-AsJob</span></span>
<span data-ttu-id="b7c78-136">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b7c78-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7c78-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c78-137">-DefaultProfile</span></span>
<span data-ttu-id="b7c78-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7c78-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7c78-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b7c78-139">-DomainNameLabel</span></span>
<span data-ttu-id="b7c78-140">A nyilvános IP-címek relatív DNS-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7c78-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="b7c78-141">-Force</span><span class="sxs-lookup"><span data-stu-id="b7c78-141">-Force</span></span>
<span data-ttu-id="b7c78-142">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b7c78-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7c78-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b7c78-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b7c78-144">Az üresjárati időkorrekt percben adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7c78-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="b7c78-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b7c78-145">-IpAddressVersion</span></span>
<span data-ttu-id="b7c78-146">Az IP-cím verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7c78-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="b7c78-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="b7c78-147">-IpTag</span></span>
<span data-ttu-id="b7c78-148">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="b7c78-148">IpTag List.</span></span>

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

### <span data-ttu-id="b7c78-149">-Location</span><span class="sxs-lookup"><span data-stu-id="b7c78-149">-Location</span></span>
<span data-ttu-id="b7c78-150">Azt a régiót adja meg, amelyben nyilvános IP-címet kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="b7c78-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="b7c78-151">-Name</span><span class="sxs-lookup"><span data-stu-id="b7c78-151">-Name</span></span>
<span data-ttu-id="b7c78-152">A parancsmag által létrehozott nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="b7c78-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b7c78-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7c78-153">-PublicIpPrefix</span></span>
<span data-ttu-id="b7c78-154">Azt a PSPublicIpPrefixet adja meg, amelyből kiosztja a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="b7c78-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="b7c78-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c78-155">-ResourceGroupName</span></span>
<span data-ttu-id="b7c78-156">Annak az erőforráscsoportnak a nevét adja meg, amelyben nyilvános IP-címet kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="b7c78-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="b7c78-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="b7c78-157">-ReverseFqdn</span></span>
<span data-ttu-id="b7c78-158">Egy fordított, teljesen minősített tartománynevet (FQDN) ad meg.</span><span class="sxs-lookup"><span data-stu-id="b7c78-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="b7c78-159">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="b7c78-159">-Sku</span></span>
<span data-ttu-id="b7c78-160">A nyilvános IP-termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="b7c78-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="b7c78-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7c78-161">-Tag</span></span>
<span data-ttu-id="b7c78-162">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="b7c78-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7c78-163">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="b7c78-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b7c78-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="b7c78-164">-Tier</span></span>
<span data-ttu-id="b7c78-165">A nyilvános IP-termékváltozatréteg.</span><span class="sxs-lookup"><span data-stu-id="b7c78-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c78-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="b7c78-166">-Zone</span></span>
<span data-ttu-id="b7c78-167">A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="b7c78-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b7c78-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7c78-168">-Confirm</span></span>
<span data-ttu-id="b7c78-169">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7c78-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c78-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c78-170">-WhatIf</span></span>
<span data-ttu-id="b7c78-171">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7c78-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c78-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7c78-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c78-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c78-173">CommonParameters</span></span>
<span data-ttu-id="b7c78-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c78-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c78-175">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7c78-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c78-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7c78-176">INPUTS</span></span>

### <span data-ttu-id="b7c78-177">System.String</span><span class="sxs-lookup"><span data-stu-id="b7c78-177">System.String</span></span>

### <span data-ttu-id="b7c78-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="b7c78-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="b7c78-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7c78-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="b7c78-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b7c78-180">System.Int32</span></span>

### <span data-ttu-id="b7c78-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b7c78-181">System.String[]</span></span>

### <span data-ttu-id="b7c78-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7c78-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7c78-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7c78-183">OUTPUTS</span></span>

### <span data-ttu-id="b7c78-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7c78-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b7c78-185">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7c78-185">NOTES</span></span>

## <span data-ttu-id="b7c78-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7c78-186">RELATED LINKS</span></span>

[<span data-ttu-id="b7c78-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7c78-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="b7c78-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7c78-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="b7c78-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7c78-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
