---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: e45d342f7bb02034b2adf0473e6d4d1eb3c2b370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929945"
---
# <span data-ttu-id="855b3-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="855b3-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="855b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="855b3-102">SYNOPSIS</span></span>
<span data-ttu-id="855b3-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="855b3-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="855b3-104">Használja Update-AzPostgreSqlFlexibleServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="855b3-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="855b3-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="855b3-105">SYNTAX</span></span>

### <span data-ttu-id="855b3-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="855b3-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="855b3-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="855b3-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="855b3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="855b3-108">DESCRIPTION</span></span>
<span data-ttu-id="855b3-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="855b3-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="855b3-110">Használja Update-AzPostgreSqlFlexibleServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="855b3-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="855b3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="855b3-111">EXAMPLES</span></span>

### <span data-ttu-id="855b3-112">1. példa: Updatae megadott PostgreSql-konfiguráció név szerint</span><span class="sxs-lookup"><span data-stu-id="855b3-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="855b3-113">Ez a parancsmag név szerint frissíti a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="855b3-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="855b3-114">1. példa: Az updatae által megadott PostgreSql-konfiguráció identitás szerint</span><span class="sxs-lookup"><span data-stu-id="855b3-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="855b3-115">Ez a parancsmag identitás szerint frissíti a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="855b3-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="855b3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="855b3-116">PARAMETERS</span></span>

### <span data-ttu-id="855b3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="855b3-117">-AsJob</span></span>
<span data-ttu-id="855b3-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="855b3-118">Run the command as a job</span></span>

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

### <span data-ttu-id="855b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="855b3-119">-DefaultProfile</span></span>
<span data-ttu-id="855b3-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="855b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="855b3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="855b3-121">-InputObject</span></span>
<span data-ttu-id="855b3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="855b3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="855b3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="855b3-123">-Name</span></span>
<span data-ttu-id="855b3-124">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="855b3-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="855b3-125">-NoWait</span></span>
<span data-ttu-id="855b3-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="855b3-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="855b3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="855b3-127">-ResourceGroupName</span></span>
<span data-ttu-id="855b3-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-128">The name of the resource group.</span></span>
<span data-ttu-id="855b3-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="855b3-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="855b3-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="855b3-130">-ServerName</span></span>
<span data-ttu-id="855b3-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-131">The name of the server.</span></span>

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

### <span data-ttu-id="855b3-132">-Source</span><span class="sxs-lookup"><span data-stu-id="855b3-132">-Source</span></span>
<span data-ttu-id="855b3-133">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="855b3-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="855b3-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="855b3-134">-SubscriptionId</span></span>
<span data-ttu-id="855b3-135">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="855b3-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="855b3-136">-Érték</span><span class="sxs-lookup"><span data-stu-id="855b3-136">-Value</span></span>
<span data-ttu-id="855b3-137">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="855b3-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="855b3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="855b3-138">-Confirm</span></span>
<span data-ttu-id="855b3-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="855b3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="855b3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="855b3-140">-WhatIf</span></span>
<span data-ttu-id="855b3-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="855b3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="855b3-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="855b3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="855b3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="855b3-143">CommonParameters</span></span>
<span data-ttu-id="855b3-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="855b3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="855b3-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="855b3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="855b3-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="855b3-146">INPUTS</span></span>

### <span data-ttu-id="855b3-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="855b3-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="855b3-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="855b3-148">OUTPUTS</span></span>

### <span data-ttu-id="855b3-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="855b3-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="855b3-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="855b3-150">NOTES</span></span>

<span data-ttu-id="855b3-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="855b3-151">ALIASES</span></span>

<span data-ttu-id="855b3-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="855b3-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="855b3-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="855b3-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="855b3-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="855b3-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="855b3-155">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="855b3-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="855b3-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="855b3-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="855b3-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="855b3-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="855b3-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="855b3-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="855b3-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="855b3-162">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="855b3-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="855b3-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="855b3-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="855b3-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="855b3-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="855b3-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="855b3-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="855b3-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="855b3-167">RELATED LINKS</span></span>

