---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 46408fc5cd6f718f26c4f55eb7f8bab56891d8b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926993"
---
# <span data-ttu-id="8ac27-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="8ac27-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="8ac27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ac27-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac27-103">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="8ac27-103">Updates an existing server.</span></span>
<span data-ttu-id="8ac27-104">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="8ac27-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8ac27-105">Használjon Update-AzMySqlConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8ac27-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8ac27-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ac27-106">SYNTAX</span></span>

### <span data-ttu-id="8ac27-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ac27-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ac27-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8ac27-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ac27-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ac27-109">DESCRIPTION</span></span>
<span data-ttu-id="8ac27-110">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="8ac27-110">Updates an existing server.</span></span>
<span data-ttu-id="8ac27-111">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="8ac27-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8ac27-112">Használjon Update-AzMySqlConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8ac27-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8ac27-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ac27-113">EXAMPLES</span></span>

### <span data-ttu-id="8ac27-114">1. példa: A MySql-kiszolgáló frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="8ac27-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8ac27-115">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="8ac27-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="8ac27-116">2. példa: A MySql-kiszolgáló frissítése identitás alapján.</span><span class="sxs-lookup"><span data-stu-id="8ac27-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8ac27-117">Ez a parancsmag identitás szerint frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="8ac27-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="8ac27-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ac27-118">PARAMETERS</span></span>

### <span data-ttu-id="8ac27-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8ac27-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8ac27-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="8ac27-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="8ac27-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ac27-121">-AsJob</span></span>
<span data-ttu-id="8ac27-122">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="8ac27-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="8ac27-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8ac27-123">-BackupRetentionDay</span></span>
<span data-ttu-id="8ac27-124">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="8ac27-124">Backup retention days for the server.</span></span>
<span data-ttu-id="8ac27-125">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="8ac27-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="8ac27-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac27-126">-DefaultProfile</span></span>
<span data-ttu-id="8ac27-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ac27-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac27-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ac27-128">-InputObject</span></span>
<span data-ttu-id="8ac27-129">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="8ac27-129">Identity Parameter.</span></span>
<span data-ttu-id="8ac27-130">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="8ac27-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8ac27-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8ac27-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="8ac27-132">Állítsa be a minimális TLS-verziót a kiszolgálói kapcsolatokhoz, ha engedélyezve van az SSL.</span><span class="sxs-lookup"><span data-stu-id="8ac27-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="8ac27-133">A alapértelmezett érték a TLSEnforcementDisabled.accepted érték: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="8ac27-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac27-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8ac27-134">-Name</span></span>
<span data-ttu-id="8ac27-135">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-135">The name of the server.</span></span>

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

### <span data-ttu-id="8ac27-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8ac27-136">-NoWait</span></span>
<span data-ttu-id="8ac27-137">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="8ac27-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8ac27-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="8ac27-138">-ReplicationRole</span></span>
<span data-ttu-id="8ac27-139">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="8ac27-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="8ac27-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac27-140">-ResourceGroupName</span></span>
<span data-ttu-id="8ac27-141">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8ac27-142">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="8ac27-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8ac27-143">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="8ac27-143">-Sku</span></span>
<span data-ttu-id="8ac27-144">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8ac27-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8ac27-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8ac27-145">-SkuCapacity</span></span>
<span data-ttu-id="8ac27-146">A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="8ac27-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="8ac27-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="8ac27-147">-SkuFamily</span></span>
<span data-ttu-id="8ac27-148">A hardver család.</span><span class="sxs-lookup"><span data-stu-id="8ac27-148">The family of hardware.</span></span>

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

### <span data-ttu-id="8ac27-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8ac27-149">-SkuTier</span></span>
<span data-ttu-id="8ac27-150">Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="8ac27-150">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac27-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8ac27-151">-SslEnforcement</span></span>
<span data-ttu-id="8ac27-152">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="8ac27-152">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac27-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8ac27-153">-StorageAutogrow</span></span>
<span data-ttu-id="8ac27-154">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="8ac27-154">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac27-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8ac27-155">-StorageInMb</span></span>
<span data-ttu-id="8ac27-156">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="8ac27-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8ac27-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ac27-157">-SubscriptionId</span></span>
<span data-ttu-id="8ac27-158">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="8ac27-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8ac27-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ac27-159">-Tag</span></span>
<span data-ttu-id="8ac27-160">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="8ac27-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8ac27-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ac27-161">-Confirm</span></span>
<span data-ttu-id="8ac27-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8ac27-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac27-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac27-163">-WhatIf</span></span>
<span data-ttu-id="8ac27-164">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8ac27-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ac27-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ac27-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac27-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac27-166">CommonParameters</span></span>
<span data-ttu-id="8ac27-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac27-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac27-168">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ac27-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac27-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ac27-169">INPUTS</span></span>

### <span data-ttu-id="8ac27-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8ac27-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8ac27-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ac27-171">OUTPUTS</span></span>

### <span data-ttu-id="8ac27-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="8ac27-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8ac27-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ac27-173">NOTES</span></span>

<span data-ttu-id="8ac27-174">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8ac27-174">ALIASES</span></span>

<span data-ttu-id="8ac27-175">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8ac27-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ac27-176">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="8ac27-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ac27-177">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8ac27-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ac27-178">INPUTOBJECT: <IMySqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="8ac27-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="8ac27-179">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8ac27-180">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8ac27-181">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8ac27-182">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8ac27-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ac27-183">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8ac27-184">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8ac27-185">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8ac27-186">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="8ac27-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="8ac27-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8ac27-188">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8ac27-189">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ac27-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8ac27-190">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="8ac27-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8ac27-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ac27-191">RELATED LINKS</span></span>

