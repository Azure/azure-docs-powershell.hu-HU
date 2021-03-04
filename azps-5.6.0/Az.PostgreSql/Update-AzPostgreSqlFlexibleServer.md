---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 65004c35ffa9c4cb227845787c91219a319789fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929946"
---
# <span data-ttu-id="efa34-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="efa34-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="efa34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa34-102">SYNOPSIS</span></span>
<span data-ttu-id="efa34-103">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="efa34-103">Updates an existing server.</span></span>
<span data-ttu-id="efa34-104">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="efa34-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="efa34-105">Használjon Update-AzPostSqlFlexibleServerConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="efa34-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="efa34-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efa34-106">SYNTAX</span></span>

### <span data-ttu-id="efa34-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efa34-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efa34-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="efa34-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efa34-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efa34-109">DESCRIPTION</span></span>
<span data-ttu-id="efa34-110">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="efa34-110">Updates an existing server.</span></span>
<span data-ttu-id="efa34-111">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="efa34-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="efa34-112">Használjon Update-AzPostgreSqlFlexibleServerConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="efa34-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="efa34-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efa34-113">EXAMPLES</span></span>

### <span data-ttu-id="efa34-114">1. példa: A PostgreSql-kiszolgáló frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="efa34-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="efa34-115">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="efa34-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="efa34-116">2. példa: A PostgreSql-kiszolgáló frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="efa34-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="efa34-117">Ez a parancsmag identitás szerint frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="efa34-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="efa34-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efa34-118">PARAMETERS</span></span>

### <span data-ttu-id="efa34-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="efa34-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="efa34-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="efa34-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="efa34-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efa34-121">-AsJob</span></span>
<span data-ttu-id="efa34-122">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="efa34-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="efa34-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="efa34-123">-BackupRetentionDay</span></span>
<span data-ttu-id="efa34-124">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="efa34-124">Backup retention days for the server.</span></span>
<span data-ttu-id="efa34-125">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="efa34-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="efa34-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa34-126">-DefaultProfile</span></span>
<span data-ttu-id="efa34-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efa34-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa34-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="efa34-128">-HaEnabled</span></span>
<span data-ttu-id="efa34-129">A magas elérhetőségű funkció engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="efa34-129">Enable or disable high availability feature.</span></span>

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

### <span data-ttu-id="efa34-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa34-130">-InputObject</span></span>
<span data-ttu-id="efa34-131">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="efa34-131">Identity Parameter.</span></span>
<span data-ttu-id="efa34-132">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="efa34-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="efa34-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="efa34-133">-MaintenanceWindow</span></span>
<span data-ttu-id="efa34-134">Karbantartásra kijelölt időtartam (UTC).</span><span class="sxs-lookup"><span data-stu-id="efa34-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="efa34-135">Példák: "Nap:23:30" az ütemezéshez vasárnap, 11:30 UTC.</span><span class="sxs-lookup"><span data-stu-id="efa34-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="efa34-136">Vissza az alapértelmezett bérletre a "Letiltva" beállításban</span><span class="sxs-lookup"><span data-stu-id="efa34-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="efa34-137">-Name</span><span class="sxs-lookup"><span data-stu-id="efa34-137">-Name</span></span>
<span data-ttu-id="efa34-138">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-138">The name of the server.</span></span>

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

### <span data-ttu-id="efa34-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="efa34-139">-NoWait</span></span>
<span data-ttu-id="efa34-140">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="efa34-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="efa34-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="efa34-141">-ReplicationRole</span></span>
<span data-ttu-id="efa34-142">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="efa34-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="efa34-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa34-143">-ResourceGroupName</span></span>
<span data-ttu-id="efa34-144">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="efa34-145">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="efa34-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="efa34-146">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="efa34-146">-Sku</span></span>
<span data-ttu-id="efa34-147">A termékváltozat neve, például Burstable_B1ms, Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="efa34-147">The name of the sku, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="efa34-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="efa34-148">-SkuTier</span></span>
<span data-ttu-id="efa34-149">Az adott termékváltozat rétege.</span><span class="sxs-lookup"><span data-stu-id="efa34-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="efa34-150">Elfogadott értékek: Sorozatos, GeneralPurpose, Memória optimalizálva.</span><span class="sxs-lookup"><span data-stu-id="efa34-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="efa34-151">Alapérték: Törhető.</span><span class="sxs-lookup"><span data-stu-id="efa34-151">Default: Burstable.</span></span>

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

### <span data-ttu-id="efa34-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="efa34-152">-SslEnforcement</span></span>
<span data-ttu-id="efa34-153">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="efa34-153">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="efa34-154">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="efa34-154">-StorageAutogrow</span></span>
<span data-ttu-id="efa34-155">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="efa34-155">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="efa34-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="efa34-156">-StorageInMb</span></span>
<span data-ttu-id="efa34-157">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="efa34-157">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="efa34-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efa34-158">-SubscriptionId</span></span>
<span data-ttu-id="efa34-159">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="efa34-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="efa34-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="efa34-160">-Tag</span></span>
<span data-ttu-id="efa34-161">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="efa34-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="efa34-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efa34-162">-Confirm</span></span>
<span data-ttu-id="efa34-163">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efa34-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa34-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa34-164">-WhatIf</span></span>
<span data-ttu-id="efa34-165">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efa34-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa34-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efa34-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa34-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa34-167">CommonParameters</span></span>
<span data-ttu-id="efa34-168">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa34-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa34-169">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efa34-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa34-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efa34-170">INPUTS</span></span>

### <span data-ttu-id="efa34-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="efa34-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="efa34-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa34-172">OUTPUTS</span></span>

### <span data-ttu-id="efa34-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="efa34-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="efa34-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efa34-174">NOTES</span></span>

<span data-ttu-id="efa34-175">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="efa34-175">ALIASES</span></span>

<span data-ttu-id="efa34-176">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="efa34-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efa34-177">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="efa34-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efa34-178">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efa34-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efa34-179">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="efa34-179">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="efa34-180">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="efa34-181">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="efa34-182">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="efa34-183">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="efa34-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efa34-184">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="efa34-185">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="efa34-186">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="efa34-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="efa34-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="efa34-188">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="efa34-189">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="efa34-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="efa34-190">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="efa34-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="efa34-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efa34-191">RELATED LINKS</span></span>

