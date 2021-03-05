---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 0c7e29b0c9b59842e885cf8763da63c2d65cfff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001110"
---
# <span data-ttu-id="008a5-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="008a5-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="008a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="008a5-102">SYNOPSIS</span></span>
<span data-ttu-id="008a5-103">Új Azure tűzfal-házirend alkalmazásszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="008a5-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="008a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="008a5-104">SYNTAX</span></span>

### <span data-ttu-id="008a5-105">SourceAddressAndTargetFqdn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="008a5-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008a5-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="008a5-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008a5-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="008a5-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008a5-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="008a5-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008a5-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="008a5-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008a5-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="008a5-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008a5-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="008a5-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008a5-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="008a5-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="008a5-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="008a5-113">DESCRIPTION</span></span>
<span data-ttu-id="008a5-114">A **New-AzFirewallPolicyApplicationRule** parancsmag alkalmazásszabályt hoz létre az Azure tűzfal házirendjére.</span><span class="sxs-lookup"><span data-stu-id="008a5-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="008a5-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="008a5-115">EXAMPLES</span></span>

### <span data-ttu-id="008a5-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="008a5-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="008a5-117">Ebben a példában egy alkalmazásszabályt hoz létre a forráscím, a protokoll és a cél fqdns címével.</span><span class="sxs-lookup"><span data-stu-id="008a5-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="008a5-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="008a5-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="008a5-119">Ebben a példában egy alkalmazásszabályt hoz létre a forráscím, a protokoll és a webes kategóriákkal.</span><span class="sxs-lookup"><span data-stu-id="008a5-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="008a5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="008a5-120">PARAMETERS</span></span>

### <span data-ttu-id="008a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008a5-121">-DefaultProfile</span></span>
<span data-ttu-id="008a5-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="008a5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="008a5-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="008a5-123">-Description</span></span>
<span data-ttu-id="008a5-124">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="008a5-124">The description of the rule</span></span>

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

### <span data-ttu-id="008a5-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="008a5-125">-FqdnTag</span></span>
<span data-ttu-id="008a5-126">A szabály teljes tartományhoz (FQDN) címkéi</span><span class="sxs-lookup"><span data-stu-id="008a5-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008a5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="008a5-127">-Name</span></span>
<span data-ttu-id="008a5-128">Az alkalmazásszabály neve</span><span class="sxs-lookup"><span data-stu-id="008a5-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="008a5-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="008a5-129">-Protocol</span></span>
<span data-ttu-id="008a5-130">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="008a5-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008a5-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="008a5-131">-SourceAddress</span></span>
<span data-ttu-id="008a5-132">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="008a5-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008a5-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="008a5-133">-SourceIpGroup</span></span>
<span data-ttu-id="008a5-134">A szabály forrás IP-csoportjai</span><span class="sxs-lookup"><span data-stu-id="008a5-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008a5-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="008a5-135">-TargetFqdn</span></span>
<span data-ttu-id="008a5-136">A szabály cél FQDN-ei</span><span class="sxs-lookup"><span data-stu-id="008a5-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008a5-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="008a5-137">-WebCategory</span></span>
<span data-ttu-id="008a5-138">A szabály webes kategóriái</span><span class="sxs-lookup"><span data-stu-id="008a5-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008a5-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="008a5-139">-TargetUrl</span></span>
<span data-ttu-id="008a5-140">A szabály cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="008a5-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008a5-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="008a5-141">-TerminateTLS</span></span>
<span data-ttu-id="008a5-142">A TLS megszüntetését jelzi</span><span class="sxs-lookup"><span data-stu-id="008a5-142">Indicates terminating TLS</span></span>

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

### <span data-ttu-id="008a5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008a5-143">CommonParameters</span></span>
<span data-ttu-id="008a5-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008a5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008a5-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="008a5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008a5-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="008a5-146">INPUTS</span></span>

### <span data-ttu-id="008a5-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="008a5-147">None</span></span>

## <span data-ttu-id="008a5-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="008a5-148">OUTPUTS</span></span>

### <span data-ttu-id="008a5-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="008a5-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="008a5-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="008a5-150">NOTES</span></span>

## <span data-ttu-id="008a5-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="008a5-151">RELATED LINKS</span></span>
