---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344814"
---
# <span data-ttu-id="36431-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36431-101">New-AzNatGateway</span></span>

## <span data-ttu-id="36431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36431-102">SYNOPSIS</span></span>
<span data-ttu-id="36431-103">Hozzon létre új Nat Gateway-erőforrást nyilvános IP-cím/nyilvános IP-előtag, IdleTimeoutInMinutes és Sku tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="36431-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="36431-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36431-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36431-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36431-105">DESCRIPTION</span></span>
<span data-ttu-id="36431-106">A **New-AzNatGateway** parancsmag létrehoz egy Nat Átjáró típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="36431-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="36431-107">A natgateway használatához az alábbiakra van szükség:</span><span class="sxs-lookup"><span data-stu-id="36431-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="36431-108">Nyilvános IP-cím és/vagy nyilvános IP-előtag</span><span class="sxs-lookup"><span data-stu-id="36431-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="36431-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="36431-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="36431-110">Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="36431-110">Sku</span></span>
- <span data-ttu-id="36431-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36431-111">ResourceGroupName</span></span>
- <span data-ttu-id="36431-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="36431-112">ResourceName</span></span>
- <span data-ttu-id="36431-113">Hely</span><span class="sxs-lookup"><span data-stu-id="36431-113">Location</span></span>

## <span data-ttu-id="36431-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36431-114">EXAMPLES</span></span>

### <span data-ttu-id="36431-115">1. példa: Nat-átjáró létrehozása nyilvános IP-címmel</span><span class="sxs-lookup"><span data-stu-id="36431-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="36431-116">2. példa: Nat-átjáró létrehozása nyilvános IP-előtaggal</span><span class="sxs-lookup"><span data-stu-id="36431-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="36431-117">3. példa: Nat-átjáró létrehozása nyilvános IP-címmel az 1. elérhetőségi zónában</span><span class="sxs-lookup"><span data-stu-id="36431-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="36431-118">Az első parancs szabványos nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36431-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="36431-119">A második parancs létrehozza a NAT-átjárót nyilvános IP-címmel az 1. elérhetőségi zónában.</span><span class="sxs-lookup"><span data-stu-id="36431-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="36431-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36431-120">PARAMETERS</span></span>

### <span data-ttu-id="36431-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36431-121">-AsJob</span></span>
<span data-ttu-id="36431-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="36431-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36431-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36431-123">-DefaultProfile</span></span>
<span data-ttu-id="36431-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36431-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36431-125">-Force</span><span class="sxs-lookup"><span data-stu-id="36431-125">-Force</span></span>
<span data-ttu-id="36431-126">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="36431-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="36431-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="36431-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="36431-128">A nat átjáró üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="36431-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="36431-129">-Location</span><span class="sxs-lookup"><span data-stu-id="36431-129">-Location</span></span>
<span data-ttu-id="36431-130">A hely.</span><span class="sxs-lookup"><span data-stu-id="36431-130">The location.</span></span>

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

### <span data-ttu-id="36431-131">-Name</span><span class="sxs-lookup"><span data-stu-id="36431-131">-Name</span></span>
<span data-ttu-id="36431-132">A nat átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="36431-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="36431-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36431-133">-PublicIpAddress</span></span>
<span data-ttu-id="36431-134">A nat-átjáró erőforrásával társított nyilvános IP-címek tömbje.</span><span class="sxs-lookup"><span data-stu-id="36431-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="36431-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="36431-135">-PublicIpPrefix</span></span>
<span data-ttu-id="36431-136">A nat átjáró erőforráshoz társított nyilvános IP-előtagok tömbje.</span><span class="sxs-lookup"><span data-stu-id="36431-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="36431-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36431-137">-ResourceGroupName</span></span>
<span data-ttu-id="36431-138">A nat átjáró erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="36431-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="36431-139">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="36431-139">-Sku</span></span>
<span data-ttu-id="36431-140">A NAT-átjáró termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="36431-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="36431-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="36431-141">-Tag</span></span>
<span data-ttu-id="36431-142">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="36431-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="36431-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="36431-143">-Zone</span></span>
<span data-ttu-id="36431-144">Az elérhetőségi zónák listája, melyben az a zóna szerepel, amelyben a Nat Átjárót telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="36431-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="36431-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36431-145">-Confirm</span></span>
<span data-ttu-id="36431-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36431-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36431-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36431-147">-WhatIf</span></span>
<span data-ttu-id="36431-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36431-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36431-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36431-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36431-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36431-150">CommonParameters</span></span>
<span data-ttu-id="36431-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36431-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36431-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36431-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36431-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36431-153">INPUTS</span></span>

### <span data-ttu-id="36431-154">System.String</span><span class="sxs-lookup"><span data-stu-id="36431-154">System.String</span></span>

### <span data-ttu-id="36431-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="36431-155">System.Int32</span></span>

### <span data-ttu-id="36431-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="36431-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="36431-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="36431-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="36431-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36431-158">OUTPUTS</span></span>

### <span data-ttu-id="36431-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="36431-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="36431-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36431-160">NOTES</span></span>

## <span data-ttu-id="36431-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36431-161">RELATED LINKS</span></span>
