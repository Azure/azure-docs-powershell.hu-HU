---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680323"
---
# <span data-ttu-id="37a68-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37a68-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="37a68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37a68-102">SYNOPSIS</span></span>
<span data-ttu-id="37a68-103">Nyilvános IP-előtagot hoz létre</span><span class="sxs-lookup"><span data-stu-id="37a68-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37a68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37a68-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37a68-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37a68-105">DESCRIPTION</span></span>
<span data-ttu-id="37a68-106">A **New-AzureRmPublicIpPrefix** parancsmag létrehoz egy nyilvános IP-előtagot.</span><span class="sxs-lookup"><span data-stu-id="37a68-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="37a68-107">Példák</span><span class="sxs-lookup"><span data-stu-id="37a68-107">EXAMPLES</span></span>

### <span data-ttu-id="37a68-108">1: új nyilvános IP-előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="37a68-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="37a68-109">A parancs új nyilvános IP-előtag-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="37a68-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="37a68-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37a68-110">PARAMETERS</span></span>

### <span data-ttu-id="37a68-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37a68-111">-AsJob</span></span>
<span data-ttu-id="37a68-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="37a68-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37a68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a68-113">-DefaultProfile</span></span>
<span data-ttu-id="37a68-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37a68-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37a68-115">-Force</span><span class="sxs-lookup"><span data-stu-id="37a68-115">-Force</span></span>
<span data-ttu-id="37a68-116">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="37a68-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="37a68-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="37a68-117">-IpAddressVersion</span></span>
<span data-ttu-id="37a68-118">Az IP-cím nyilvános verziója.</span><span class="sxs-lookup"><span data-stu-id="37a68-118">The public IP address version.</span></span>

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

### <span data-ttu-id="37a68-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="37a68-119">-IpTag</span></span>
<span data-ttu-id="37a68-120">IpTag lista.</span><span class="sxs-lookup"><span data-stu-id="37a68-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a68-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="37a68-121">-Location</span></span>
<span data-ttu-id="37a68-122">A nyilvános IP-előtag helye.</span><span class="sxs-lookup"><span data-stu-id="37a68-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="37a68-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37a68-123">-Name</span></span>
<span data-ttu-id="37a68-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="37a68-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a68-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="37a68-125">-PrefixLength</span></span>
<span data-ttu-id="37a68-126">A PublicIPPrefix hossza</span><span class="sxs-lookup"><span data-stu-id="37a68-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a68-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a68-127">-ResourceGroupName</span></span>
<span data-ttu-id="37a68-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="37a68-128">The resource group name.</span></span>

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

### <span data-ttu-id="37a68-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="37a68-129">-Sku</span></span>
<span data-ttu-id="37a68-130">A nyilvános IP-előtag SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="37a68-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a68-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="37a68-131">-Tag</span></span>
<span data-ttu-id="37a68-132">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="37a68-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="37a68-133">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="37a68-133">-Zone</span></span>
<span data-ttu-id="37a68-134">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="37a68-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="37a68-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="37a68-135">-Confirm</span></span>
<span data-ttu-id="37a68-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="37a68-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37a68-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37a68-137">-WhatIf</span></span>
<span data-ttu-id="37a68-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="37a68-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37a68-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37a68-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37a68-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a68-140">CommonParameters</span></span>
<span data-ttu-id="37a68-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37a68-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="37a68-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a68-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a68-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37a68-143">INPUTS</span></span>

### <span data-ttu-id="37a68-144">System. String</span><span class="sxs-lookup"><span data-stu-id="37a68-144">System.String</span></span>
<span data-ttu-id="37a68-145">System. UInt16 System. Collections. Generic. list `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="37a68-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="37a68-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37a68-146">OUTPUTS</span></span>

### <span data-ttu-id="37a68-147">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37a68-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="37a68-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37a68-148">NOTES</span></span>

## <span data-ttu-id="37a68-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37a68-149">RELATED LINKS</span></span>
