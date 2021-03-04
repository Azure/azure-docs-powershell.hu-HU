---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 2147921826c6f50882345bc68603b0dae8cb26ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926994"
---
# <span data-ttu-id="c4711-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4711-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="c4711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4711-102">SYNOPSIS</span></span>
<span data-ttu-id="c4711-103">Egy meglévő tűzfalszabály frissítése.</span><span class="sxs-lookup"><span data-stu-id="c4711-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="c4711-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4711-104">SYNTAX</span></span>

### <span data-ttu-id="c4711-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4711-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4711-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4711-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4711-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4711-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4711-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c4711-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c4711-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4711-109">DESCRIPTION</span></span>
<span data-ttu-id="c4711-110">Egy meglévő tűzfalszabály frissítése.</span><span class="sxs-lookup"><span data-stu-id="c4711-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="c4711-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4711-111">EXAMPLES</span></span>

### <span data-ttu-id="c4711-112">1. példa: A MySql tűzfalszabály frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="c4711-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="c4711-113">Ez a parancsmag név szerint frissíti a MySql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="c4711-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="c4711-114">2. példa: A MySql tűzfalszabály frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="c4711-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="c4711-115">Ezek a parancsmagok identitás szerint frissítik a MySql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="c4711-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="c4711-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4711-116">PARAMETERS</span></span>

### <span data-ttu-id="c4711-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4711-117">-AsJob</span></span>
<span data-ttu-id="c4711-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="c4711-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c4711-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4711-119">-ClientIPAddress</span></span>
<span data-ttu-id="c4711-120">Az ügyfél a kiszolgáló tűzfalszabályának egyetlen IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4711-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="c4711-121">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4711-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c4711-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4711-122">-DefaultProfile</span></span>
<span data-ttu-id="c4711-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4711-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4711-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4711-124">-EndIPAddress</span></span>
<span data-ttu-id="c4711-125">A kiszolgáló tűzfalszabályának záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c4711-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="c4711-126">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4711-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c4711-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4711-127">-InputObject</span></span>
<span data-ttu-id="c4711-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c4711-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4711-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c4711-129">-Name</span></span>
<span data-ttu-id="c4711-130">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="c4711-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4711-131">-NoWait</span></span>
<span data-ttu-id="c4711-132">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="c4711-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4711-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4711-133">-ResourceGroupName</span></span>
<span data-ttu-id="c4711-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-134">The name of the resource group.</span></span>
<span data-ttu-id="c4711-135">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c4711-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c4711-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4711-136">-ServerName</span></span>
<span data-ttu-id="c4711-137">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-137">The name of the server.</span></span>

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

### <span data-ttu-id="c4711-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4711-138">-StartIPAddress</span></span>
<span data-ttu-id="c4711-139">A kiszolgáló tűzfalszabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c4711-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="c4711-140">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4711-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c4711-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4711-141">-SubscriptionId</span></span>
<span data-ttu-id="c4711-142">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4711-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c4711-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4711-143">-Confirm</span></span>
<span data-ttu-id="c4711-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c4711-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4711-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4711-145">-WhatIf</span></span>
<span data-ttu-id="c4711-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c4711-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4711-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4711-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4711-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4711-148">CommonParameters</span></span>
<span data-ttu-id="c4711-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4711-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4711-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4711-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4711-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4711-151">INPUTS</span></span>

### <span data-ttu-id="c4711-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c4711-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c4711-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4711-153">OUTPUTS</span></span>

### <span data-ttu-id="c4711-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4711-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="c4711-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4711-155">NOTES</span></span>

<span data-ttu-id="c4711-156">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c4711-156">ALIASES</span></span>

<span data-ttu-id="c4711-157">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c4711-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4711-158">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c4711-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4711-159">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4711-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4711-160">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c4711-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4711-161">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c4711-162">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c4711-163">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c4711-164">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c4711-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4711-165">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c4711-166">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c4711-167">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4711-168">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c4711-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4711-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c4711-170">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c4711-171">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4711-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4711-172">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c4711-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c4711-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4711-173">RELATED LINKS</span></span>

