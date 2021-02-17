---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156739"
---
# <span data-ttu-id="e6572-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e6572-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="e6572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6572-102">SYNOPSIS</span></span>
<span data-ttu-id="e6572-103">Módosított Azure tűzfal-házirend mentése</span><span class="sxs-lookup"><span data-stu-id="e6572-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="e6572-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6572-104">SYNTAX</span></span>

### <span data-ttu-id="e6572-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6572-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6572-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6572-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6572-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6572-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6572-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6572-108">DESCRIPTION</span></span>
<span data-ttu-id="e6572-109">A **Set-AzFirewallPolicy** parancsmag frissíti az Azure tűzfal házirendet.</span><span class="sxs-lookup"><span data-stu-id="e6572-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="e6572-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6572-110">EXAMPLES</span></span>

### <span data-ttu-id="e6572-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6572-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="e6572-112">Ebben a példában a tűzfal házirendet az új tűzfal házirendértékkel állítja be</span><span class="sxs-lookup"><span data-stu-id="e6572-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="e6572-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e6572-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="e6572-114">Ez a példa beállítja a tűzfal házirendet az új veszélyforrás-intel móddal</span><span class="sxs-lookup"><span data-stu-id="e6572-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="e6572-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e6572-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="e6572-116">Ebben a példában a tűzfal házirendje az új veszélyforrás-intel whitelistát állítja be</span><span class="sxs-lookup"><span data-stu-id="e6572-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="e6572-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6572-117">PARAMETERS</span></span>

### <span data-ttu-id="e6572-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6572-118">-AsJob</span></span>
<span data-ttu-id="e6572-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6572-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6572-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="e6572-120">-BasePolicy</span></span>
<span data-ttu-id="e6572-121">Az alap házirend, amelytől örökölni kell</span><span class="sxs-lookup"><span data-stu-id="e6572-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="e6572-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6572-122">-DefaultProfile</span></span>
<span data-ttu-id="e6572-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6572-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6572-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e6572-124">-DnsSetting</span></span>
<span data-ttu-id="e6572-125">A DNS-beállítás</span><span class="sxs-lookup"><span data-stu-id="e6572-125">The DNS Setting</span></span>

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

### <span data-ttu-id="e6572-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6572-126">-InputObject</span></span>
<span data-ttu-id="e6572-127">Az AzureFirewall házirend</span><span class="sxs-lookup"><span data-stu-id="e6572-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="e6572-128">-Location</span><span class="sxs-lookup"><span data-stu-id="e6572-128">-Location</span></span>
<span data-ttu-id="e6572-129">helyére.</span><span class="sxs-lookup"><span data-stu-id="e6572-129">location.</span></span>

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

### <span data-ttu-id="e6572-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e6572-130">-Name</span></span>
<span data-ttu-id="e6572-131">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e6572-131">The resource name.</span></span>

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

### <span data-ttu-id="e6572-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6572-132">-ResourceGroupName</span></span>
<span data-ttu-id="e6572-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6572-133">The resource group name.</span></span>

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

### <span data-ttu-id="e6572-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6572-134">-ResourceId</span></span>
<span data-ttu-id="e6572-135">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6572-135">The resource Id.</span></span>

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

### <span data-ttu-id="e6572-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6572-136">-Tag</span></span>
<span data-ttu-id="e6572-137">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="e6572-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e6572-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="e6572-138">-ThreatIntelMode</span></span>
<span data-ttu-id="e6572-139">A veszélyforrás-felderítés műveleti módja.</span><span class="sxs-lookup"><span data-stu-id="e6572-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="e6572-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e6572-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="e6572-141">The whitelist for Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="e6572-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="e6572-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6572-142">-Confirm</span></span>
<span data-ttu-id="e6572-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6572-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6572-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6572-144">-WhatIf</span></span>
<span data-ttu-id="e6572-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6572-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6572-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6572-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6572-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6572-147">CommonParameters</span></span>
<span data-ttu-id="e6572-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6572-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6572-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6572-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6572-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6572-150">INPUTS</span></span>

### <span data-ttu-id="e6572-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e6572-151">System.String</span></span>

### <span data-ttu-id="e6572-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e6572-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="e6572-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6572-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e6572-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6572-154">OUTPUTS</span></span>

### <span data-ttu-id="e6572-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e6572-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e6572-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6572-156">NOTES</span></span>

## <span data-ttu-id="e6572-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6572-157">RELATED LINKS</span></span>
