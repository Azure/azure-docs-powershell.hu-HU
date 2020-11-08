---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024686"
---
# <span data-ttu-id="3068c-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3068c-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="3068c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3068c-102">SYNOPSIS</span></span>
<span data-ttu-id="3068c-103">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="3068c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3068c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3068c-104">SYNTAX</span></span>

### <span data-ttu-id="3068c-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3068c-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3068c-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3068c-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3068c-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3068c-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3068c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3068c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3068c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3068c-109">DESCRIPTION</span></span>
<span data-ttu-id="3068c-110">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="3068c-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3068c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3068c-111">EXAMPLES</span></span>

### <span data-ttu-id="3068c-112">Példa 1: a MySql tűzfal szabályának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="3068c-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="3068c-113">Ez a parancsmag a MySql tűzfal szabályait név szerint frissíti.</span><span class="sxs-lookup"><span data-stu-id="3068c-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="3068c-114">2. példa: a MySql tűzfal szabályának frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="3068c-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="3068c-115">Ezek a parancsmagok a MySql-tűzfal szabályait identitás szerint frissítik.</span><span class="sxs-lookup"><span data-stu-id="3068c-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="3068c-116">3. példa: frissítse a MySql Firewall Rule by-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3068c-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="3068c-117">Ezek a parancsmagok frissítik a MySql Firewall Rule by-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3068c-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="3068c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3068c-118">PARAMETERS</span></span>

### <span data-ttu-id="3068c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3068c-119">-AsJob</span></span>
<span data-ttu-id="3068c-120">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="3068c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3068c-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3068c-121">-ClientIPAddress</span></span>
<span data-ttu-id="3068c-122">Ügyfél: a kiszolgálói tűzfalszabályok egyetlen IP-címe van megadva.</span><span class="sxs-lookup"><span data-stu-id="3068c-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="3068c-123">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3068c-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3068c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3068c-124">-DefaultProfile</span></span>
<span data-ttu-id="3068c-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3068c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3068c-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="3068c-126">-EndIPAddress</span></span>
<span data-ttu-id="3068c-127">A kiszolgáló tűzfal-szabályának End IP-címe.</span><span class="sxs-lookup"><span data-stu-id="3068c-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="3068c-128">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3068c-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3068c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3068c-129">-InputObject</span></span>
<span data-ttu-id="3068c-130">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3068c-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3068c-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3068c-131">-Name</span></span>
<span data-ttu-id="3068c-132">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="3068c-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="3068c-133">-NoWait</span></span>
<span data-ttu-id="3068c-134">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="3068c-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3068c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3068c-135">-ResourceGroupName</span></span>
<span data-ttu-id="3068c-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-136">The name of the resource group.</span></span>
<span data-ttu-id="3068c-137">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="3068c-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3068c-138">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3068c-138">-ServerName</span></span>
<span data-ttu-id="3068c-139">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-139">The name of the server.</span></span>

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

### <span data-ttu-id="3068c-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="3068c-140">-StartIPAddress</span></span>
<span data-ttu-id="3068c-141">A kiszolgáló tűzfal-szabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="3068c-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="3068c-142">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3068c-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3068c-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3068c-143">-SubscriptionId</span></span>
<span data-ttu-id="3068c-144">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3068c-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3068c-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3068c-145">-Confirm</span></span>
<span data-ttu-id="3068c-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3068c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3068c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3068c-147">-WhatIf</span></span>
<span data-ttu-id="3068c-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3068c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3068c-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3068c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3068c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3068c-150">CommonParameters</span></span>
<span data-ttu-id="3068c-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3068c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3068c-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3068c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3068c-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3068c-153">INPUTS</span></span>

### <span data-ttu-id="3068c-154">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3068c-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="3068c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3068c-155">OUTPUTS</span></span>

### <span data-ttu-id="3068c-156">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3068c-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="3068c-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3068c-157">NOTES</span></span>

<span data-ttu-id="3068c-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3068c-158">ALIASES</span></span>

<span data-ttu-id="3068c-159">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3068c-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3068c-160">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3068c-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3068c-161">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3068c-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3068c-162">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3068c-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3068c-163">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3068c-164">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3068c-165">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3068c-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3068c-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3068c-167">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3068c-168">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3068c-169">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="3068c-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="3068c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3068c-171">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3068c-172">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3068c-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3068c-173">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3068c-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3068c-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3068c-174">RELATED LINKS</span></span>

