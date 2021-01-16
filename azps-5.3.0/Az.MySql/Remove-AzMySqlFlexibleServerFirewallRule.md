---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: f7e874114436d60bdba3fa3fe2d8628a97925c09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466279"
---
# <span data-ttu-id="fe131-101">Remove-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fe131-101">Remove-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="fe131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe131-102">SYNOPSIS</span></span>
<span data-ttu-id="fe131-103">Egy tűzfalszabály törlése.</span><span class="sxs-lookup"><span data-stu-id="fe131-103">Deletes a firewall rule.</span></span>

## <span data-ttu-id="fe131-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe131-104">SYNTAX</span></span>

### <span data-ttu-id="fe131-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe131-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fe131-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fe131-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe131-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe131-107">DESCRIPTION</span></span>
<span data-ttu-id="fe131-108">Egy tűzfalszabály törlése.</span><span class="sxs-lookup"><span data-stu-id="fe131-108">Deletes a firewall rule.</span></span>

## <span data-ttu-id="fe131-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe131-109">EXAMPLES</span></span>

### <span data-ttu-id="fe131-110">1. példa: A MySql tűzfalszabály eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="fe131-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerFirewallRule -Name firewall-rule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="fe131-111">Ez a parancsmag név szerint eltávolítja a MySql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="fe131-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="fe131-112">2. példa: A MySql tűzfalszabály eltávolítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="fe131-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/firewall-rule-test"
PS C:\> Remove-AzMySqlFlexibleServerFirewallRule -InputObject $ID
 
```

<span data-ttu-id="fe131-113">Ezek a parancsmagok identitás szerint eltávolítják a MySql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="fe131-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="fe131-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe131-114">PARAMETERS</span></span>

### <span data-ttu-id="fe131-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe131-115">-AsJob</span></span>
<span data-ttu-id="fe131-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="fe131-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fe131-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe131-117">-DefaultProfile</span></span>
<span data-ttu-id="fe131-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe131-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe131-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe131-119">-InputObject</span></span>
<span data-ttu-id="fe131-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fe131-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe131-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fe131-121">-Name</span></span>
<span data-ttu-id="fe131-122">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe131-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fe131-123">-NoWait</span></span>
<span data-ttu-id="fe131-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="fe131-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fe131-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe131-125">-PassThru</span></span>
<span data-ttu-id="fe131-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="fe131-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fe131-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe131-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe131-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-128">The name of the resource group.</span></span>
<span data-ttu-id="fe131-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fe131-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe131-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe131-130">-ServerName</span></span>
<span data-ttu-id="fe131-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe131-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe131-132">-SubscriptionId</span></span>
<span data-ttu-id="fe131-133">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fe131-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe131-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe131-134">-Confirm</span></span>
<span data-ttu-id="fe131-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fe131-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe131-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe131-136">-WhatIf</span></span>
<span data-ttu-id="fe131-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fe131-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe131-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe131-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe131-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe131-139">CommonParameters</span></span>
<span data-ttu-id="fe131-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe131-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe131-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe131-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe131-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe131-142">INPUTS</span></span>

### <span data-ttu-id="fe131-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fe131-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="fe131-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe131-144">OUTPUTS</span></span>

### <span data-ttu-id="fe131-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe131-145">System.Boolean</span></span>

## <span data-ttu-id="fe131-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe131-146">NOTES</span></span>

<span data-ttu-id="fe131-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fe131-147">ALIASES</span></span>

<span data-ttu-id="fe131-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fe131-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe131-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="fe131-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe131-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe131-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe131-151">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fe131-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fe131-152">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fe131-153">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fe131-154">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fe131-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fe131-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fe131-156">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="fe131-157">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fe131-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fe131-159">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fe131-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="fe131-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fe131-161">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fe131-162">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fe131-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fe131-163">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fe131-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fe131-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe131-164">RELATED LINKS</span></span>

