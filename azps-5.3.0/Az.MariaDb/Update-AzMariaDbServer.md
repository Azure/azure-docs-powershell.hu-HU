---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467622"
---
# <span data-ttu-id="81cf9-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="81cf9-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="81cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="81cf9-103">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="81cf9-103">Updates an existing server.</span></span>
<span data-ttu-id="81cf9-104">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="81cf9-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="81cf9-105">Használjon Update-AzMariaDbConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="81cf9-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="81cf9-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81cf9-106">SYNTAX</span></span>

### <span data-ttu-id="81cf9-107">ServerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81cf9-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="81cf9-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="81cf9-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81cf9-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81cf9-109">DESCRIPTION</span></span>
<span data-ttu-id="81cf9-110">Egy meglévő kiszolgáló frissítése.</span><span class="sxs-lookup"><span data-stu-id="81cf9-110">Updates an existing server.</span></span>
<span data-ttu-id="81cf9-111">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="81cf9-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="81cf9-112">Használjon Update-AzMariaDbConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="81cf9-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="81cf9-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81cf9-113">EXAMPLES</span></span>

### <span data-ttu-id="81cf9-114">1. példa: A MariaDB frissítése</span><span class="sxs-lookup"><span data-stu-id="81cf9-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="81cf9-115">Ez a parancs frissíti a MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="81cf9-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="81cf9-116">2. példa: A MariadB frissítése</span><span class="sxs-lookup"><span data-stu-id="81cf9-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="81cf9-117">Ez a parancs frissíti a MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="81cf9-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="81cf9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81cf9-118">PARAMETERS</span></span>

### <span data-ttu-id="81cf9-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="81cf9-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="81cf9-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="81cf9-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="81cf9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81cf9-121">-AsJob</span></span>
<span data-ttu-id="81cf9-122">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="81cf9-122">Run the command as a job</span></span>

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

### <span data-ttu-id="81cf9-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="81cf9-123">-BackupRetentionDay</span></span>
<span data-ttu-id="81cf9-124">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="81cf9-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="81cf9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cf9-125">-DefaultProfile</span></span>
<span data-ttu-id="81cf9-126">régió DefaultParameters Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81cf9-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81cf9-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="81cf9-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="81cf9-128">Engedélyezze a georedundáns helymeghatározást, vagy ne engedélyezze a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="81cf9-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cf9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81cf9-129">-InputObject</span></span>
<span data-ttu-id="81cf9-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="81cf9-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81cf9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="81cf9-131">-Name</span></span>
<span data-ttu-id="81cf9-132">MariaDB-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="81cf9-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cf9-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="81cf9-133">-NoWait</span></span>
<span data-ttu-id="81cf9-134">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="81cf9-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="81cf9-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="81cf9-135">-ReplicationRole</span></span>
<span data-ttu-id="81cf9-136">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="81cf9-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="81cf9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cf9-137">-ResourceGroupName</span></span>
<span data-ttu-id="81cf9-138">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cf9-139">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="81cf9-139">-Sku</span></span>
<span data-ttu-id="81cf9-140">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="81cf9-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="81cf9-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="81cf9-141">-SslEnforcement</span></span>
<span data-ttu-id="81cf9-142">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="81cf9-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cf9-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="81cf9-143">-StorageAutogrow</span></span>
<span data-ttu-id="81cf9-144">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="81cf9-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cf9-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="81cf9-145">-StorageInMb</span></span>
<span data-ttu-id="81cf9-146">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="81cf9-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="81cf9-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81cf9-147">-SubscriptionId</span></span>
<span data-ttu-id="81cf9-148">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része</span><span class="sxs-lookup"><span data-stu-id="81cf9-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cf9-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="81cf9-149">-Tag</span></span>
<span data-ttu-id="81cf9-150">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="81cf9-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="81cf9-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81cf9-151">-Confirm</span></span>
<span data-ttu-id="81cf9-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="81cf9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81cf9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cf9-153">-WhatIf</span></span>
<span data-ttu-id="81cf9-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="81cf9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81cf9-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81cf9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81cf9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cf9-156">CommonParameters</span></span>
<span data-ttu-id="81cf9-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81cf9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cf9-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81cf9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cf9-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81cf9-159">INPUTS</span></span>

### <span data-ttu-id="81cf9-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="81cf9-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="81cf9-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81cf9-161">OUTPUTS</span></span>

### <span data-ttu-id="81cf9-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="81cf9-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="81cf9-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81cf9-163">NOTES</span></span>

<span data-ttu-id="81cf9-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="81cf9-164">ALIASES</span></span>

<span data-ttu-id="81cf9-165">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="81cf9-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81cf9-166">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="81cf9-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81cf9-167">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81cf9-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81cf9-168">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="81cf9-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81cf9-169">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="81cf9-170">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="81cf9-171">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="81cf9-172">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="81cf9-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81cf9-173">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="81cf9-174">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="81cf9-175">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="81cf9-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="81cf9-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="81cf9-177">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="81cf9-178">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="81cf9-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="81cf9-179">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="81cf9-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="81cf9-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81cf9-180">RELATED LINKS</span></span>

