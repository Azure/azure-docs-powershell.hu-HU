---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466748"
---
# <span data-ttu-id="8ec05-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec05-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="8ec05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec05-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec05-103">Nyilvános IP-előtagot hoz létre</span><span class="sxs-lookup"><span data-stu-id="8ec05-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="8ec05-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ec05-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec05-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ec05-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec05-106">A **New-AzPublicIpPrefix** parancsmag létrehoz egy nyilvános IP-előtagot.</span><span class="sxs-lookup"><span data-stu-id="8ec05-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="8ec05-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ec05-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec05-108">1. példa: Új nyilvános IP-előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="8ec05-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="8ec05-109">Ez a parancs új nyilvános IP-előtagforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8ec05-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="8ec05-110">2. példa: Új globális nyilvános IP-előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="8ec05-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="8ec05-111">Ez a parancs egy új globális nyilvános IP-előtagforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8ec05-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="8ec05-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ec05-112">PARAMETERS</span></span>

### <span data-ttu-id="8ec05-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ec05-113">-AsJob</span></span>
<span data-ttu-id="8ec05-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8ec05-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ec05-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec05-115">-CustomIpPrefix</span></span>
<span data-ttu-id="8ec05-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span><span class="sxs-lookup"><span data-stu-id="8ec05-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec05-117">-DefaultProfile</span></span>
<span data-ttu-id="8ec05-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ec05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ec05-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8ec05-119">-Force</span></span>
<span data-ttu-id="8ec05-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="8ec05-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8ec05-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8ec05-121">-IpAddressVersion</span></span>
<span data-ttu-id="8ec05-122">A nyilvános IP-cím verziója.</span><span class="sxs-lookup"><span data-stu-id="8ec05-122">The public IP address version.</span></span>

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

### <span data-ttu-id="8ec05-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="8ec05-123">-IpTag</span></span>
<span data-ttu-id="8ec05-124">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="8ec05-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec05-125">-Location</span><span class="sxs-lookup"><span data-stu-id="8ec05-125">-Location</span></span>
<span data-ttu-id="8ec05-126">A nyilvános IP-előtag helye.</span><span class="sxs-lookup"><span data-stu-id="8ec05-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="8ec05-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8ec05-127">-Name</span></span>
<span data-ttu-id="8ec05-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8ec05-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec05-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="8ec05-129">-PrefixLength</span></span>
<span data-ttu-id="8ec05-130">A PublicIPPrefix hossza</span><span class="sxs-lookup"><span data-stu-id="8ec05-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec05-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec05-131">-ResourceGroupName</span></span>
<span data-ttu-id="8ec05-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ec05-132">The resource group name.</span></span>

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

### <span data-ttu-id="8ec05-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="8ec05-133">-Sku</span></span>
<span data-ttu-id="8ec05-134">A nyilvános IP-előtag termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="8ec05-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec05-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ec05-135">-Tag</span></span>
<span data-ttu-id="8ec05-136">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="8ec05-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8ec05-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="8ec05-137">-Tier</span></span>
<span data-ttu-id="8ec05-138">A nyilvános IP-előtag termékváltozatrétege.</span><span class="sxs-lookup"><span data-stu-id="8ec05-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="8ec05-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="8ec05-139">-Zone</span></span>
<span data-ttu-id="8ec05-140">A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8ec05-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8ec05-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ec05-141">-Confirm</span></span>
<span data-ttu-id="8ec05-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8ec05-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec05-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec05-143">-WhatIf</span></span>
<span data-ttu-id="8ec05-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8ec05-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec05-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ec05-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec05-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec05-146">CommonParameters</span></span>
<span data-ttu-id="8ec05-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec05-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec05-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ec05-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec05-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ec05-149">INPUTS</span></span>

### <span data-ttu-id="8ec05-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8ec05-150">System.String</span></span>

### <span data-ttu-id="8ec05-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="8ec05-151">System.UInt16</span></span>

### <span data-ttu-id="8ec05-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="8ec05-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="8ec05-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8ec05-153">System.String[]</span></span>

### <span data-ttu-id="8ec05-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ec05-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8ec05-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ec05-155">OUTPUTS</span></span>

### <span data-ttu-id="8ec05-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec05-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="8ec05-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ec05-157">NOTES</span></span>

## <span data-ttu-id="8ec05-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ec05-158">RELATED LINKS</span></span>

[<span data-ttu-id="8ec05-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec05-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="8ec05-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec05-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="8ec05-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec05-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
