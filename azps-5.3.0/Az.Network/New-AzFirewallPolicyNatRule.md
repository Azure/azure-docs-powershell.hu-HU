---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469002"
---
# <span data-ttu-id="c3e2b-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="c3e2b-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="c3e2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e2b-103">Új Azure Firewall Policy NAT-szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="c3e2b-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="c3e2b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3e2b-104">SYNTAX</span></span>

### <span data-ttu-id="c3e2b-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c3e2b-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e2b-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c3e2b-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e2b-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c3e2b-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e2b-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c3e2b-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e2b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3e2b-109">DESCRIPTION</span></span>
<span data-ttu-id="c3e2b-110">A **New-AzFirewallPolicyNatRule** parancsmag NAT-szabályt hoz létre az Azure tűzfal-házirendhez.</span><span class="sxs-lookup"><span data-stu-id="c3e2b-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c3e2b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3e2b-111">EXAMPLES</span></span>

### <span data-ttu-id="c3e2b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3e2b-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="c3e2b-113">Ebben a példában egy NAT-szabályt hoz létre a forráscím, a protokoll, a célcím, a célport, a lefordított cím és a lefordított port alapján.</span><span class="sxs-lookup"><span data-stu-id="c3e2b-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="c3e2b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3e2b-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="c3e2b-115">Ebben a példában egy NAT-szabályt hoz létre a forráscím, a protokoll, a célcím, a célport, a lefordított fqdn és a lefordított port alapján.</span><span class="sxs-lookup"><span data-stu-id="c3e2b-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="c3e2b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3e2b-116">PARAMETERS</span></span>

### <span data-ttu-id="c3e2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e2b-117">-DefaultProfile</span></span>
<span data-ttu-id="c3e2b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3e2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e2b-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c3e2b-119">-Description</span></span>
<span data-ttu-id="c3e2b-120">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="c3e2b-120">The description of the rule</span></span>

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

### <span data-ttu-id="c3e2b-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c3e2b-121">-DestinationAddress</span></span>
<span data-ttu-id="c3e2b-122">A szabály célcíme.</span><span class="sxs-lookup"><span data-stu-id="c3e2b-122">The destination addresses of the rule.</span></span> <span data-ttu-id="c3e2b-123">Ennek a tűzfal nyilvános IP-címének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c3e2b-123">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="c3e2b-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c3e2b-124">-DestinationPort</span></span>
<span data-ttu-id="c3e2b-125">A szabály célportjai</span><span class="sxs-lookup"><span data-stu-id="c3e2b-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="c3e2b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c3e2b-126">-Name</span></span>
<span data-ttu-id="c3e2b-127">A NAT-szabálygyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="c3e2b-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="c3e2b-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c3e2b-128">-Protocol</span></span>
<span data-ttu-id="c3e2b-129">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="c3e2b-129">The protocols of the rule</span></span>

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

### <span data-ttu-id="c3e2b-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="c3e2b-130">-SourceAddress</span></span>
<span data-ttu-id="c3e2b-131">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="c3e2b-131">The source addresses of the rule</span></span>

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

### <span data-ttu-id="c3e2b-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="c3e2b-132">-SourceIpGroup</span></span>
<span data-ttu-id="c3e2b-133">A szabály forrás IP-csoportjai</span><span class="sxs-lookup"><span data-stu-id="c3e2b-133">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="c3e2b-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c3e2b-134">-TranslatedAddress</span></span>
<span data-ttu-id="c3e2b-135">A NAT-szabály lefordított címe</span><span class="sxs-lookup"><span data-stu-id="c3e2b-135">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="c3e2b-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c3e2b-136">-TranslatedFqdn</span></span>
<span data-ttu-id="c3e2b-137">A NAT-szabály lefordított teljes tartománya</span><span class="sxs-lookup"><span data-stu-id="c3e2b-137">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="c3e2b-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="c3e2b-138">-TranslatedPort</span></span>
<span data-ttu-id="c3e2b-139">A NAT-szabály lefordított portja</span><span class="sxs-lookup"><span data-stu-id="c3e2b-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="c3e2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e2b-140">CommonParameters</span></span>
<span data-ttu-id="c3e2b-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e2b-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3e2b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e2b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3e2b-143">INPUTS</span></span>

### <span data-ttu-id="c3e2b-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="c3e2b-144">None</span></span>

## <span data-ttu-id="c3e2b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3e2b-145">OUTPUTS</span></span>

### <span data-ttu-id="c3e2b-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c3e2b-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="c3e2b-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3e2b-147">NOTES</span></span>

## <span data-ttu-id="c3e2b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3e2b-148">RELATED LINKS</span></span>
