---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184778"
---
# <span data-ttu-id="6b5b4-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6b5b4-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="6b5b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="6b5b4-103">Módosított Azure tűzfal-házirend mentése</span><span class="sxs-lookup"><span data-stu-id="6b5b4-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="6b5b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b5b4-104">SYNTAX</span></span>

### <span data-ttu-id="6b5b4-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b5b4-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b5b4-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5b4-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b5b4-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5b4-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b5b4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b5b4-108">DESCRIPTION</span></span>
<span data-ttu-id="6b5b4-109">A **set-AzFirewallPolicy** parancsmag egy Azure tűzfal-házirendet frissít.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="6b5b4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6b5b4-110">EXAMPLES</span></span>

### <span data-ttu-id="6b5b4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6b5b4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="6b5b4-112">Ez a példa beállítja a tűzfal házirendjét az új tűzfal házirend-értékkel.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="6b5b4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6b5b4-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="6b5b4-114">Ebben a példában a tűzfal-házirendet az új veszélyforrás Intel módra állítja be</span><span class="sxs-lookup"><span data-stu-id="6b5b4-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="6b5b4-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="6b5b4-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="6b5b4-116">Ez a példa beállítja a tűzfal házirendjét az új veszélyforrás az Intel whitelist szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="6b5b4-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="6b5b4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b5b4-117">PARAMETERS</span></span>

### <span data-ttu-id="6b5b4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b5b4-118">-AsJob</span></span>
<span data-ttu-id="6b5b4-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6b5b4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b5b4-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="6b5b4-120">-BasePolicy</span></span>
<span data-ttu-id="6b5b4-121">Az alapházirend, amelyet örökölni szeretne</span><span class="sxs-lookup"><span data-stu-id="6b5b4-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="6b5b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b5b4-122">-DefaultProfile</span></span>
<span data-ttu-id="6b5b4-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b5b4-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="6b5b4-124">-DnsSetting</span></span>
<span data-ttu-id="6b5b4-125">A DNS-beállítás</span><span class="sxs-lookup"><span data-stu-id="6b5b4-125">The DNS Setting</span></span>

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

### <span data-ttu-id="6b5b4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b5b4-126">-InputObject</span></span>
<span data-ttu-id="6b5b4-127">A AzureFirewall házirend</span><span class="sxs-lookup"><span data-stu-id="6b5b4-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="6b5b4-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="6b5b4-128">-Location</span></span>
<span data-ttu-id="6b5b4-129">helyre.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-129">location.</span></span>

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

### <span data-ttu-id="6b5b4-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b5b4-130">-Name</span></span>
<span data-ttu-id="6b5b4-131">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-131">The resource name.</span></span>

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

### <span data-ttu-id="6b5b4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b5b4-132">-ResourceGroupName</span></span>
<span data-ttu-id="6b5b4-133">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-133">The resource group name.</span></span>

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

### <span data-ttu-id="6b5b4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b5b4-134">-ResourceId</span></span>
<span data-ttu-id="6b5b4-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-135">The resource Id.</span></span>

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

### <span data-ttu-id="6b5b4-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="6b5b4-136">-Tag</span></span>
<span data-ttu-id="6b5b4-137">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6b5b4-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="6b5b4-138">-ThreatIntelMode</span></span>
<span data-ttu-id="6b5b4-139">A veszélyforrások felderítésének üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="6b5b4-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="6b5b4-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="6b5b4-141">A fenyegetések elleni intelligencia whitelist (whitelist)</span><span class="sxs-lookup"><span data-stu-id="6b5b4-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="6b5b4-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b5b4-142">-Confirm</span></span>
<span data-ttu-id="6b5b4-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b5b4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b5b4-144">-WhatIf</span></span>
<span data-ttu-id="6b5b4-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b5b4-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b5b4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b5b4-147">CommonParameters</span></span>
<span data-ttu-id="6b5b4-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b5b4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b5b4-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6b5b4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b5b4-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b5b4-150">INPUTS</span></span>

### <span data-ttu-id="6b5b4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6b5b4-151">System.String</span></span>

### <span data-ttu-id="6b5b4-152">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6b5b4-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="6b5b4-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6b5b4-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6b5b4-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b5b4-154">OUTPUTS</span></span>

### <span data-ttu-id="6b5b4-155">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6b5b4-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="6b5b4-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b5b4-156">NOTES</span></span>

## <span data-ttu-id="6b5b4-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b5b4-157">RELATED LINKS</span></span>
