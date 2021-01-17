---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330713"
---
# <span data-ttu-id="3f513-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f513-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="3f513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f513-102">SYNOPSIS</span></span>
<span data-ttu-id="3f513-103">Privát hivatkozásszolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="3f513-103">Creates a private link service</span></span>

## <span data-ttu-id="3f513-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f513-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f513-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f513-105">DESCRIPTION</span></span>
<span data-ttu-id="3f513-106">A **New-AzPrivateLinkService** parancsmag privát hivatkozásszolgáltatást hoz létre</span><span class="sxs-lookup"><span data-stu-id="3f513-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="3f513-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f513-107">EXAMPLES</span></span>

### <span data-ttu-id="3f513-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3f513-108">Example 1</span></span>

<span data-ttu-id="3f513-109">Az alábbi példa létrehoz egy privát hivatkozásszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="3f513-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="3f513-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f513-110">PARAMETERS</span></span>

### <span data-ttu-id="3f513-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f513-111">-AsJob</span></span>
<span data-ttu-id="3f513-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f513-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f513-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="3f513-113">-AutoApproval</span></span>
<span data-ttu-id="3f513-114">A privát hivatkozásszolgáltatás automatikus jóváhagyási előfizetései</span><span class="sxs-lookup"><span data-stu-id="3f513-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="3f513-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f513-115">-DefaultProfile</span></span>
<span data-ttu-id="3f513-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f513-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f513-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="3f513-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="3f513-118">Proxy protokoll engedélyezése a privát csatolási szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="3f513-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="3f513-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3f513-119">-Force</span></span>
<span data-ttu-id="3f513-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="3f513-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3f513-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f513-121">-IpConfiguration</span></span>
<span data-ttu-id="3f513-122">Az IP-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="3f513-122">The ip configurations</span></span>

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

### <span data-ttu-id="3f513-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f513-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="3f513-124">Az előlapi IP-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="3f513-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="3f513-125">-Location</span><span class="sxs-lookup"><span data-stu-id="3f513-125">-Location</span></span>
<span data-ttu-id="3f513-126">helyére.</span><span class="sxs-lookup"><span data-stu-id="3f513-126">location.</span></span>

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

### <span data-ttu-id="3f513-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3f513-127">-Name</span></span>
<span data-ttu-id="3f513-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3f513-128">The name of the service.</span></span>

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

### <span data-ttu-id="3f513-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f513-129">-ResourceGroupName</span></span>
<span data-ttu-id="3f513-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f513-130">The resource group name.</span></span>

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

### <span data-ttu-id="3f513-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f513-131">-Tag</span></span>
<span data-ttu-id="3f513-132">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="3f513-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3f513-133">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="3f513-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3f513-134">-Láthatóság</span><span class="sxs-lookup"><span data-stu-id="3f513-134">-Visibility</span></span>
<span data-ttu-id="3f513-135">A privát hivatkozásszolgáltatás láthatósági előfizetései</span><span class="sxs-lookup"><span data-stu-id="3f513-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="3f513-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f513-136">-Confirm</span></span>
<span data-ttu-id="3f513-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f513-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f513-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f513-138">-WhatIf</span></span>
<span data-ttu-id="3f513-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f513-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f513-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f513-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f513-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f513-141">CommonParameters</span></span>
<span data-ttu-id="3f513-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f513-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f513-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f513-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f513-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f513-144">INPUTS</span></span>

### <span data-ttu-id="3f513-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3f513-145">System.String</span></span>

### <span data-ttu-id="3f513-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="3f513-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="3f513-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="3f513-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="3f513-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f513-148">OUTPUTS</span></span>

### <span data-ttu-id="3f513-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f513-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="3f513-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f513-150">NOTES</span></span>

## <span data-ttu-id="3f513-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f513-151">RELATED LINKS</span></span>

[<span data-ttu-id="3f513-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f513-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="3f513-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f513-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="3f513-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f513-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
