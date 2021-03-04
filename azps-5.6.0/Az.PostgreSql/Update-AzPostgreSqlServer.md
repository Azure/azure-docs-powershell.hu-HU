---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: d6d4480f2a4be2fa10a6e6ea8b69da1de9c61f39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929937"
---
# <span data-ttu-id="aafdc-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="aafdc-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="aafdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aafdc-102">SYNOPSIS</span></span>
<span data-ttu-id="aafdc-103">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="aafdc-103">Updates an existing server.</span></span>
<span data-ttu-id="aafdc-104">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="aafdc-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="aafdc-105">Használjon Update-AzPostSqlConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="aafdc-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="aafdc-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aafdc-106">SYNTAX</span></span>

### <span data-ttu-id="aafdc-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aafdc-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aafdc-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aafdc-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aafdc-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aafdc-109">DESCRIPTION</span></span>
<span data-ttu-id="aafdc-110">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="aafdc-110">Updates an existing server.</span></span>
<span data-ttu-id="aafdc-111">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="aafdc-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="aafdc-112">Használjon Update-AzPostSqlConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="aafdc-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="aafdc-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aafdc-113">EXAMPLES</span></span>

### <span data-ttu-id="aafdc-114">1. példa: A PostgreSql-kiszolgáló frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="aafdc-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="aafdc-115">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="aafdc-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="aafdc-116">2. példa: A PostgreSql-kiszolgáló frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="aafdc-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="aafdc-117">Ez a parancsmag identitás szerint frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="aafdc-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="aafdc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aafdc-118">PARAMETERS</span></span>

### <span data-ttu-id="aafdc-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="aafdc-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="aafdc-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="aafdc-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="aafdc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aafdc-121">-AsJob</span></span>
<span data-ttu-id="aafdc-122">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="aafdc-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="aafdc-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="aafdc-123">-BackupRetentionDay</span></span>
<span data-ttu-id="aafdc-124">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="aafdc-124">Backup retention days for the server.</span></span>
<span data-ttu-id="aafdc-125">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="aafdc-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="aafdc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aafdc-126">-DefaultProfile</span></span>
<span data-ttu-id="aafdc-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aafdc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aafdc-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aafdc-128">-InputObject</span></span>
<span data-ttu-id="aafdc-129">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="aafdc-129">Identity Parameter.</span></span>
<span data-ttu-id="aafdc-130">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="aafdc-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aafdc-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="aafdc-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="aafdc-132">Állítsa be a minimális TLS-verziót a kiszolgálói kapcsolatokhoz, ha engedélyezve van az SSL.</span><span class="sxs-lookup"><span data-stu-id="aafdc-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="aafdc-133">A alapértelmezett érték a TLSEnforcementDisabled.accepted érték: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="aafdc-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aafdc-134">-Name</span><span class="sxs-lookup"><span data-stu-id="aafdc-134">-Name</span></span>
<span data-ttu-id="aafdc-135">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-135">The name of the server.</span></span>

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

### <span data-ttu-id="aafdc-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aafdc-136">-NoWait</span></span>
<span data-ttu-id="aafdc-137">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="aafdc-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="aafdc-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="aafdc-138">-ReplicationRole</span></span>
<span data-ttu-id="aafdc-139">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="aafdc-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="aafdc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aafdc-140">-ResourceGroupName</span></span>
<span data-ttu-id="aafdc-141">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aafdc-142">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="aafdc-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aafdc-143">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="aafdc-143">-Sku</span></span>
<span data-ttu-id="aafdc-144">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="aafdc-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="aafdc-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="aafdc-145">-SkuCapacity</span></span>
<span data-ttu-id="aafdc-146">A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="aafdc-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="aafdc-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="aafdc-147">-SkuFamily</span></span>
<span data-ttu-id="aafdc-148">A hardver család.</span><span class="sxs-lookup"><span data-stu-id="aafdc-148">The family of hardware.</span></span>

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

### <span data-ttu-id="aafdc-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="aafdc-149">-SkuTier</span></span>
<span data-ttu-id="aafdc-150">Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="aafdc-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="aafdc-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="aafdc-151">-SslEnforcement</span></span>
<span data-ttu-id="aafdc-152">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="aafdc-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="aafdc-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="aafdc-153">-StorageAutogrow</span></span>
<span data-ttu-id="aafdc-154">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="aafdc-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="aafdc-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="aafdc-155">-StorageInMb</span></span>
<span data-ttu-id="aafdc-156">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="aafdc-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="aafdc-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aafdc-157">-SubscriptionId</span></span>
<span data-ttu-id="aafdc-158">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="aafdc-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="aafdc-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="aafdc-159">-Tag</span></span>
<span data-ttu-id="aafdc-160">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="aafdc-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="aafdc-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aafdc-161">-Confirm</span></span>
<span data-ttu-id="aafdc-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aafdc-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aafdc-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aafdc-163">-WhatIf</span></span>
<span data-ttu-id="aafdc-164">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aafdc-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aafdc-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aafdc-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aafdc-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aafdc-166">CommonParameters</span></span>
<span data-ttu-id="aafdc-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aafdc-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aafdc-168">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aafdc-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aafdc-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aafdc-169">INPUTS</span></span>

### <span data-ttu-id="aafdc-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="aafdc-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="aafdc-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aafdc-171">OUTPUTS</span></span>

### <span data-ttu-id="aafdc-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="aafdc-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="aafdc-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aafdc-173">NOTES</span></span>

<span data-ttu-id="aafdc-174">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aafdc-174">ALIASES</span></span>

<span data-ttu-id="aafdc-175">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="aafdc-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aafdc-176">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="aafdc-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aafdc-177">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aafdc-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aafdc-178">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="aafdc-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="aafdc-179">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="aafdc-180">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="aafdc-181">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="aafdc-182">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="aafdc-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aafdc-183">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="aafdc-184">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aafdc-185">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="aafdc-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="aafdc-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="aafdc-187">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="aafdc-188">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aafdc-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="aafdc-189">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="aafdc-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="aafdc-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aafdc-190">RELATED LINKS</span></span>

