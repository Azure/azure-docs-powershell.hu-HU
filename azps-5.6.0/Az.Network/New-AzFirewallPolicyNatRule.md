---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 2ba006beef1c698c12086ef65efca0213920092c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936754"
---
# <span data-ttu-id="c32c1-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="c32c1-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="c32c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c32c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c32c1-103">Új Azure Firewall Policy NAT-szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="c32c1-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="c32c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c32c1-104">SYNTAX</span></span>

### <span data-ttu-id="c32c1-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c32c1-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c32c1-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c32c1-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c32c1-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c32c1-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c32c1-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c32c1-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c32c1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c32c1-109">DESCRIPTION</span></span>
<span data-ttu-id="c32c1-110">A **New-AzFirewallPolicyNatRule** parancsmag NAT-szabályt hoz létre az Azure tűzfal-házirendhez.</span><span class="sxs-lookup"><span data-stu-id="c32c1-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c32c1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c32c1-111">EXAMPLES</span></span>

### <span data-ttu-id="c32c1-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c32c1-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="c32c1-113">Ebben a példában egy NAT-szabályt hoz létre a forráscím, a protokoll, a célcím, a célport, a lefordított cím és a lefordított port alapján.</span><span class="sxs-lookup"><span data-stu-id="c32c1-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="c32c1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c32c1-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="c32c1-115">Ebben a példában egy NAT-szabályt hoz létre a forráscím, a protokoll, a célcím, a célport, a lefordított fqdn és a lefordított port alapján.</span><span class="sxs-lookup"><span data-stu-id="c32c1-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="c32c1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c32c1-116">PARAMETERS</span></span>

### <span data-ttu-id="c32c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32c1-117">-DefaultProfile</span></span>
<span data-ttu-id="c32c1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c32c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c32c1-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c32c1-119">-Description</span></span>
<span data-ttu-id="c32c1-120">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="c32c1-120">The description of the rule</span></span>

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

### <span data-ttu-id="c32c1-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c32c1-121">-DestinationAddress</span></span>
<span data-ttu-id="c32c1-122">A szabály célcíme.</span><span class="sxs-lookup"><span data-stu-id="c32c1-122">The destination addresses of the rule.</span></span> <span data-ttu-id="c32c1-123">Ennek a tűzfal nyilvános IP-címének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c32c1-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32c1-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c32c1-124">-DestinationPort</span></span>
<span data-ttu-id="c32c1-125">A szabály célportjai</span><span class="sxs-lookup"><span data-stu-id="c32c1-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32c1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c32c1-126">-Name</span></span>
<span data-ttu-id="c32c1-127">A NAT-szabálygyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="c32c1-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="c32c1-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c32c1-128">-Protocol</span></span>
<span data-ttu-id="c32c1-129">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="c32c1-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32c1-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="c32c1-130">-SourceAddress</span></span>
<span data-ttu-id="c32c1-131">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="c32c1-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32c1-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="c32c1-132">-SourceIpGroup</span></span>
<span data-ttu-id="c32c1-133">A szabály forrás IP-csoportjai</span><span class="sxs-lookup"><span data-stu-id="c32c1-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32c1-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c32c1-134">-TranslatedAddress</span></span>
<span data-ttu-id="c32c1-135">A NAT-szabály lefordított címe</span><span class="sxs-lookup"><span data-stu-id="c32c1-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32c1-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c32c1-136">-TranslatedFqdn</span></span>
<span data-ttu-id="c32c1-137">A NAT-szabály lefordított teljes tartománya</span><span class="sxs-lookup"><span data-stu-id="c32c1-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32c1-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="c32c1-138">-TranslatedPort</span></span>
<span data-ttu-id="c32c1-139">A NAT-szabály lefordított portja</span><span class="sxs-lookup"><span data-stu-id="c32c1-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="c32c1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32c1-140">CommonParameters</span></span>
<span data-ttu-id="c32c1-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32c1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32c1-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c32c1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32c1-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c32c1-143">INPUTS</span></span>

### <span data-ttu-id="c32c1-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="c32c1-144">None</span></span>

## <span data-ttu-id="c32c1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c32c1-145">OUTPUTS</span></span>

### <span data-ttu-id="c32c1-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c32c1-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="c32c1-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c32c1-147">NOTES</span></span>

## <span data-ttu-id="c32c1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c32c1-148">RELATED LINKS</span></span>
