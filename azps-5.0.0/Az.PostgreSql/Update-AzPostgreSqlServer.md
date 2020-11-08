---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187557"
---
# <span data-ttu-id="6aa98-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="6aa98-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="6aa98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6aa98-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa98-103">Frissít egy meglévő kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aa98-103">Updates an existing server.</span></span>
<span data-ttu-id="6aa98-104">A kérelem törzse tartalmazhat egyet a normál kiszolgálói definícióban szereplő tulajdonságok közül.</span><span class="sxs-lookup"><span data-stu-id="6aa98-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6aa98-105">Ha a kiszolgálói paramétereket (például wait_timeout vagy net_retry_count) szeretné használni, használja a Update-AzPostSqlConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="6aa98-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6aa98-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6aa98-106">SYNTAX</span></span>

### <span data-ttu-id="6aa98-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6aa98-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6aa98-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6aa98-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6aa98-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6aa98-109">DESCRIPTION</span></span>
<span data-ttu-id="6aa98-110">Frissít egy meglévő kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aa98-110">Updates an existing server.</span></span>
<span data-ttu-id="6aa98-111">A kérelem törzse tartalmazhat egyet a normál kiszolgálói definícióban szereplő tulajdonságok közül.</span><span class="sxs-lookup"><span data-stu-id="6aa98-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6aa98-112">Ha a kiszolgálói paramétereket (például wait_timeout vagy net_retry_count) szeretné használni, használja a Update-AzPostSqlConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="6aa98-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6aa98-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6aa98-113">EXAMPLES</span></span>

### <span data-ttu-id="6aa98-114">1. példa: a PostgreSql-kiszolgáló frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="6aa98-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="6aa98-115">Ez a parancsmag az erőforráscsoport és a kiszolgáló neve szerint frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aa98-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="6aa98-116">2. példa: a PostgreSql-kiszolgáló frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="6aa98-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="6aa98-117">Ez a parancsmag identitással frissíti a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aa98-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="6aa98-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6aa98-118">PARAMETERS</span></span>

### <span data-ttu-id="6aa98-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6aa98-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6aa98-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="6aa98-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="6aa98-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aa98-121">-AsJob</span></span>
<span data-ttu-id="6aa98-122">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="6aa98-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="6aa98-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6aa98-123">-BackupRetentionDay</span></span>
<span data-ttu-id="6aa98-124">A kiszolgáló biztonságimásolat-adatmegőrzési napjai</span><span class="sxs-lookup"><span data-stu-id="6aa98-124">Backup retention days for the server.</span></span>
<span data-ttu-id="6aa98-125">A napok száma 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="6aa98-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6aa98-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa98-126">-DefaultProfile</span></span>
<span data-ttu-id="6aa98-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6aa98-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa98-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6aa98-128">-InputObject</span></span>
<span data-ttu-id="6aa98-129">Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6aa98-129">Identity Parameter.</span></span>
<span data-ttu-id="6aa98-130">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6aa98-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6aa98-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6aa98-131">-Name</span></span>
<span data-ttu-id="6aa98-132">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-132">The name of the server.</span></span>

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

### <span data-ttu-id="6aa98-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="6aa98-133">-NoWait</span></span>
<span data-ttu-id="6aa98-134">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="6aa98-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6aa98-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="6aa98-135">-ReplicationRole</span></span>
<span data-ttu-id="6aa98-136">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="6aa98-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="6aa98-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa98-137">-ResourceGroupName</span></span>
<span data-ttu-id="6aa98-138">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6aa98-139">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6aa98-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6aa98-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="6aa98-140">-Sku</span></span>
<span data-ttu-id="6aa98-141">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6aa98-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6aa98-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6aa98-142">-SkuCapacity</span></span>
<span data-ttu-id="6aa98-143">A méretezési/kitöltési kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6aa98-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="6aa98-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="6aa98-144">-SkuFamily</span></span>
<span data-ttu-id="6aa98-145">A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="6aa98-145">The family of hardware.</span></span>

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

### <span data-ttu-id="6aa98-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6aa98-146">-SkuTier</span></span>
<span data-ttu-id="6aa98-147">Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="6aa98-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="6aa98-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="6aa98-148">-SslEnforcement</span></span>
<span data-ttu-id="6aa98-149">Engedélyezze az SSL-kényszerítést, vagy ne a csatlakozás a kiszolgálóhoz lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6aa98-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="6aa98-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="6aa98-150">-StorageAutogrow</span></span>
<span data-ttu-id="6aa98-151">A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="6aa98-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="6aa98-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6aa98-152">-StorageInMb</span></span>
<span data-ttu-id="6aa98-153">Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6aa98-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6aa98-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6aa98-154">-SubscriptionId</span></span>
<span data-ttu-id="6aa98-155">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="6aa98-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6aa98-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="6aa98-156">-Tag</span></span>
<span data-ttu-id="6aa98-157">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="6aa98-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6aa98-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6aa98-158">-Confirm</span></span>
<span data-ttu-id="6aa98-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6aa98-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa98-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa98-160">-WhatIf</span></span>
<span data-ttu-id="6aa98-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6aa98-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aa98-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6aa98-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa98-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa98-163">CommonParameters</span></span>
<span data-ttu-id="6aa98-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6aa98-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa98-165">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6aa98-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa98-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aa98-166">INPUTS</span></span>

### <span data-ttu-id="6aa98-167">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6aa98-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6aa98-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aa98-168">OUTPUTS</span></span>

### <span data-ttu-id="6aa98-169">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="6aa98-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6aa98-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6aa98-170">NOTES</span></span>

<span data-ttu-id="6aa98-171">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6aa98-171">ALIASES</span></span>

<span data-ttu-id="6aa98-172">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6aa98-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6aa98-173">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6aa98-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6aa98-174">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6aa98-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6aa98-175">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6aa98-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="6aa98-176">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6aa98-177">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6aa98-178">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6aa98-179">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6aa98-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6aa98-180">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6aa98-181">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6aa98-182">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6aa98-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="6aa98-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6aa98-184">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6aa98-185">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6aa98-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6aa98-186">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6aa98-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6aa98-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6aa98-187">RELATED LINKS</span></span>

