---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151610"
---
# <span data-ttu-id="475b2-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="475b2-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="475b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475b2-102">SYNOPSIS</span></span>
<span data-ttu-id="475b2-103">Privát hivatkozásszolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="475b2-103">Creates a private link service</span></span>

## <span data-ttu-id="475b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="475b2-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="475b2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="475b2-105">DESCRIPTION</span></span>
<span data-ttu-id="475b2-106">A **New-AzPrivateLinkService** parancsmag privát hivatkozásszolgáltatást hoz létre</span><span class="sxs-lookup"><span data-stu-id="475b2-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="475b2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="475b2-107">EXAMPLES</span></span>

### <span data-ttu-id="475b2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="475b2-108">Example 1</span></span>

<span data-ttu-id="475b2-109">Az alábbi példa létrehoz egy privát hivatkozásszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="475b2-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="475b2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="475b2-110">PARAMETERS</span></span>

### <span data-ttu-id="475b2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="475b2-111">-AsJob</span></span>
<span data-ttu-id="475b2-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="475b2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="475b2-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="475b2-113">-AutoApproval</span></span>
<span data-ttu-id="475b2-114">A privát hivatkozásszolgáltatás automatikus jóváhagyási előfizetései</span><span class="sxs-lookup"><span data-stu-id="475b2-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="475b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475b2-115">-DefaultProfile</span></span>
<span data-ttu-id="475b2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="475b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="475b2-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="475b2-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="475b2-118">Proxy protokoll engedélyezése a privát csatolási szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="475b2-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="475b2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="475b2-119">-Force</span></span>
<span data-ttu-id="475b2-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="475b2-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="475b2-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="475b2-121">-IpConfiguration</span></span>
<span data-ttu-id="475b2-122">Az IP-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="475b2-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475b2-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="475b2-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="475b2-124">Az előlapi IP-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="475b2-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475b2-125">-Location</span><span class="sxs-lookup"><span data-stu-id="475b2-125">-Location</span></span>
<span data-ttu-id="475b2-126">helyére.</span><span class="sxs-lookup"><span data-stu-id="475b2-126">location.</span></span>

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

### <span data-ttu-id="475b2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="475b2-127">-Name</span></span>
<span data-ttu-id="475b2-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="475b2-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475b2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475b2-129">-ResourceGroupName</span></span>
<span data-ttu-id="475b2-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="475b2-130">The resource group name.</span></span>

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

### <span data-ttu-id="475b2-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="475b2-131">-Tag</span></span>
<span data-ttu-id="475b2-132">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="475b2-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="475b2-133">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="475b2-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="475b2-134">-Láthatóság</span><span class="sxs-lookup"><span data-stu-id="475b2-134">-Visibility</span></span>
<span data-ttu-id="475b2-135">A privát hivatkozásszolgáltatás láthatósági előfizetései</span><span class="sxs-lookup"><span data-stu-id="475b2-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="475b2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="475b2-136">-Confirm</span></span>
<span data-ttu-id="475b2-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="475b2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475b2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475b2-138">-WhatIf</span></span>
<span data-ttu-id="475b2-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="475b2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="475b2-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="475b2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475b2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475b2-141">CommonParameters</span></span>
<span data-ttu-id="475b2-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475b2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475b2-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="475b2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475b2-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="475b2-144">INPUTS</span></span>

### <span data-ttu-id="475b2-145">System.String</span><span class="sxs-lookup"><span data-stu-id="475b2-145">System.String</span></span>

### <span data-ttu-id="475b2-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="475b2-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="475b2-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="475b2-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="475b2-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="475b2-148">OUTPUTS</span></span>

### <span data-ttu-id="475b2-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="475b2-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="475b2-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="475b2-150">NOTES</span></span>

## <span data-ttu-id="475b2-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="475b2-151">RELATED LINKS</span></span>

[<span data-ttu-id="475b2-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="475b2-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="475b2-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="475b2-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="475b2-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="475b2-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
