---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184840"
---
# <span data-ttu-id="417ba-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="417ba-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="417ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="417ba-102">SYNOPSIS</span></span>
<span data-ttu-id="417ba-103">Új Azure tűzfal-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="417ba-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="417ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="417ba-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="417ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="417ba-105">DESCRIPTION</span></span>
<span data-ttu-id="417ba-106">A **New-AzFirewallPolicy** parancsmag Azure tűzfal-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="417ba-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="417ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="417ba-107">EXAMPLES</span></span>

### <span data-ttu-id="417ba-108">Példa 1:1.</span><span class="sxs-lookup"><span data-stu-id="417ba-108">Example 1: 1.</span></span> <span data-ttu-id="417ba-109">Üres házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="417ba-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="417ba-110">Ez a példa Azure tűzfal-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="417ba-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="417ba-111">Példa 2:2.</span><span class="sxs-lookup"><span data-stu-id="417ba-111">Example 2: 2.</span></span> <span data-ttu-id="417ba-112">Üres házirend létrehozása a ThreatIntel móddal</span><span class="sxs-lookup"><span data-stu-id="417ba-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="417ba-113">Ez a példa egy Azure tűzfal-házirendet hoz létre egy veszélyforrás Intel móddal</span><span class="sxs-lookup"><span data-stu-id="417ba-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="417ba-114">Példa 3:3.</span><span class="sxs-lookup"><span data-stu-id="417ba-114">Example 3: 3.</span></span> <span data-ttu-id="417ba-115">Üres házirend létrehozása a ThreatIntel whitelist szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="417ba-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="417ba-116">Ez a példa egy Azure tűzfal-házirendet hoz létre egy veszélyforrás Intel whitelist segítségével</span><span class="sxs-lookup"><span data-stu-id="417ba-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="417ba-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="417ba-117">PARAMETERS</span></span>

### <span data-ttu-id="417ba-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="417ba-118">-AsJob</span></span>
<span data-ttu-id="417ba-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="417ba-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="417ba-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="417ba-120">-BasePolicy</span></span>
<span data-ttu-id="417ba-121">Az alapházirend, amelyet örökölni szeretne</span><span class="sxs-lookup"><span data-stu-id="417ba-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="417ba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417ba-122">-DefaultProfile</span></span>
<span data-ttu-id="417ba-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="417ba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="417ba-124">-Force</span><span class="sxs-lookup"><span data-stu-id="417ba-124">-Force</span></span>
<span data-ttu-id="417ba-125">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="417ba-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="417ba-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="417ba-126">-Location</span></span>
<span data-ttu-id="417ba-127">helyre.</span><span class="sxs-lookup"><span data-stu-id="417ba-127">location.</span></span>

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

### <span data-ttu-id="417ba-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="417ba-128">-Name</span></span>
<span data-ttu-id="417ba-129">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="417ba-129">The resource name.</span></span>

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

### <span data-ttu-id="417ba-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="417ba-130">-ResourceGroupName</span></span>
<span data-ttu-id="417ba-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="417ba-131">The resource group name.</span></span>

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

### <span data-ttu-id="417ba-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="417ba-132">-Tag</span></span>
<span data-ttu-id="417ba-133">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="417ba-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="417ba-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="417ba-134">-ThreatIntelMode</span></span>
<span data-ttu-id="417ba-135">A veszélyforrások felderítésének üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="417ba-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="417ba-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="417ba-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="417ba-137">A fenyegetések elleni intelligencia whitelist (whitelist)</span><span class="sxs-lookup"><span data-stu-id="417ba-137">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="417ba-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="417ba-138">-DnsSetting</span></span>
<span data-ttu-id="417ba-139">A DNS-beállítás</span><span class="sxs-lookup"><span data-stu-id="417ba-139">The DNS Setting</span></span>

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

### <span data-ttu-id="417ba-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="417ba-140">-Confirm</span></span>
<span data-ttu-id="417ba-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="417ba-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="417ba-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="417ba-142">-WhatIf</span></span>
<span data-ttu-id="417ba-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="417ba-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="417ba-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="417ba-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="417ba-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417ba-145">CommonParameters</span></span>
<span data-ttu-id="417ba-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="417ba-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417ba-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="417ba-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417ba-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="417ba-148">INPUTS</span></span>

### <span data-ttu-id="417ba-149">System. String</span><span class="sxs-lookup"><span data-stu-id="417ba-149">System.String</span></span>

### <span data-ttu-id="417ba-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="417ba-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="417ba-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="417ba-151">OUTPUTS</span></span>

### <span data-ttu-id="417ba-152">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="417ba-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="417ba-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="417ba-153">NOTES</span></span>

## <span data-ttu-id="417ba-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="417ba-154">RELATED LINKS</span></span>
