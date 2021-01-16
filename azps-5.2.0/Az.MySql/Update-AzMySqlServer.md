---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: b205f3d4eb9b1ebce360596714ea2524fb2e3be2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360190"
---
# <span data-ttu-id="a5183-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="a5183-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="a5183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5183-102">SYNOPSIS</span></span>
<span data-ttu-id="a5183-103">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="a5183-103">Updates an existing server.</span></span>
<span data-ttu-id="a5183-104">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="a5183-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="a5183-105">Használjon Update-AzMySqlConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="a5183-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="a5183-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5183-106">SYNTAX</span></span>

### <span data-ttu-id="a5183-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5183-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a5183-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a5183-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5183-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5183-109">DESCRIPTION</span></span>
<span data-ttu-id="a5183-110">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="a5183-110">Updates an existing server.</span></span>
<span data-ttu-id="a5183-111">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="a5183-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="a5183-112">Használjon Update-AzMySqlConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="a5183-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="a5183-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5183-113">EXAMPLES</span></span>

### <span data-ttu-id="a5183-114">1. példa: A MySql-kiszolgáló frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="a5183-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="a5183-115">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="a5183-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="a5183-116">2. példa: A MySql-kiszolgáló frissítése identitás alapján.</span><span class="sxs-lookup"><span data-stu-id="a5183-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="a5183-117">Ez a parancsmag identitás szerint frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="a5183-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="a5183-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5183-118">PARAMETERS</span></span>

### <span data-ttu-id="a5183-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a5183-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a5183-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="a5183-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="a5183-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5183-121">-AsJob</span></span>
<span data-ttu-id="a5183-122">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="a5183-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="a5183-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="a5183-123">-BackupRetentionDay</span></span>
<span data-ttu-id="a5183-124">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="a5183-124">Backup retention days for the server.</span></span>
<span data-ttu-id="a5183-125">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="a5183-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="a5183-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5183-126">-DefaultProfile</span></span>
<span data-ttu-id="a5183-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5183-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5183-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5183-128">-InputObject</span></span>
<span data-ttu-id="a5183-129">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="a5183-129">Identity Parameter.</span></span>
<span data-ttu-id="a5183-130">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="a5183-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5183-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a5183-131">-Name</span></span>
<span data-ttu-id="a5183-132">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-132">The name of the server.</span></span>

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

### <span data-ttu-id="a5183-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5183-133">-NoWait</span></span>
<span data-ttu-id="a5183-134">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="a5183-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a5183-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="a5183-135">-ReplicationRole</span></span>
<span data-ttu-id="a5183-136">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="a5183-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="a5183-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5183-137">-ResourceGroupName</span></span>
<span data-ttu-id="a5183-138">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a5183-139">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="a5183-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a5183-140">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="a5183-140">-Sku</span></span>
<span data-ttu-id="a5183-141">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a5183-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="a5183-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a5183-142">-SkuCapacity</span></span>
<span data-ttu-id="a5183-143">A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="a5183-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="a5183-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="a5183-144">-SkuFamily</span></span>
<span data-ttu-id="a5183-145">A hardver család.</span><span class="sxs-lookup"><span data-stu-id="a5183-145">The family of hardware.</span></span>

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

### <span data-ttu-id="a5183-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a5183-146">-SkuTier</span></span>
<span data-ttu-id="a5183-147">Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="a5183-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="a5183-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="a5183-148">-SslEnforcement</span></span>
<span data-ttu-id="a5183-149">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="a5183-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="a5183-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="a5183-150">-StorageAutogrow</span></span>
<span data-ttu-id="a5183-151">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="a5183-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="a5183-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="a5183-152">-StorageInMb</span></span>
<span data-ttu-id="a5183-153">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="a5183-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="a5183-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5183-154">-SubscriptionId</span></span>
<span data-ttu-id="a5183-155">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="a5183-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a5183-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5183-156">-Tag</span></span>
<span data-ttu-id="a5183-157">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="a5183-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="a5183-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5183-158">-Confirm</span></span>
<span data-ttu-id="a5183-159">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a5183-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5183-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5183-160">-WhatIf</span></span>
<span data-ttu-id="a5183-161">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a5183-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5183-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5183-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5183-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5183-163">CommonParameters</span></span>
<span data-ttu-id="a5183-164">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5183-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5183-165">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5183-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5183-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5183-166">INPUTS</span></span>

### <span data-ttu-id="a5183-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a5183-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a5183-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5183-168">OUTPUTS</span></span>

### <span data-ttu-id="a5183-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a5183-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a5183-170">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5183-170">NOTES</span></span>

<span data-ttu-id="a5183-171">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a5183-171">ALIASES</span></span>

<span data-ttu-id="a5183-172">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a5183-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5183-173">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a5183-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5183-174">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5183-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5183-175">INPUTOBJECT: <IMySqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="a5183-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="a5183-176">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a5183-177">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a5183-178">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a5183-179">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a5183-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5183-180">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-180">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a5183-181">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-181">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a5183-182">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-182">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a5183-183">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a5183-183">The name is case insensitive.</span></span>
  - <span data-ttu-id="a5183-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a5183-185">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-185">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a5183-186">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a5183-186">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a5183-187">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="a5183-187">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a5183-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5183-188">RELATED LINKS</span></span>

