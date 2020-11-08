---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188067"
---
# <span data-ttu-id="da34c-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da34c-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="da34c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da34c-102">SYNOPSIS</span></span>
<span data-ttu-id="da34c-103">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="da34c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="da34c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da34c-104">SYNTAX</span></span>

### <span data-ttu-id="da34c-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da34c-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da34c-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="da34c-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da34c-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da34c-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da34c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="da34c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="da34c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="da34c-109">DESCRIPTION</span></span>
<span data-ttu-id="da34c-110">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="da34c-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="da34c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="da34c-111">EXAMPLES</span></span>

### <span data-ttu-id="da34c-112">1. példa: a PostgreSql-tűzfal szabályának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="da34c-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="da34c-113">Ez a parancsmag a PostgreSql-tűzfal szabályait név szerint frissíti.</span><span class="sxs-lookup"><span data-stu-id="da34c-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="da34c-114">2. példa: a PostgreSql-tűzfal szabályának frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="da34c-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="da34c-115">Ezek a parancsmagok a PostgreSql-tűzfal szabályait identitás szerint frissítik.</span><span class="sxs-lookup"><span data-stu-id="da34c-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="da34c-116">3. példa: a PostgreSql Firewall Rule by-ClientIPAddress frissítése</span><span class="sxs-lookup"><span data-stu-id="da34c-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="da34c-117">Ezek a parancsmagok a PostgreSql tűzfal szabályait frissítik ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="da34c-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="da34c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da34c-118">PARAMETERS</span></span>

### <span data-ttu-id="da34c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da34c-119">-AsJob</span></span>
<span data-ttu-id="da34c-120">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="da34c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="da34c-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="da34c-121">-ClientIPAddress</span></span>
<span data-ttu-id="da34c-122">Ügyfél: a kiszolgálói tűzfalszabályok egyetlen IP-címe van megadva.</span><span class="sxs-lookup"><span data-stu-id="da34c-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="da34c-123">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="da34c-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da34c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da34c-124">-DefaultProfile</span></span>
<span data-ttu-id="da34c-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da34c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da34c-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="da34c-126">-EndIPAddress</span></span>
<span data-ttu-id="da34c-127">A kiszolgáló tűzfal-szabályának End IP-címe.</span><span class="sxs-lookup"><span data-stu-id="da34c-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="da34c-128">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="da34c-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da34c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da34c-129">-InputObject</span></span>
<span data-ttu-id="da34c-130">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da34c-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da34c-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da34c-131">-Name</span></span>
<span data-ttu-id="da34c-132">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="da34c-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="da34c-133">-NoWait</span></span>
<span data-ttu-id="da34c-134">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="da34c-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da34c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da34c-135">-ResourceGroupName</span></span>
<span data-ttu-id="da34c-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-136">The name of the resource group.</span></span>
<span data-ttu-id="da34c-137">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="da34c-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="da34c-138">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="da34c-138">-ServerName</span></span>
<span data-ttu-id="da34c-139">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-139">The name of the server.</span></span>

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

### <span data-ttu-id="da34c-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="da34c-140">-StartIPAddress</span></span>
<span data-ttu-id="da34c-141">A kiszolgáló tűzfal-szabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="da34c-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="da34c-142">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="da34c-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da34c-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da34c-143">-SubscriptionId</span></span>
<span data-ttu-id="da34c-144">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da34c-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="da34c-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da34c-145">-Confirm</span></span>
<span data-ttu-id="da34c-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da34c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da34c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da34c-147">-WhatIf</span></span>
<span data-ttu-id="da34c-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da34c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da34c-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da34c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da34c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da34c-150">CommonParameters</span></span>
<span data-ttu-id="da34c-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da34c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da34c-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da34c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da34c-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da34c-153">INPUTS</span></span>

### <span data-ttu-id="da34c-154">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="da34c-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="da34c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da34c-155">OUTPUTS</span></span>

### <span data-ttu-id="da34c-156">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da34c-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="da34c-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da34c-157">NOTES</span></span>

<span data-ttu-id="da34c-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="da34c-158">ALIASES</span></span>

<span data-ttu-id="da34c-159">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="da34c-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da34c-160">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="da34c-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da34c-161">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="da34c-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da34c-162">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="da34c-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da34c-163">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="da34c-164">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="da34c-165">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="da34c-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="da34c-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da34c-167">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="da34c-168">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="da34c-169">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="da34c-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="da34c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="da34c-171">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="da34c-172">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da34c-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="da34c-173">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="da34c-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="da34c-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da34c-174">RELATED LINKS</span></span>

