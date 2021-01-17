---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468714"
---
# <span data-ttu-id="4b938-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b938-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="4b938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b938-102">SYNOPSIS</span></span>
<span data-ttu-id="4b938-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4b938-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="4b938-104">Használja Update-AzPostgreSqlServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="4b938-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4b938-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b938-105">SYNTAX</span></span>

### <span data-ttu-id="4b938-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b938-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b938-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4b938-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b938-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b938-108">DESCRIPTION</span></span>
<span data-ttu-id="4b938-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4b938-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="4b938-110">Használja Update-AzPostgreSqlServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="4b938-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4b938-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b938-111">EXAMPLES</span></span>

### <span data-ttu-id="4b938-112">1. példa: A PostgreSql-konfiguráció frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="4b938-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="4b938-113">Ez a parancsmag név szerint frissíti a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4b938-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="4b938-114">2. példa: A PostgreSql-konfiguráció frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="4b938-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="4b938-115">Ezek a parancsmagok identitás szerint frissítik a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4b938-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="4b938-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b938-116">PARAMETERS</span></span>

### <span data-ttu-id="4b938-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b938-117">-AsJob</span></span>
<span data-ttu-id="4b938-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="4b938-118">Run the command as a job</span></span>

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

### <span data-ttu-id="4b938-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b938-119">-DefaultProfile</span></span>
<span data-ttu-id="4b938-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b938-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b938-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b938-121">-InputObject</span></span>
<span data-ttu-id="4b938-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4b938-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b938-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4b938-123">-Name</span></span>
<span data-ttu-id="4b938-124">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4b938-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4b938-125">-NoWait</span></span>
<span data-ttu-id="4b938-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="4b938-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4b938-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b938-127">-ResourceGroupName</span></span>
<span data-ttu-id="4b938-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-128">The name of the resource group.</span></span>
<span data-ttu-id="4b938-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4b938-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4b938-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4b938-130">-ServerName</span></span>
<span data-ttu-id="4b938-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-131">The name of the server.</span></span>

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

### <span data-ttu-id="4b938-132">-Source</span><span class="sxs-lookup"><span data-stu-id="4b938-132">-Source</span></span>
<span data-ttu-id="4b938-133">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="4b938-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="4b938-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b938-134">-SubscriptionId</span></span>
<span data-ttu-id="4b938-135">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4b938-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4b938-136">-Érték</span><span class="sxs-lookup"><span data-stu-id="4b938-136">-Value</span></span>
<span data-ttu-id="4b938-137">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="4b938-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="4b938-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b938-138">-Confirm</span></span>
<span data-ttu-id="4b938-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4b938-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b938-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b938-140">-WhatIf</span></span>
<span data-ttu-id="4b938-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4b938-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b938-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b938-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b938-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b938-143">CommonParameters</span></span>
<span data-ttu-id="4b938-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b938-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b938-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b938-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b938-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b938-146">INPUTS</span></span>

### <span data-ttu-id="4b938-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4b938-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="4b938-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b938-148">OUTPUTS</span></span>

### <span data-ttu-id="4b938-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b938-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="4b938-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b938-150">NOTES</span></span>

<span data-ttu-id="4b938-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4b938-151">ALIASES</span></span>

<span data-ttu-id="4b938-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4b938-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b938-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4b938-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b938-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b938-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b938-155">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4b938-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b938-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4b938-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4b938-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4b938-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4b938-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b938-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4b938-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4b938-162">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4b938-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="4b938-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4b938-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4b938-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4b938-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4b938-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="4b938-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4b938-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b938-167">RELATED LINKS</span></span>

