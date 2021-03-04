---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 4e328d28ebe7faafa942d4f3448108a174f2aa71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920465"
---
# <span data-ttu-id="e1d4d-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1d4d-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="e1d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d4d-103">Módosított Azure tűzfal-házirend mentése</span><span class="sxs-lookup"><span data-stu-id="e1d4d-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="e1d4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1d4d-104">SYNTAX</span></span>

### <span data-ttu-id="e1d4d-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1d4d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d4d-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d4d-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d4d-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d4d-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d4d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="e1d4d-109">A **Set-AzFirewallPolicy** parancsmag frissíti az Azure tűzfal házirendet.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="e1d4d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1d4d-110">EXAMPLES</span></span>

### <span data-ttu-id="e1d4d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e1d4d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="e1d4d-112">Ebben a példában a tűzfal házirendet az új tűzfal házirendértékkel állítja be</span><span class="sxs-lookup"><span data-stu-id="e1d4d-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="e1d4d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1d4d-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="e1d4d-114">Ez a példa beállítja a tűzfal házirendet az új veszélyforrás-intel móddal</span><span class="sxs-lookup"><span data-stu-id="e1d4d-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="e1d4d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e1d4d-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="e1d4d-116">Ebben a példában a tűzfal házirendje az új veszélyforrás-intel whitelistát állítja be</span><span class="sxs-lookup"><span data-stu-id="e1d4d-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="e1d4d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d4d-117">PARAMETERS</span></span>

### <span data-ttu-id="e1d4d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1d4d-118">-AsJob</span></span>
<span data-ttu-id="e1d4d-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e1d4d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1d4d-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="e1d4d-120">-BasePolicy</span></span>
<span data-ttu-id="e1d4d-121">Az alap házirend, amelytől örökölni kell</span><span class="sxs-lookup"><span data-stu-id="e1d4d-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="e1d4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d4d-122">-DefaultProfile</span></span>
<span data-ttu-id="e1d4d-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1d4d-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e1d4d-124">-DnsSetting</span></span>
<span data-ttu-id="e1d4d-125">A DNS-beállítás</span><span class="sxs-lookup"><span data-stu-id="e1d4d-125">The DNS Setting</span></span>

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

### <span data-ttu-id="e1d4d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1d4d-126">-InputObject</span></span>
<span data-ttu-id="e1d4d-127">Az AzureFirewall házirend</span><span class="sxs-lookup"><span data-stu-id="e1d4d-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d4d-128">-Location</span><span class="sxs-lookup"><span data-stu-id="e1d4d-128">-Location</span></span>
<span data-ttu-id="e1d4d-129">helyére.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d4d-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e1d4d-130">-Name</span></span>
<span data-ttu-id="e1d4d-131">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d4d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d4d-132">-ResourceGroupName</span></span>
<span data-ttu-id="e1d4d-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d4d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1d4d-134">-ResourceId</span></span>
<span data-ttu-id="e1d4d-135">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d4d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1d4d-136">-Tag</span></span>
<span data-ttu-id="e1d4d-137">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e1d4d-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="e1d4d-138">-ThreatIntelMode</span></span>
<span data-ttu-id="e1d4d-139">A veszélyforrás-felderítés műveleti módja.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="e1d4d-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e1d4d-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="e1d4d-141">The whitelist for Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="e1d4d-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="e1d4d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1d4d-142">-Confirm</span></span>
<span data-ttu-id="e1d4d-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d4d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d4d-144">-WhatIf</span></span>
<span data-ttu-id="e1d4d-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d4d-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d4d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d4d-147">CommonParameters</span></span>
<span data-ttu-id="e1d4d-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d4d-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1d4d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d4d-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1d4d-150">INPUTS</span></span>

### <span data-ttu-id="e1d4d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d4d-151">System.String</span></span>

### <span data-ttu-id="e1d4d-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1d4d-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="e1d4d-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1d4d-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e1d4d-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1d4d-154">OUTPUTS</span></span>

### <span data-ttu-id="e1d4d-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e1d4d-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e1d4d-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1d4d-156">NOTES</span></span>

## <span data-ttu-id="e1d4d-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1d4d-157">RELATED LINKS</span></span>
