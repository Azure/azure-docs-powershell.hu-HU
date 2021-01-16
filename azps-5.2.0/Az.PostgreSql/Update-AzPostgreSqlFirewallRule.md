---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331134"
---
# <span data-ttu-id="f1650-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f1650-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="f1650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1650-102">SYNOPSIS</span></span>
<span data-ttu-id="f1650-103">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="f1650-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f1650-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1650-104">SYNTAX</span></span>

### <span data-ttu-id="f1650-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1650-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1650-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1650-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1650-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1650-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1650-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f1650-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f1650-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1650-109">DESCRIPTION</span></span>
<span data-ttu-id="f1650-110">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="f1650-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f1650-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1650-111">EXAMPLES</span></span>

### <span data-ttu-id="f1650-112">1. példa: A PostgreSql tűzfalszabály frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="f1650-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="f1650-113">Ez a parancsmag név szerint frissíti a PostgreSql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="f1650-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="f1650-114">2. példa: A PostgreSql tűzfalszabály frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="f1650-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f1650-115">Ezek a parancsmagok identitás szerint frissítik a PostgreSql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="f1650-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="f1650-116">3. példa: A PostgreSql tűzfalszabály frissítése -ClientIPAddress szerint.</span><span class="sxs-lookup"><span data-stu-id="f1650-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="f1650-117">Ezek a parancsmagok frissítik a PostgreSql tűzfalszabályt a -ClientIPAddress szerint.</span><span class="sxs-lookup"><span data-stu-id="f1650-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="f1650-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1650-118">PARAMETERS</span></span>

### <span data-ttu-id="f1650-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1650-119">-AsJob</span></span>
<span data-ttu-id="f1650-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f1650-120">Run the command as a job</span></span>

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

### <span data-ttu-id="f1650-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1650-121">-ClientIPAddress</span></span>
<span data-ttu-id="f1650-122">Az ügyfél a kiszolgáló tűzfalszabályának egyetlen IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1650-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="f1650-123">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f1650-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f1650-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1650-124">-DefaultProfile</span></span>
<span data-ttu-id="f1650-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1650-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1650-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1650-126">-EndIPAddress</span></span>
<span data-ttu-id="f1650-127">A kiszolgáló tűzfalszabályának záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="f1650-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="f1650-128">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f1650-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f1650-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1650-129">-InputObject</span></span>
<span data-ttu-id="f1650-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f1650-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1650-131">-Name</span><span class="sxs-lookup"><span data-stu-id="f1650-131">-Name</span></span>
<span data-ttu-id="f1650-132">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="f1650-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1650-133">-NoWait</span></span>
<span data-ttu-id="f1650-134">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f1650-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1650-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1650-135">-ResourceGroupName</span></span>
<span data-ttu-id="f1650-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-136">The name of the resource group.</span></span>
<span data-ttu-id="f1650-137">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f1650-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f1650-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1650-138">-ServerName</span></span>
<span data-ttu-id="f1650-139">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-139">The name of the server.</span></span>

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

### <span data-ttu-id="f1650-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1650-140">-StartIPAddress</span></span>
<span data-ttu-id="f1650-141">A kiszolgáló tűzfalszabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="f1650-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="f1650-142">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f1650-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f1650-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1650-143">-SubscriptionId</span></span>
<span data-ttu-id="f1650-144">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1650-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f1650-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1650-145">-Confirm</span></span>
<span data-ttu-id="f1650-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f1650-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1650-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1650-147">-WhatIf</span></span>
<span data-ttu-id="f1650-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f1650-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1650-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1650-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1650-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1650-150">CommonParameters</span></span>
<span data-ttu-id="f1650-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1650-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1650-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1650-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1650-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1650-153">INPUTS</span></span>

### <span data-ttu-id="f1650-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f1650-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f1650-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1650-155">OUTPUTS</span></span>

### <span data-ttu-id="f1650-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f1650-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="f1650-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1650-157">NOTES</span></span>

<span data-ttu-id="f1650-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f1650-158">ALIASES</span></span>

<span data-ttu-id="f1650-159">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f1650-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1650-160">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f1650-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1650-161">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1650-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1650-162">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f1650-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1650-163">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f1650-164">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f1650-165">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f1650-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f1650-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1650-167">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f1650-168">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f1650-169">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f1650-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="f1650-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f1650-171">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f1650-172">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1650-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f1650-173">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f1650-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f1650-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1650-174">RELATED LINKS</span></span>

