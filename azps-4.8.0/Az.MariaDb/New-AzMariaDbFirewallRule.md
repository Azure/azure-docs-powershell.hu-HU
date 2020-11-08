---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024727"
---
# <span data-ttu-id="f47f4-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f47f4-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="f47f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f47f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f47f4-103">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="f47f4-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f47f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f47f4-104">SYNTAX</span></span>

### <span data-ttu-id="f47f4-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f47f4-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f47f4-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="f47f4-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f47f4-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f47f4-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f47f4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f47f4-108">DESCRIPTION</span></span>
<span data-ttu-id="f47f4-109">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="f47f4-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f47f4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f47f4-110">EXAMPLES</span></span>

### <span data-ttu-id="f47f4-111">Példa 1: tűzfalszabály létrehozása egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="f47f4-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="f47f4-112">Ez a parancs a MariaDB csoportban hoz létre tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="f47f4-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="f47f4-113">2. példa: új MariaDB-tűzfal-szabály létrehozása a-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="f47f4-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="f47f4-114">Ezzel a parancsmaggal létrehozhatja a MariaDB-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="f47f4-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="f47f4-115">3. példa: új MariaDB-tűzfalszabályok létrehozása az összes IPs engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f47f4-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="f47f4-116">Ezzel a parancsmaggal új MariaDB-tűzfalszabályok hozhatók létre az összes IP-hez.</span><span class="sxs-lookup"><span data-stu-id="f47f4-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="f47f4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f47f4-117">PARAMETERS</span></span>

### <span data-ttu-id="f47f4-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="f47f4-118">-AllowAll</span></span>
<span data-ttu-id="f47f4-119">A 0.0.0.0-től a 255.255.255.255-ig terjedő összes IP-t engedélyezni kell.</span><span class="sxs-lookup"><span data-stu-id="f47f4-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47f4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f47f4-120">-AsJob</span></span>
<span data-ttu-id="f47f4-121">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="f47f4-121">Run the command as a job</span></span>

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

### <span data-ttu-id="f47f4-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f47f4-122">-ClientIPAddress</span></span>
<span data-ttu-id="f47f4-123">Ügyfél: a kiszolgálói tűzfalszabályok egyetlen IP-címe van megadva.</span><span class="sxs-lookup"><span data-stu-id="f47f4-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="f47f4-124">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f47f4-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47f4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47f4-125">-DefaultProfile</span></span>
<span data-ttu-id="f47f4-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f47f4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47f4-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="f47f4-127">-EndIPAddress</span></span>
<span data-ttu-id="f47f4-128">A kiszolgáló tűzfal-szabályának End IP-címe.</span><span class="sxs-lookup"><span data-stu-id="f47f4-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="f47f4-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f47f4-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47f4-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f47f4-130">-Name</span></span>
<span data-ttu-id="f47f4-131">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="f47f4-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="f47f4-132">Ha nincs megadva, az alapértelmezett érték nincs definiálva.</span><span class="sxs-lookup"><span data-stu-id="f47f4-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="f47f4-133">Ha a AllowAll létezik, az alapértelmezett név AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="f47f4-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47f4-134">-Várva</span><span class="sxs-lookup"><span data-stu-id="f47f4-134">-NoWait</span></span>
<span data-ttu-id="f47f4-135">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="f47f4-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f47f4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47f4-136">-ResourceGroupName</span></span>
<span data-ttu-id="f47f4-137">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f47f4-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f47f4-138">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f47f4-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f47f4-139">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f47f4-139">-ServerName</span></span>
<span data-ttu-id="f47f4-140">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f47f4-140">The name of the server.</span></span>

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

### <span data-ttu-id="f47f4-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="f47f4-141">-StartIPAddress</span></span>
<span data-ttu-id="f47f4-142">A kiszolgáló tűzfal-szabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="f47f4-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="f47f4-143">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f47f4-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47f4-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f47f4-144">-SubscriptionId</span></span>
<span data-ttu-id="f47f4-145">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f47f4-145">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47f4-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f47f4-146">-Confirm</span></span>
<span data-ttu-id="f47f4-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f47f4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47f4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47f4-148">-WhatIf</span></span>
<span data-ttu-id="f47f4-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f47f4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f47f4-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f47f4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47f4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47f4-151">CommonParameters</span></span>
<span data-ttu-id="f47f4-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f47f4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47f4-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f47f4-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47f4-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f47f4-154">INPUTS</span></span>

## <span data-ttu-id="f47f4-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f47f4-155">OUTPUTS</span></span>

### <span data-ttu-id="f47f4-156">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f47f4-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="f47f4-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f47f4-157">NOTES</span></span>

<span data-ttu-id="f47f4-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f47f4-158">ALIASES</span></span>

## <span data-ttu-id="f47f4-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f47f4-159">RELATED LINKS</span></span>

