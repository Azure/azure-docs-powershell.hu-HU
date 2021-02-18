---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: fe6ef1a5193119c4778d18c39a7ecff98354cf89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206246"
---
# <span data-ttu-id="ba26e-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ba26e-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="ba26e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba26e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba26e-103">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="ba26e-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ba26e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba26e-104">SYNTAX</span></span>

### <span data-ttu-id="ba26e-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba26e-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba26e-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ba26e-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba26e-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba26e-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba26e-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ba26e-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ba26e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba26e-109">DESCRIPTION</span></span>
<span data-ttu-id="ba26e-110">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="ba26e-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ba26e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba26e-111">EXAMPLES</span></span>

### <span data-ttu-id="ba26e-112">1. példa: A PostgreSql tűzfalszabály frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="ba26e-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="ba26e-113">Ez a parancsmag név szerint frissíti a PostgreSql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="ba26e-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="ba26e-114">2. példa: A PostgreSql tűzfalszabály frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="ba26e-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="ba26e-115">Ezek a parancsmagok identitás szerint frissítik a PostgreSql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="ba26e-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="ba26e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba26e-116">PARAMETERS</span></span>

### <span data-ttu-id="ba26e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba26e-117">-AsJob</span></span>
<span data-ttu-id="ba26e-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="ba26e-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ba26e-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ba26e-119">-ClientIPAddress</span></span>
<span data-ttu-id="ba26e-120">Az ügyfél a kiszolgáló tűzfalszabályának egyetlen IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba26e-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="ba26e-121">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ba26e-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="ba26e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba26e-122">-DefaultProfile</span></span>
<span data-ttu-id="ba26e-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba26e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba26e-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="ba26e-124">-EndIPAddress</span></span>
<span data-ttu-id="ba26e-125">A kiszolgáló tűzfalszabályának záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="ba26e-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="ba26e-126">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ba26e-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="ba26e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba26e-127">-InputObject</span></span>
<span data-ttu-id="ba26e-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ba26e-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba26e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ba26e-129">-Name</span></span>
<span data-ttu-id="ba26e-130">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="ba26e-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba26e-131">-NoWait</span></span>
<span data-ttu-id="ba26e-132">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="ba26e-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba26e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba26e-133">-ResourceGroupName</span></span>
<span data-ttu-id="ba26e-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-134">The name of the resource group.</span></span>
<span data-ttu-id="ba26e-135">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ba26e-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ba26e-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba26e-136">-ServerName</span></span>
<span data-ttu-id="ba26e-137">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-137">The name of the server.</span></span>

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

### <span data-ttu-id="ba26e-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="ba26e-138">-StartIPAddress</span></span>
<span data-ttu-id="ba26e-139">A kiszolgáló tűzfalszabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="ba26e-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="ba26e-140">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ba26e-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="ba26e-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba26e-141">-SubscriptionId</span></span>
<span data-ttu-id="ba26e-142">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba26e-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ba26e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba26e-143">-Confirm</span></span>
<span data-ttu-id="ba26e-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ba26e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba26e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba26e-145">-WhatIf</span></span>
<span data-ttu-id="ba26e-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ba26e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba26e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba26e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba26e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba26e-148">CommonParameters</span></span>
<span data-ttu-id="ba26e-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba26e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba26e-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba26e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba26e-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba26e-151">INPUTS</span></span>

### <span data-ttu-id="ba26e-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ba26e-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ba26e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba26e-153">OUTPUTS</span></span>

### <span data-ttu-id="ba26e-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ba26e-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="ba26e-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba26e-155">NOTES</span></span>

<span data-ttu-id="ba26e-156">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ba26e-156">ALIASES</span></span>

<span data-ttu-id="ba26e-157">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ba26e-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba26e-158">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ba26e-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba26e-159">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba26e-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba26e-160">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ba26e-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba26e-161">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ba26e-162">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ba26e-163">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ba26e-164">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ba26e-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba26e-165">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ba26e-166">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ba26e-167">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ba26e-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="ba26e-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ba26e-169">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ba26e-170">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba26e-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ba26e-171">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ba26e-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ba26e-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba26e-172">RELATED LINKS</span></span>

