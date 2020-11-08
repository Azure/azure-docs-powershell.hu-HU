---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195801"
---
# <span data-ttu-id="51e9a-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51e9a-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="51e9a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="51e9a-103">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="51e9a-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="51e9a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51e9a-104">SYNTAX</span></span>

### <span data-ttu-id="51e9a-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51e9a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51e9a-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="51e9a-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51e9a-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="51e9a-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51e9a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="51e9a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51e9a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="51e9a-109">DESCRIPTION</span></span>
<span data-ttu-id="51e9a-110">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="51e9a-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="51e9a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="51e9a-111">EXAMPLES</span></span>

### <span data-ttu-id="51e9a-112">1. példa: a MariaDB-tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="51e9a-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="51e9a-113">Ez a parancs frissíti a MariaDB-tűzfal szabályát.</span><span class="sxs-lookup"><span data-stu-id="51e9a-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="51e9a-114">2. példa: a MariaDB-tűzfal szabályának frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="51e9a-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="51e9a-115">A parancsmag úgy frissíti a MariaDB, hogy identitás szerint frissíti a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="51e9a-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="51e9a-116">3. példa: a MariaDB-tűzfal szabályának frissítése by-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="51e9a-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="51e9a-117">A parancsmag frissíti a MariaDB-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="51e9a-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="51e9a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51e9a-118">PARAMETERS</span></span>

### <span data-ttu-id="51e9a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51e9a-119">-AsJob</span></span>
<span data-ttu-id="51e9a-120">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="51e9a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="51e9a-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="51e9a-121">-ClientIPAddress</span></span>
<span data-ttu-id="51e9a-122">Ügyfél: a kiszolgálói tűzfalszabályok egyetlen IP-címe van megadva.</span><span class="sxs-lookup"><span data-stu-id="51e9a-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="51e9a-123">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="51e9a-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e9a-124">-DefaultProfile</span></span>
<span data-ttu-id="51e9a-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51e9a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e9a-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="51e9a-126">-EndIPAddress</span></span>
<span data-ttu-id="51e9a-127">A kiszolgáló tűzfal-szabályának End IP-címe.</span><span class="sxs-lookup"><span data-stu-id="51e9a-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="51e9a-128">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="51e9a-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51e9a-129">-InputObject</span></span>
<span data-ttu-id="51e9a-130">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51e9a-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51e9a-131">-Name</span></span>
<span data-ttu-id="51e9a-132">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="51e9a-133">-NoWait</span></span>
<span data-ttu-id="51e9a-134">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="51e9a-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="51e9a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e9a-135">-ResourceGroupName</span></span>
<span data-ttu-id="51e9a-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="51e9a-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="51e9a-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-138">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="51e9a-138">-ServerName</span></span>
<span data-ttu-id="51e9a-139">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="51e9a-140">-StartIPAddress</span></span>
<span data-ttu-id="51e9a-141">A kiszolgáló tűzfal-szabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="51e9a-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="51e9a-142">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="51e9a-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51e9a-143">-SubscriptionId</span></span>
<span data-ttu-id="51e9a-144">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="51e9a-144">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e9a-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51e9a-145">-Confirm</span></span>
<span data-ttu-id="51e9a-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51e9a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e9a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e9a-147">-WhatIf</span></span>
<span data-ttu-id="51e9a-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51e9a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e9a-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51e9a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e9a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e9a-150">CommonParameters</span></span>
<span data-ttu-id="51e9a-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51e9a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e9a-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51e9a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e9a-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51e9a-153">INPUTS</span></span>

### <span data-ttu-id="51e9a-154">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="51e9a-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="51e9a-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51e9a-155">OUTPUTS</span></span>

### <span data-ttu-id="51e9a-156">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51e9a-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="51e9a-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51e9a-157">NOTES</span></span>

<span data-ttu-id="51e9a-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="51e9a-158">ALIASES</span></span>

<span data-ttu-id="51e9a-159">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="51e9a-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51e9a-160">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="51e9a-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51e9a-161">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="51e9a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51e9a-162">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="51e9a-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51e9a-163">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="51e9a-164">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="51e9a-165">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="51e9a-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="51e9a-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51e9a-167">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="51e9a-168">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="51e9a-169">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="51e9a-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="51e9a-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="51e9a-171">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="51e9a-172">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="51e9a-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="51e9a-173">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="51e9a-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="51e9a-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51e9a-174">RELATED LINKS</span></span>

