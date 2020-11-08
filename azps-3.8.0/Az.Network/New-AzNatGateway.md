---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 49a6a7d817a6b84626b200faada5c36525dc1c91
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013105"
---
# <span data-ttu-id="01057-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="01057-101">New-AzNatGateway</span></span>

## <span data-ttu-id="01057-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01057-102">SYNOPSIS</span></span>
<span data-ttu-id="01057-103">Új NAT-átjáró-erőforrás létrehozása a tulajdonságok nyilvános IP-cím/nyilvános IP-előtag, a IdleTimeoutInMinutes és a SKU beállítással.</span><span class="sxs-lookup"><span data-stu-id="01057-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="01057-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01057-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01057-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01057-105">DESCRIPTION</span></span>
<span data-ttu-id="01057-106">A **New-AzNatGateway** parancsmag hálózati címfordítási átjáró erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="01057-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="01057-107">A natgateway a következőket igényli:</span><span class="sxs-lookup"><span data-stu-id="01057-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="01057-108">Nyilvános IP-cím és/vagy nyilvános IP-előtag</span><span class="sxs-lookup"><span data-stu-id="01057-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="01057-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="01057-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="01057-110">Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="01057-110">Sku</span></span>
- <span data-ttu-id="01057-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01057-111">ResourceGroupName</span></span>
- <span data-ttu-id="01057-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="01057-112">ResourceName</span></span>
- <span data-ttu-id="01057-113">Helyre</span><span class="sxs-lookup"><span data-stu-id="01057-113">Location</span></span>

## <span data-ttu-id="01057-114">Példák</span><span class="sxs-lookup"><span data-stu-id="01057-114">EXAMPLES</span></span>

### <span data-ttu-id="01057-115">1. példa: NAT-átjáró létrehozása nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="01057-115">Example 1 : Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="01057-116">2. példa: NAT-átjáró létrehozása nyilvános IP-előtaggal</span><span class="sxs-lookup"><span data-stu-id="01057-116">Example 2 : Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="01057-117">3. példa: NAT-átjáró létrehozása nyilvános IP-címmel az elérhetőségi zóna 1.</span><span class="sxs-lookup"><span data-stu-id="01057-117">Example 3 : Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="01057-118">Az első parancs általános nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="01057-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="01057-119">A második parancs a NAT-átjárót hozza létre nyilvános IP-címmel az elérhetőségi zóna 1-es verziójában.</span><span class="sxs-lookup"><span data-stu-id="01057-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="01057-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01057-120">PARAMETERS</span></span>

### <span data-ttu-id="01057-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01057-121">-AsJob</span></span>
<span data-ttu-id="01057-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="01057-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01057-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01057-123">-DefaultProfile</span></span>
<span data-ttu-id="01057-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01057-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01057-125">-Force</span><span class="sxs-lookup"><span data-stu-id="01057-125">-Force</span></span>
<span data-ttu-id="01057-126">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01057-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="01057-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="01057-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="01057-128">A NAT-átjáró üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="01057-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="01057-129">-Location</span></span>
<span data-ttu-id="01057-130">A hely.</span><span class="sxs-lookup"><span data-stu-id="01057-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="01057-131">-Name</span></span>
<span data-ttu-id="01057-132">A NAT-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="01057-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="01057-133">-PublicIpAddress</span></span>
<span data-ttu-id="01057-134">A NAT-átjáró erőforráshoz társított nyilvános IP-címek tömbje.</span><span class="sxs-lookup"><span data-stu-id="01057-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="01057-135">-PublicIpPrefix</span></span>
<span data-ttu-id="01057-136">A NAT-átjáró erőforráshoz társított nyilvános IP-előtagok tömbje.</span><span class="sxs-lookup"><span data-stu-id="01057-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01057-137">-ResourceGroupName</span></span>
<span data-ttu-id="01057-138">A NAT-átjáró erőforrás-csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="01057-138">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="01057-139">-Sku</span></span>
<span data-ttu-id="01057-140">A NAT-átjáró SKU-ának neve</span><span class="sxs-lookup"><span data-stu-id="01057-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="01057-141">-Tag</span></span>
<span data-ttu-id="01057-142">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="01057-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-143">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="01057-143">-Zone</span></span>
<span data-ttu-id="01057-144">Az elérhetőségi zónák listája, amely azt a zónát jelöli, amelyen a NAT-átjárót telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="01057-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01057-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="01057-145">-Confirm</span></span>
<span data-ttu-id="01057-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01057-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01057-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01057-147">-WhatIf</span></span>
<span data-ttu-id="01057-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="01057-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01057-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01057-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01057-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01057-150">CommonParameters</span></span>
<span data-ttu-id="01057-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01057-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01057-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01057-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01057-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01057-153">INPUTS</span></span>

### <span data-ttu-id="01057-154">System. String</span><span class="sxs-lookup"><span data-stu-id="01057-154">System.String</span></span>

### <span data-ttu-id="01057-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="01057-155">System.Int32</span></span>

### <span data-ttu-id="01057-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="01057-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="01057-157">Microsoft. Azure. commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="01057-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="01057-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01057-158">OUTPUTS</span></span>

### <span data-ttu-id="01057-159">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="01057-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="01057-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01057-160">NOTES</span></span>

## <span data-ttu-id="01057-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01057-161">RELATED LINKS</span></span>
