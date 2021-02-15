---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 25a81344d9d8d5b8af8eed907bce7977408515ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151731"
---
# <span data-ttu-id="4aa7d-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="4aa7d-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="4aa7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa7d-103">Új Azure tűzfal-házirend alkalmazásszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="4aa7d-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="4aa7d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4aa7d-104">SYNTAX</span></span>

### <span data-ttu-id="4aa7d-105">SourceAddressAndTargetFqdn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4aa7d-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa7d-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="4aa7d-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa7d-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="4aa7d-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa7d-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="4aa7d-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa7d-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="4aa7d-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa7d-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="4aa7d-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa7d-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="4aa7d-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa7d-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="4aa7d-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa7d-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4aa7d-113">DESCRIPTION</span></span>
<span data-ttu-id="4aa7d-114">A **New-AzFirewallPolicyApplicationRule** parancsmag alkalmazásszabályt hoz létre az Azure tűzfal házirendjére.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="4aa7d-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4aa7d-115">EXAMPLES</span></span>

### <span data-ttu-id="4aa7d-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="4aa7d-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="4aa7d-117">Ebben a példában egy alkalmazásszabályt hoz létre a forráscím, a protokoll és a cél fqdns címével.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="4aa7d-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="4aa7d-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="4aa7d-119">Ebben a példában egy alkalmazásszabályt hoz létre a forráscím, a protokoll és a webes kategóriákkal.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="4aa7d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aa7d-120">PARAMETERS</span></span>

### <span data-ttu-id="4aa7d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa7d-121">-DefaultProfile</span></span>
<span data-ttu-id="4aa7d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa7d-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4aa7d-123">-Description</span></span>
<span data-ttu-id="4aa7d-124">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="4aa7d-124">The description of the rule</span></span>

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

### <span data-ttu-id="4aa7d-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="4aa7d-125">-FqdnTag</span></span>
<span data-ttu-id="4aa7d-126">A szabály teljes tartományhoz (FQDN) címkéi</span><span class="sxs-lookup"><span data-stu-id="4aa7d-126">The FQDN Tags of the rule</span></span>

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

### <span data-ttu-id="4aa7d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4aa7d-127">-Name</span></span>
<span data-ttu-id="4aa7d-128">Az alkalmazásszabály neve</span><span class="sxs-lookup"><span data-stu-id="4aa7d-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="4aa7d-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4aa7d-129">-Protocol</span></span>
<span data-ttu-id="4aa7d-130">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="4aa7d-130">The protocols of the rule</span></span>

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

### <span data-ttu-id="4aa7d-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4aa7d-131">-SourceAddress</span></span>
<span data-ttu-id="4aa7d-132">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="4aa7d-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="4aa7d-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="4aa7d-133">-SourceIpGroup</span></span>
<span data-ttu-id="4aa7d-134">A szabály forrás ip-csoportjai</span><span class="sxs-lookup"><span data-stu-id="4aa7d-134">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="4aa7d-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="4aa7d-135">-TargetFqdn</span></span>
<span data-ttu-id="4aa7d-136">A szabály cél FQDN-ei</span><span class="sxs-lookup"><span data-stu-id="4aa7d-136">The target FQDNs of the rule</span></span>

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

### <span data-ttu-id="4aa7d-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="4aa7d-137">-WebCategory</span></span>
<span data-ttu-id="4aa7d-138">A szabály webes kategóriái</span><span class="sxs-lookup"><span data-stu-id="4aa7d-138">The Web Categories of the rule</span></span>

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

### <span data-ttu-id="4aa7d-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="4aa7d-139">-TargetUrl</span></span>
<span data-ttu-id="4aa7d-140">A szabály cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="4aa7d-140">The Target Url of the rule</span></span>

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

### <span data-ttu-id="4aa7d-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="4aa7d-141">-TerminateTLS</span></span>
<span data-ttu-id="4aa7d-142">A TLS megszüntetését jelzi</span><span class="sxs-lookup"><span data-stu-id="4aa7d-142">Indicates terminating TLS</span></span>

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

### <span data-ttu-id="4aa7d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa7d-143">CommonParameters</span></span>
<span data-ttu-id="4aa7d-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa7d-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aa7d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa7d-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4aa7d-146">INPUTS</span></span>

### <span data-ttu-id="4aa7d-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="4aa7d-147">None</span></span>

## <span data-ttu-id="4aa7d-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aa7d-148">OUTPUTS</span></span>

### <span data-ttu-id="4aa7d-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="4aa7d-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="4aa7d-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4aa7d-150">NOTES</span></span>

## <span data-ttu-id="4aa7d-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4aa7d-151">RELATED LINKS</span></span>
