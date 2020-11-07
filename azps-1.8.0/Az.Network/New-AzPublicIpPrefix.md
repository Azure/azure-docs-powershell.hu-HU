---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 6ee4f046281a36f0d0da798f1954a29f8d98d9c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670287"
---
# <span data-ttu-id="c479f-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c479f-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="c479f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c479f-102">SYNOPSIS</span></span>
<span data-ttu-id="c479f-103">Nyilvános IP-előtagot hoz létre</span><span class="sxs-lookup"><span data-stu-id="c479f-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="c479f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c479f-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c479f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c479f-105">DESCRIPTION</span></span>
<span data-ttu-id="c479f-106">A **New-AzPublicIpPrefix** parancsmag létrehoz egy nyilvános IP-előtagot.</span><span class="sxs-lookup"><span data-stu-id="c479f-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="c479f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c479f-107">EXAMPLES</span></span>

### <span data-ttu-id="c479f-108">1: új nyilvános IP-előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="c479f-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="c479f-109">A parancs új nyilvános IP-előtag-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c479f-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="c479f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c479f-110">PARAMETERS</span></span>

### <span data-ttu-id="c479f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c479f-111">-AsJob</span></span>
<span data-ttu-id="c479f-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c479f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c479f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c479f-113">-DefaultProfile</span></span>
<span data-ttu-id="c479f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c479f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c479f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c479f-115">-Force</span></span>
<span data-ttu-id="c479f-116">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="c479f-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c479f-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="c479f-117">-IpAddressVersion</span></span>
<span data-ttu-id="c479f-118">Az IP-cím nyilvános verziója.</span><span class="sxs-lookup"><span data-stu-id="c479f-118">The public IP address version.</span></span>

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

### <span data-ttu-id="c479f-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="c479f-119">-IpTag</span></span>
<span data-ttu-id="c479f-120">IpTag lista.</span><span class="sxs-lookup"><span data-stu-id="c479f-120">IpTag List.</span></span>

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

### <span data-ttu-id="c479f-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="c479f-121">-Location</span></span>
<span data-ttu-id="c479f-122">A nyilvános IP-előtag helye.</span><span class="sxs-lookup"><span data-stu-id="c479f-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="c479f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c479f-123">-Name</span></span>
<span data-ttu-id="c479f-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c479f-124">The resource name.</span></span>

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

### <span data-ttu-id="c479f-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="c479f-125">-PrefixLength</span></span>
<span data-ttu-id="c479f-126">A PublicIPPrefix hossza</span><span class="sxs-lookup"><span data-stu-id="c479f-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="c479f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c479f-127">-ResourceGroupName</span></span>
<span data-ttu-id="c479f-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c479f-128">The resource group name.</span></span>

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

### <span data-ttu-id="c479f-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="c479f-129">-Sku</span></span>
<span data-ttu-id="c479f-130">A nyilvános IP-előtag SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="c479f-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="c479f-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="c479f-131">-Tag</span></span>
<span data-ttu-id="c479f-132">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c479f-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c479f-133">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="c479f-133">-Zone</span></span>
<span data-ttu-id="c479f-134">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="c479f-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="c479f-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c479f-135">-Confirm</span></span>
<span data-ttu-id="c479f-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c479f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c479f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c479f-137">-WhatIf</span></span>
<span data-ttu-id="c479f-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c479f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c479f-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c479f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c479f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c479f-140">CommonParameters</span></span>
<span data-ttu-id="c479f-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c479f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c479f-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c479f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c479f-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c479f-143">INPUTS</span></span>

### <span data-ttu-id="c479f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c479f-144">System.String</span></span>

### <span data-ttu-id="c479f-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="c479f-145">System.UInt16</span></span>

### <span data-ttu-id="c479f-146">Microsoft. Azure. commands. Network. models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="c479f-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="c479f-147">System. string []</span><span class="sxs-lookup"><span data-stu-id="c479f-147">System.String[]</span></span>

### <span data-ttu-id="c479f-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c479f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c479f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c479f-149">OUTPUTS</span></span>

### <span data-ttu-id="c479f-150">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c479f-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="c479f-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c479f-151">NOTES</span></span>

## <span data-ttu-id="c479f-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c479f-152">RELATED LINKS</span></span>

[<span data-ttu-id="c479f-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c479f-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="c479f-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c479f-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="c479f-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c479f-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
