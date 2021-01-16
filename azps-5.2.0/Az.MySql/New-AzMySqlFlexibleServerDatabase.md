---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335633"
---
# <span data-ttu-id="6711f-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="6711f-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="6711f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6711f-102">SYNOPSIS</span></span>
<span data-ttu-id="6711f-103">Új adatbázist hoz létre, vagy frissíti a meglévő adatbázist.</span><span class="sxs-lookup"><span data-stu-id="6711f-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="6711f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6711f-104">SYNTAX</span></span>

### <span data-ttu-id="6711f-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6711f-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6711f-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6711f-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6711f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6711f-107">DESCRIPTION</span></span>
<span data-ttu-id="6711f-108">Új adatbázist hoz létre, vagy frissíti a meglévő adatbázist.</span><span class="sxs-lookup"><span data-stu-id="6711f-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="6711f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6711f-109">EXAMPLES</span></span>

### <span data-ttu-id="6711f-110">1. példa: Új MySql-kiszolgálóadatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="6711f-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="6711f-111">Hozzon létre egy adatbázist alapértelmezett beállításokkal.</span><span class="sxs-lookup"><span data-stu-id="6711f-111">Create a database with default settings.</span></span>

## <span data-ttu-id="6711f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6711f-112">PARAMETERS</span></span>

### <span data-ttu-id="6711f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6711f-113">-AsJob</span></span>
<span data-ttu-id="6711f-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="6711f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6711f-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="6711f-115">-Charset</span></span>
<span data-ttu-id="6711f-116">Az adatbázis karakterkészlete.</span><span class="sxs-lookup"><span data-stu-id="6711f-116">The charset of the database.</span></span>

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

### <span data-ttu-id="6711f-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="6711f-117">-Collation</span></span>
<span data-ttu-id="6711f-118">Az adatbázis szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="6711f-118">The collation of the database.</span></span>

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

### <span data-ttu-id="6711f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6711f-119">-DefaultProfile</span></span>
<span data-ttu-id="6711f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6711f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6711f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6711f-121">-InputObject</span></span>
<span data-ttu-id="6711f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6711f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6711f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6711f-123">-Name</span></span>
<span data-ttu-id="6711f-124">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6711f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6711f-125">-NoWait</span></span>
<span data-ttu-id="6711f-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="6711f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6711f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6711f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6711f-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-128">The name of the resource group.</span></span>
<span data-ttu-id="6711f-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6711f-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6711f-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6711f-130">-ServerName</span></span>
<span data-ttu-id="6711f-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-131">The name of the server.</span></span>

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

### <span data-ttu-id="6711f-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6711f-132">-SubscriptionId</span></span>
<span data-ttu-id="6711f-133">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6711f-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6711f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6711f-134">-Confirm</span></span>
<span data-ttu-id="6711f-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6711f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6711f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6711f-136">-WhatIf</span></span>
<span data-ttu-id="6711f-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6711f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6711f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6711f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6711f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6711f-139">CommonParameters</span></span>
<span data-ttu-id="6711f-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6711f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6711f-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6711f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6711f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6711f-142">INPUTS</span></span>

### <span data-ttu-id="6711f-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6711f-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="6711f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6711f-144">OUTPUTS</span></span>

### <span data-ttu-id="6711f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="6711f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="6711f-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6711f-146">NOTES</span></span>

<span data-ttu-id="6711f-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6711f-147">ALIASES</span></span>

<span data-ttu-id="6711f-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6711f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6711f-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6711f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6711f-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6711f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6711f-151">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6711f-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6711f-152">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6711f-153">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6711f-154">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6711f-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6711f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6711f-156">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="6711f-157">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6711f-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6711f-159">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6711f-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="6711f-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6711f-161">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6711f-162">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6711f-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6711f-163">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6711f-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6711f-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6711f-164">RELATED LINKS</span></span>

