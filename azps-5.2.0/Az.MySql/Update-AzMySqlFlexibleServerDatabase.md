---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360204"
---
# <span data-ttu-id="2994f-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="2994f-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="2994f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2994f-102">SYNOPSIS</span></span>
<span data-ttu-id="2994f-103">Új adatbázist hoz létre, vagy frissíti a meglévő adatbázist.</span><span class="sxs-lookup"><span data-stu-id="2994f-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2994f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2994f-104">SYNTAX</span></span>

### <span data-ttu-id="2994f-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2994f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2994f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2994f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2994f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2994f-107">DESCRIPTION</span></span>
<span data-ttu-id="2994f-108">Új adatbázist hoz létre, vagy frissíti a meglévő adatbázist.</span><span class="sxs-lookup"><span data-stu-id="2994f-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2994f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2994f-109">EXAMPLES</span></span>

### <span data-ttu-id="2994f-110">1. példa: MySql-kiszolgálói adatbázis frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="2994f-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="2994f-111">Adatbázis frissítése erőforrásnév szerint.</span><span class="sxs-lookup"><span data-stu-id="2994f-111">Update a database by resource name.</span></span>

### <span data-ttu-id="2994f-112">2. példa: A MySql-adatbázis frissítése paraméter szerint.</span><span class="sxs-lookup"><span data-stu-id="2994f-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="2994f-113">Adatbázis frissítése paraméter szerint</span><span class="sxs-lookup"><span data-stu-id="2994f-113">Update a database by parameter</span></span>

## <span data-ttu-id="2994f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2994f-114">PARAMETERS</span></span>

### <span data-ttu-id="2994f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2994f-115">-AsJob</span></span>
<span data-ttu-id="2994f-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="2994f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2994f-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="2994f-117">-Charset</span></span>
<span data-ttu-id="2994f-118">Az adatbázis karakterkészlete.</span><span class="sxs-lookup"><span data-stu-id="2994f-118">The charset of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994f-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="2994f-119">-Collation</span></span>
<span data-ttu-id="2994f-120">Az adatbázis szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="2994f-120">The collation of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2994f-121">-DefaultProfile</span></span>
<span data-ttu-id="2994f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2994f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2994f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2994f-123">-InputObject</span></span>
<span data-ttu-id="2994f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2994f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2994f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2994f-125">-Name</span></span>
<span data-ttu-id="2994f-126">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994f-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2994f-127">-NoWait</span></span>
<span data-ttu-id="2994f-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="2994f-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2994f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2994f-129">-ResourceGroupName</span></span>
<span data-ttu-id="2994f-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-130">The name of the resource group.</span></span>
<span data-ttu-id="2994f-131">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="2994f-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994f-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2994f-132">-ServerName</span></span>
<span data-ttu-id="2994f-133">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2994f-134">-SubscriptionId</span></span>
<span data-ttu-id="2994f-135">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2994f-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2994f-136">-Confirm</span></span>
<span data-ttu-id="2994f-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2994f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2994f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2994f-138">-WhatIf</span></span>
<span data-ttu-id="2994f-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2994f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2994f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2994f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2994f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2994f-141">CommonParameters</span></span>
<span data-ttu-id="2994f-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2994f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2994f-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2994f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2994f-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2994f-144">INPUTS</span></span>

### <span data-ttu-id="2994f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2994f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2994f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2994f-146">OUTPUTS</span></span>

### <span data-ttu-id="2994f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="2994f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="2994f-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2994f-148">NOTES</span></span>

<span data-ttu-id="2994f-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2994f-149">ALIASES</span></span>

<span data-ttu-id="2994f-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2994f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2994f-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2994f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2994f-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2994f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2994f-153">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2994f-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2994f-154">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2994f-155">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2994f-156">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2994f-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2994f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2994f-158">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2994f-159">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2994f-160">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2994f-161">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="2994f-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="2994f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2994f-163">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2994f-164">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2994f-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2994f-165">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="2994f-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2994f-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2994f-166">RELATED LINKS</span></span>

