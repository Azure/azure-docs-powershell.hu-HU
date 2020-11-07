---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 28c359c6d9ad9ebfa0d19d7fa4f8d5a72e4884dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837173"
---
# <span data-ttu-id="fd124-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd124-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="fd124-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd124-102">SYNOPSIS</span></span>
<span data-ttu-id="fd124-103">Nyilvános IP-előtagot hoz létre</span><span class="sxs-lookup"><span data-stu-id="fd124-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="fd124-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd124-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd124-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd124-105">DESCRIPTION</span></span>
<span data-ttu-id="fd124-106">A **New-AzPublicIpPrefix** parancsmag létrehoz egy nyilvános IP-előtagot.</span><span class="sxs-lookup"><span data-stu-id="fd124-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="fd124-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd124-107">EXAMPLES</span></span>

### <span data-ttu-id="fd124-108">1: új nyilvános IP-előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd124-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="fd124-109">A parancs új nyilvános IP-előtag-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd124-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="fd124-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd124-110">PARAMETERS</span></span>

### <span data-ttu-id="fd124-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd124-111">-AsJob</span></span>
<span data-ttu-id="fd124-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fd124-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd124-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd124-113">-DefaultProfile</span></span>
<span data-ttu-id="fd124-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd124-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd124-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd124-115">-Force</span></span>
<span data-ttu-id="fd124-116">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd124-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fd124-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="fd124-117">-IpAddressVersion</span></span>
<span data-ttu-id="fd124-118">Az IP-cím nyilvános verziója.</span><span class="sxs-lookup"><span data-stu-id="fd124-118">The public IP address version.</span></span>

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

### <span data-ttu-id="fd124-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="fd124-119">-IpTag</span></span>
<span data-ttu-id="fd124-120">IpTag lista.</span><span class="sxs-lookup"><span data-stu-id="fd124-120">IpTag List.</span></span>

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

### <span data-ttu-id="fd124-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="fd124-121">-Location</span></span>
<span data-ttu-id="fd124-122">A nyilvános IP-előtag helye.</span><span class="sxs-lookup"><span data-stu-id="fd124-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="fd124-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd124-123">-Name</span></span>
<span data-ttu-id="fd124-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fd124-124">The resource name.</span></span>

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

### <span data-ttu-id="fd124-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="fd124-125">-PrefixLength</span></span>
<span data-ttu-id="fd124-126">A PublicIPPrefix hossza</span><span class="sxs-lookup"><span data-stu-id="fd124-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="fd124-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd124-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd124-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd124-128">The resource group name.</span></span>

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

### <span data-ttu-id="fd124-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="fd124-129">-Sku</span></span>
<span data-ttu-id="fd124-130">A nyilvános IP-előtag SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="fd124-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="fd124-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="fd124-131">-Tag</span></span>
<span data-ttu-id="fd124-132">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fd124-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fd124-133">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="fd124-133">-Zone</span></span>
<span data-ttu-id="fd124-134">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="fd124-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="fd124-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd124-135">-Confirm</span></span>
<span data-ttu-id="fd124-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd124-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd124-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd124-137">-WhatIf</span></span>
<span data-ttu-id="fd124-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd124-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd124-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd124-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd124-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd124-140">CommonParameters</span></span>
<span data-ttu-id="fd124-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd124-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd124-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd124-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd124-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd124-143">INPUTS</span></span>

### <span data-ttu-id="fd124-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fd124-144">System.String</span></span>

### <span data-ttu-id="fd124-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="fd124-145">System.UInt16</span></span>

### <span data-ttu-id="fd124-146">Microsoft. Azure. commands. Network. models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="fd124-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="fd124-147">System. string []</span><span class="sxs-lookup"><span data-stu-id="fd124-147">System.String[]</span></span>

### <span data-ttu-id="fd124-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd124-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fd124-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd124-149">OUTPUTS</span></span>

### <span data-ttu-id="fd124-150">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd124-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="fd124-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd124-151">NOTES</span></span>

## <span data-ttu-id="fd124-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd124-152">RELATED LINKS</span></span>

[<span data-ttu-id="fd124-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd124-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="fd124-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd124-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="fd124-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd124-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
