---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469397"
---
# <span data-ttu-id="7ff60-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ff60-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="7ff60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ff60-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff60-103">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="7ff60-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="7ff60-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ff60-104">SYNTAX</span></span>

### <span data-ttu-id="7ff60-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ff60-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ff60-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7ff60-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ff60-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ff60-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ff60-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7ff60-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ff60-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ff60-109">DESCRIPTION</span></span>
<span data-ttu-id="7ff60-110">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="7ff60-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="7ff60-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ff60-111">EXAMPLES</span></span>

### <span data-ttu-id="7ff60-112">1. példa: A MariaDB tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="7ff60-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="7ff60-113">Ez a parancs frissíti a MariaDB tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="7ff60-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="7ff60-114">2. példa: A MariaDB tűzfalszabály frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="7ff60-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="7ff60-115">A parancsmag identitás szerint frissíti a MariaDB tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="7ff60-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="7ff60-116">3. példa: A MariaDB tűzfalszabály frissítése -ClientIPAddress szerint.</span><span class="sxs-lookup"><span data-stu-id="7ff60-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="7ff60-117">A parancsmag frissíti a MariaDB tűzfalszabályt -ClientIPAddress szerint.</span><span class="sxs-lookup"><span data-stu-id="7ff60-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="7ff60-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ff60-118">PARAMETERS</span></span>

### <span data-ttu-id="7ff60-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ff60-119">-AsJob</span></span>
<span data-ttu-id="7ff60-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7ff60-120">Run the command as a job</span></span>

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

### <span data-ttu-id="7ff60-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7ff60-121">-ClientIPAddress</span></span>
<span data-ttu-id="7ff60-122">Az ügyfél a kiszolgáló tűzfalszabályának egyetlen IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ff60-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="7ff60-123">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7ff60-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7ff60-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff60-124">-DefaultProfile</span></span>
<span data-ttu-id="7ff60-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ff60-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ff60-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="7ff60-126">-EndIPAddress</span></span>
<span data-ttu-id="7ff60-127">A kiszolgáló tűzfalszabályának záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="7ff60-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="7ff60-128">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7ff60-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7ff60-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ff60-129">-InputObject</span></span>
<span data-ttu-id="7ff60-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7ff60-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ff60-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7ff60-131">-Name</span></span>
<span data-ttu-id="7ff60-132">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="7ff60-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7ff60-133">-NoWait</span></span>
<span data-ttu-id="7ff60-134">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7ff60-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7ff60-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff60-135">-ResourceGroupName</span></span>
<span data-ttu-id="7ff60-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7ff60-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="7ff60-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7ff60-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7ff60-138">-ServerName</span></span>
<span data-ttu-id="7ff60-139">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-139">The name of the server.</span></span>

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

### <span data-ttu-id="7ff60-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="7ff60-140">-StartIPAddress</span></span>
<span data-ttu-id="7ff60-141">A kiszolgáló tűzfalszabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="7ff60-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="7ff60-142">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7ff60-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7ff60-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ff60-143">-SubscriptionId</span></span>
<span data-ttu-id="7ff60-144">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="7ff60-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="7ff60-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ff60-145">-Confirm</span></span>
<span data-ttu-id="7ff60-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ff60-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ff60-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff60-147">-WhatIf</span></span>
<span data-ttu-id="7ff60-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ff60-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ff60-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ff60-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ff60-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff60-150">CommonParameters</span></span>
<span data-ttu-id="7ff60-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff60-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff60-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ff60-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff60-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ff60-153">INPUTS</span></span>

### <span data-ttu-id="7ff60-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="7ff60-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="7ff60-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ff60-155">OUTPUTS</span></span>

### <span data-ttu-id="7ff60-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ff60-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="7ff60-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ff60-157">NOTES</span></span>

<span data-ttu-id="7ff60-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7ff60-158">ALIASES</span></span>

<span data-ttu-id="7ff60-159">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7ff60-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ff60-160">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7ff60-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ff60-161">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ff60-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ff60-162">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7ff60-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ff60-163">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7ff60-164">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7ff60-165">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7ff60-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7ff60-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ff60-167">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7ff60-168">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7ff60-169">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="7ff60-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7ff60-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7ff60-171">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7ff60-172">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="7ff60-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="7ff60-173">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="7ff60-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7ff60-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ff60-174">RELATED LINKS</span></span>

