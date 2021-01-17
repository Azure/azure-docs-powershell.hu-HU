---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469013"
---
# <span data-ttu-id="db73d-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="db73d-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="db73d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db73d-102">SYNOPSIS</span></span>
<span data-ttu-id="db73d-103">Új Azure tűzfal-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="db73d-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="db73d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db73d-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db73d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db73d-105">DESCRIPTION</span></span>
<span data-ttu-id="db73d-106">A **New-AzFirewallPolicy** parancsmag létrehoz egy Azure tűzfalházi házirendet.</span><span class="sxs-lookup"><span data-stu-id="db73d-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="db73d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db73d-107">EXAMPLES</span></span>

### <span data-ttu-id="db73d-108">1. példa: 1.</span><span class="sxs-lookup"><span data-stu-id="db73d-108">Example 1: 1.</span></span> <span data-ttu-id="db73d-109">Üres házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="db73d-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="db73d-110">Ebben a példában egy Azure tűzfal-házirendet hoz létre</span><span class="sxs-lookup"><span data-stu-id="db73d-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="db73d-111">2. példa: 2.</span><span class="sxs-lookup"><span data-stu-id="db73d-111">Example 2: 2.</span></span> <span data-ttu-id="db73d-112">Üres házirend létrehozása a ThreatIntel módban</span><span class="sxs-lookup"><span data-stu-id="db73d-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="db73d-113">Ebben a példában egy veszélyforrás-intel módú Azure tűzfal-házirendet hoz létre</span><span class="sxs-lookup"><span data-stu-id="db73d-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="db73d-114">3. példa: 3.</span><span class="sxs-lookup"><span data-stu-id="db73d-114">Example 3: 3.</span></span> <span data-ttu-id="db73d-115">Üres házirend létrehozása a ThreatIntel Whitelist segítségével</span><span class="sxs-lookup"><span data-stu-id="db73d-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="db73d-116">Ez a példa létrehoz egy Azure tűzfal házirendet veszélyforrás-intel whitelistával</span><span class="sxs-lookup"><span data-stu-id="db73d-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="db73d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db73d-117">PARAMETERS</span></span>

### <span data-ttu-id="db73d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db73d-118">-AsJob</span></span>
<span data-ttu-id="db73d-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="db73d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db73d-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="db73d-120">-BasePolicy</span></span>
<span data-ttu-id="db73d-121">Az alap házirend, amelytől örökölni kell</span><span class="sxs-lookup"><span data-stu-id="db73d-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="db73d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db73d-122">-DefaultProfile</span></span>
<span data-ttu-id="db73d-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db73d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db73d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="db73d-124">-Force</span></span>
<span data-ttu-id="db73d-125">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="db73d-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="db73d-126">-Location</span><span class="sxs-lookup"><span data-stu-id="db73d-126">-Location</span></span>
<span data-ttu-id="db73d-127">helyére.</span><span class="sxs-lookup"><span data-stu-id="db73d-127">location.</span></span>

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

### <span data-ttu-id="db73d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="db73d-128">-Name</span></span>
<span data-ttu-id="db73d-129">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="db73d-129">The resource name.</span></span>

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

### <span data-ttu-id="db73d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db73d-130">-ResourceGroupName</span></span>
<span data-ttu-id="db73d-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db73d-131">The resource group name.</span></span>

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

### <span data-ttu-id="db73d-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="db73d-132">-Tag</span></span>
<span data-ttu-id="db73d-133">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="db73d-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="db73d-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="db73d-134">-ThreatIntelMode</span></span>
<span data-ttu-id="db73d-135">A veszélyforrás-felderítés műveleti módja.</span><span class="sxs-lookup"><span data-stu-id="db73d-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db73d-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="db73d-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="db73d-137">The whitelist for Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="db73d-137">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db73d-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="db73d-138">-DnsSetting</span></span>
<span data-ttu-id="db73d-139">A DNS-beállítás</span><span class="sxs-lookup"><span data-stu-id="db73d-139">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db73d-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db73d-140">-Confirm</span></span>
<span data-ttu-id="db73d-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db73d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db73d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db73d-142">-WhatIf</span></span>
<span data-ttu-id="db73d-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db73d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db73d-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db73d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db73d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db73d-145">CommonParameters</span></span>
<span data-ttu-id="db73d-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db73d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db73d-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db73d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db73d-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db73d-148">INPUTS</span></span>

### <span data-ttu-id="db73d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="db73d-149">System.String</span></span>

### <span data-ttu-id="db73d-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="db73d-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db73d-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db73d-151">OUTPUTS</span></span>

### <span data-ttu-id="db73d-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="db73d-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="db73d-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db73d-153">NOTES</span></span>

## <span data-ttu-id="db73d-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db73d-154">RELATED LINKS</span></span>
