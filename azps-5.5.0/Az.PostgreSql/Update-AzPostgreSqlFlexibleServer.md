---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: f6634f83e89abe4c775779c052ad9ee7b21bea6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151234"
---
# <span data-ttu-id="79712-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="79712-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="79712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79712-102">SYNOPSIS</span></span>
<span data-ttu-id="79712-103">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="79712-103">Updates an existing server.</span></span>
<span data-ttu-id="79712-104">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="79712-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="79712-105">Használjon Update-AzPostSqlFlexibleServerConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="79712-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="79712-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79712-106">SYNTAX</span></span>

### <span data-ttu-id="79712-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79712-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="79712-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="79712-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79712-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79712-109">DESCRIPTION</span></span>
<span data-ttu-id="79712-110">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="79712-110">Updates an existing server.</span></span>
<span data-ttu-id="79712-111">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="79712-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="79712-112">Használjon Update-AzPostgreSqlFlexibleServerConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="79712-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="79712-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79712-113">EXAMPLES</span></span>

### <span data-ttu-id="79712-114">1. példa: A PostgreSql-kiszolgáló frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="79712-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="79712-115">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="79712-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="79712-116">2. példa: A PostgreSql-kiszolgáló frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="79712-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="79712-117">Ez a parancsmag identitás szerint frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="79712-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="79712-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79712-118">PARAMETERS</span></span>

### <span data-ttu-id="79712-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="79712-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="79712-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="79712-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79712-121">-AsJob</span></span>
<span data-ttu-id="79712-122">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="79712-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="79712-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="79712-123">-BackupRetentionDay</span></span>
<span data-ttu-id="79712-124">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="79712-124">Backup retention days for the server.</span></span>
<span data-ttu-id="79712-125">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="79712-125">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79712-126">-DefaultProfile</span></span>
<span data-ttu-id="79712-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79712-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79712-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="79712-128">-HaEnabled</span></span>
<span data-ttu-id="79712-129">A magas elérhetőségű funkció engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="79712-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79712-130">-InputObject</span></span>
<span data-ttu-id="79712-131">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="79712-131">Identity Parameter.</span></span>
<span data-ttu-id="79712-132">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="79712-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="79712-133">-Name</span><span class="sxs-lookup"><span data-stu-id="79712-133">-Name</span></span>
<span data-ttu-id="79712-134">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="79712-134">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79712-135">-NoWait</span></span>
<span data-ttu-id="79712-136">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="79712-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="79712-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="79712-137">-ReplicationRole</span></span>
<span data-ttu-id="79712-138">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="79712-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="79712-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79712-139">-ResourceGroupName</span></span>
<span data-ttu-id="79712-140">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="79712-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="79712-141">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="79712-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="79712-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="79712-142">-Sku</span></span>
<span data-ttu-id="79712-143">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="79712-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="79712-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="79712-144">-SkuTier</span></span>
<span data-ttu-id="79712-145">Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="79712-145">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="79712-146">-SslEnforcement</span></span>
<span data-ttu-id="79712-147">Engedélyezze az ssl kényszerítési funkcióját, vagy ne, amikor a kiszolgálóhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="79712-147">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="79712-148">-StorageAutogrow</span></span>
<span data-ttu-id="79712-149">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="79712-149">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="79712-150">-StorageInMb</span></span>
<span data-ttu-id="79712-151">A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="79712-151">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79712-152">-SubscriptionId</span></span>
<span data-ttu-id="79712-153">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="79712-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="79712-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="79712-154">-Tag</span></span>
<span data-ttu-id="79712-155">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="79712-155">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79712-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79712-156">-Confirm</span></span>
<span data-ttu-id="79712-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79712-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79712-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79712-158">-WhatIf</span></span>
<span data-ttu-id="79712-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79712-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79712-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79712-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79712-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79712-161">CommonParameters</span></span>
<span data-ttu-id="79712-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79712-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79712-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79712-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79712-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79712-164">INPUTS</span></span>

### <span data-ttu-id="79712-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="79712-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="79712-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79712-166">OUTPUTS</span></span>

### <span data-ttu-id="79712-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="79712-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="79712-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79712-168">NOTES</span></span>

<span data-ttu-id="79712-169">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="79712-169">ALIASES</span></span>

<span data-ttu-id="79712-170">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="79712-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="79712-171">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="79712-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="79712-172">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="79712-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="79712-173">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="79712-173">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="79712-174">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="79712-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="79712-175">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="79712-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="79712-176">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="79712-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="79712-177">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="79712-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="79712-178">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="79712-178">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="79712-179">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="79712-179">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="79712-180">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="79712-180">The name is case insensitive.</span></span>
  - <span data-ttu-id="79712-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="79712-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="79712-182">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="79712-182">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="79712-183">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="79712-183">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="79712-184">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="79712-184">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="79712-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79712-185">RELATED LINKS</span></span>

