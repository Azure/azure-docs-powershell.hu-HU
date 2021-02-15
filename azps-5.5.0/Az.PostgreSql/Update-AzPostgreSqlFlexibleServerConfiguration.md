---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 82945caa08fb102c0ef5a05e95586f9c66d3d4a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151219"
---
# <span data-ttu-id="e13fd-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e13fd-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="e13fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e13fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e13fd-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e13fd-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="e13fd-104">Használja Update-AzPostgreSqlFlexibleServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="e13fd-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e13fd-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e13fd-105">SYNTAX</span></span>

### <span data-ttu-id="e13fd-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e13fd-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e13fd-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e13fd-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e13fd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e13fd-108">DESCRIPTION</span></span>
<span data-ttu-id="e13fd-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e13fd-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="e13fd-110">Használja Update-AzPostgreSqlFlexibleServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="e13fd-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e13fd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e13fd-111">EXAMPLES</span></span>

### <span data-ttu-id="e13fd-112">1. példa: Updatae megadott PostgreSql-konfiguráció név szerint</span><span class="sxs-lookup"><span data-stu-id="e13fd-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="e13fd-113">Ez a parancsmag név szerint frissíti a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e13fd-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="e13fd-114">1. példa: Az updatae által megadott PostgreSql-konfiguráció identitás szerint</span><span class="sxs-lookup"><span data-stu-id="e13fd-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="e13fd-115">Ez a parancsmag identitás szerint frissíti a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e13fd-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="e13fd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e13fd-116">PARAMETERS</span></span>

### <span data-ttu-id="e13fd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e13fd-117">-AsJob</span></span>
<span data-ttu-id="e13fd-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="e13fd-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e13fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13fd-119">-DefaultProfile</span></span>
<span data-ttu-id="e13fd-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e13fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e13fd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e13fd-121">-InputObject</span></span>
<span data-ttu-id="e13fd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e13fd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e13fd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e13fd-123">-Name</span></span>
<span data-ttu-id="e13fd-124">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e13fd-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e13fd-125">-NoWait</span></span>
<span data-ttu-id="e13fd-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="e13fd-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e13fd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e13fd-127">-ResourceGroupName</span></span>
<span data-ttu-id="e13fd-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-128">The name of the resource group.</span></span>
<span data-ttu-id="e13fd-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e13fd-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e13fd-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e13fd-130">-ServerName</span></span>
<span data-ttu-id="e13fd-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-131">The name of the server.</span></span>

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

### <span data-ttu-id="e13fd-132">-Source</span><span class="sxs-lookup"><span data-stu-id="e13fd-132">-Source</span></span>
<span data-ttu-id="e13fd-133">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="e13fd-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="e13fd-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e13fd-134">-SubscriptionId</span></span>
<span data-ttu-id="e13fd-135">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e13fd-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e13fd-136">-Érték</span><span class="sxs-lookup"><span data-stu-id="e13fd-136">-Value</span></span>
<span data-ttu-id="e13fd-137">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="e13fd-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="e13fd-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e13fd-138">-Confirm</span></span>
<span data-ttu-id="e13fd-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e13fd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e13fd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e13fd-140">-WhatIf</span></span>
<span data-ttu-id="e13fd-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e13fd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e13fd-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e13fd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e13fd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13fd-143">CommonParameters</span></span>
<span data-ttu-id="e13fd-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e13fd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13fd-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e13fd-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13fd-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e13fd-146">INPUTS</span></span>

### <span data-ttu-id="e13fd-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e13fd-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e13fd-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e13fd-148">OUTPUTS</span></span>

### <span data-ttu-id="e13fd-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e13fd-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="e13fd-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e13fd-150">NOTES</span></span>

<span data-ttu-id="e13fd-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e13fd-151">ALIASES</span></span>

<span data-ttu-id="e13fd-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e13fd-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e13fd-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e13fd-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e13fd-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e13fd-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e13fd-155">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e13fd-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e13fd-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e13fd-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e13fd-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e13fd-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e13fd-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e13fd-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e13fd-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e13fd-162">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e13fd-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="e13fd-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e13fd-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e13fd-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e13fd-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e13fd-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="e13fd-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e13fd-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e13fd-167">RELATED LINKS</span></span>

