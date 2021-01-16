---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360231"
---
# <span data-ttu-id="c61b8-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="c61b8-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="c61b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c61b8-103">Frissíti a meglévő rugalmas MySQL-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="c61b8-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="c61b8-104">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="c61b8-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c61b8-105">Használjon Update-AzMySqlFlexibleServerConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="c61b8-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c61b8-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c61b8-106">SYNTAX</span></span>

### <span data-ttu-id="c61b8-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c61b8-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c61b8-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c61b8-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c61b8-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c61b8-109">DESCRIPTION</span></span>
<span data-ttu-id="c61b8-110">Frissíti a meglévő rugalmas MySQL-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="c61b8-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="c61b8-111">A kérés törzse a normál kiszolgálódefinícióban található tulajdonságok közül egy vagy többet tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="c61b8-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c61b8-112">Használjon Update-AzMySqlFlexibleServerConfiguration kiszolgálóparamétereket, például wait_timeout vagy net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="c61b8-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c61b8-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c61b8-113">EXAMPLES</span></span>

### <span data-ttu-id="c61b8-114">1. példa: A MySql-kiszolgáló frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="c61b8-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="c61b8-115">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="c61b8-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="c61b8-116">2. példa: A MySql-kiszolgáló frissítése identitás alapján.</span><span class="sxs-lookup"><span data-stu-id="c61b8-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="c61b8-117">Ez a parancsmag identitás szerint frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="c61b8-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="c61b8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c61b8-118">PARAMETERS</span></span>

### <span data-ttu-id="c61b8-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c61b8-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c61b8-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="c61b8-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="c61b8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c61b8-121">-AsJob</span></span>
<span data-ttu-id="c61b8-122">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="c61b8-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="c61b8-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="c61b8-123">-BackupRetentionDay</span></span>
<span data-ttu-id="c61b8-124">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="c61b8-124">Backup retention days for the server.</span></span>
<span data-ttu-id="c61b8-125">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="c61b8-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="c61b8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61b8-126">-DefaultProfile</span></span>
<span data-ttu-id="c61b8-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c61b8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c61b8-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="c61b8-128">-HaEnabled</span></span>
<span data-ttu-id="c61b8-129">A magas elérhetőségű funkció engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="c61b8-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61b8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c61b8-130">-InputObject</span></span>
<span data-ttu-id="c61b8-131">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="c61b8-131">Identity Parameter.</span></span>
<span data-ttu-id="c61b8-132">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="c61b8-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c61b8-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c61b8-133">-Name</span></span>
<span data-ttu-id="c61b8-134">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-134">The name of the server.</span></span>

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

### <span data-ttu-id="c61b8-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c61b8-135">-NoWait</span></span>
<span data-ttu-id="c61b8-136">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="c61b8-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c61b8-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="c61b8-137">-ReplicationRole</span></span>
<span data-ttu-id="c61b8-138">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="c61b8-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="c61b8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c61b8-139">-ResourceGroupName</span></span>
<span data-ttu-id="c61b8-140">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c61b8-141">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="c61b8-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c61b8-142">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="c61b8-142">-Sku</span></span>
<span data-ttu-id="c61b8-143">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c61b8-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="c61b8-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c61b8-144">-SkuTier</span></span>
<span data-ttu-id="c61b8-145">Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="c61b8-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="c61b8-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="c61b8-146">-SslEnforcement</span></span>
<span data-ttu-id="c61b8-147">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="c61b8-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="c61b8-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="c61b8-148">-StorageAutogrow</span></span>
<span data-ttu-id="c61b8-149">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="c61b8-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="c61b8-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="c61b8-150">-StorageInMb</span></span>
<span data-ttu-id="c61b8-151">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="c61b8-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="c61b8-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c61b8-152">-SubscriptionId</span></span>
<span data-ttu-id="c61b8-153">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="c61b8-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c61b8-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="c61b8-154">-Tag</span></span>
<span data-ttu-id="c61b8-155">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="c61b8-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c61b8-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c61b8-156">-Confirm</span></span>
<span data-ttu-id="c61b8-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c61b8-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c61b8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c61b8-158">-WhatIf</span></span>
<span data-ttu-id="c61b8-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c61b8-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c61b8-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c61b8-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c61b8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61b8-161">CommonParameters</span></span>
<span data-ttu-id="c61b8-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c61b8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61b8-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c61b8-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61b8-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c61b8-164">INPUTS</span></span>

### <span data-ttu-id="c61b8-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c61b8-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c61b8-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c61b8-166">OUTPUTS</span></span>

### <span data-ttu-id="c61b8-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c61b8-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="c61b8-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c61b8-168">NOTES</span></span>

<span data-ttu-id="c61b8-169">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c61b8-169">ALIASES</span></span>

<span data-ttu-id="c61b8-170">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c61b8-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c61b8-171">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c61b8-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c61b8-172">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c61b8-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c61b8-173">INPUTOBJECT: <IMySqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="c61b8-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="c61b8-174">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c61b8-175">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c61b8-176">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c61b8-177">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c61b8-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c61b8-178">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c61b8-179">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c61b8-180">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c61b8-181">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c61b8-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="c61b8-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c61b8-183">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c61b8-184">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c61b8-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c61b8-185">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c61b8-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c61b8-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c61b8-186">RELATED LINKS</span></span>

