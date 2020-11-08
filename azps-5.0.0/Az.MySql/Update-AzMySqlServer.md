---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: e23cc8b942033805d8ed8cd122b19e6a59bf457c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187615"
---
# <span data-ttu-id="0024d-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="0024d-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="0024d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0024d-102">SYNOPSIS</span></span>
<span data-ttu-id="0024d-103">Frissít egy meglévő kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="0024d-103">Updates an existing server.</span></span>
<span data-ttu-id="0024d-104">A kérelem törzse tartalmazhat egyet a normál kiszolgálói definícióban szereplő tulajdonságok közül.</span><span class="sxs-lookup"><span data-stu-id="0024d-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0024d-105">Ha a kiszolgálói paramétereket (például wait_timeout vagy net_retry_count) szeretné használni, használja a Update-AzMySqlConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="0024d-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0024d-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0024d-106">SYNTAX</span></span>

### <span data-ttu-id="0024d-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0024d-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0024d-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0024d-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0024d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0024d-109">DESCRIPTION</span></span>
<span data-ttu-id="0024d-110">Frissít egy meglévő kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="0024d-110">Updates an existing server.</span></span>
<span data-ttu-id="0024d-111">A kérelem törzse tartalmazhat egyet a normál kiszolgálói definícióban szereplő tulajdonságok közül.</span><span class="sxs-lookup"><span data-stu-id="0024d-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0024d-112">Ha a kiszolgálói paramétereket (például wait_timeout vagy net_retry_count) szeretné használni, használja a Update-AzMySqlConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="0024d-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0024d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0024d-113">EXAMPLES</span></span>

### <span data-ttu-id="0024d-114">1. példa: a MySql-kiszolgáló frissítése az erőforráscsoport és a kiszolgáló neve szerint</span><span class="sxs-lookup"><span data-stu-id="0024d-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0024d-115">Ez a parancsmag az erőforráscsoport és a kiszolgáló neve szerint frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="0024d-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="0024d-116">2. példa: frissítse a MySql szervert identitással.</span><span class="sxs-lookup"><span data-stu-id="0024d-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0024d-117">Ez a parancsmag identitással frissíti a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="0024d-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="0024d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0024d-118">PARAMETERS</span></span>

### <span data-ttu-id="0024d-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="0024d-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="0024d-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="0024d-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="0024d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0024d-121">-AsJob</span></span>
<span data-ttu-id="0024d-122">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="0024d-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="0024d-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="0024d-123">-BackupRetentionDay</span></span>
<span data-ttu-id="0024d-124">A kiszolgáló biztonságimásolat-adatmegőrzési napjai</span><span class="sxs-lookup"><span data-stu-id="0024d-124">Backup retention days for the server.</span></span>
<span data-ttu-id="0024d-125">A napok száma 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="0024d-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="0024d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0024d-126">-DefaultProfile</span></span>
<span data-ttu-id="0024d-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0024d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0024d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0024d-128">-InputObject</span></span>
<span data-ttu-id="0024d-129">Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0024d-129">Identity Parameter.</span></span>
<span data-ttu-id="0024d-130">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0024d-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0024d-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0024d-131">-Name</span></span>
<span data-ttu-id="0024d-132">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-132">The name of the server.</span></span>

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

### <span data-ttu-id="0024d-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="0024d-133">-NoWait</span></span>
<span data-ttu-id="0024d-134">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="0024d-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0024d-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="0024d-135">-ReplicationRole</span></span>
<span data-ttu-id="0024d-136">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="0024d-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="0024d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0024d-137">-ResourceGroupName</span></span>
<span data-ttu-id="0024d-138">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0024d-139">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="0024d-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0024d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="0024d-140">-Sku</span></span>
<span data-ttu-id="0024d-141">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0024d-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0024d-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0024d-142">-SkuCapacity</span></span>
<span data-ttu-id="0024d-143">A méretezési/kitöltési kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0024d-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="0024d-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="0024d-144">-SkuFamily</span></span>
<span data-ttu-id="0024d-145">A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="0024d-145">The family of hardware.</span></span>

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

### <span data-ttu-id="0024d-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0024d-146">-SkuTier</span></span>
<span data-ttu-id="0024d-147">Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="0024d-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="0024d-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="0024d-148">-SslEnforcement</span></span>
<span data-ttu-id="0024d-149">Engedélyezze az SSL-kényszerítést, vagy ne a csatlakozás a kiszolgálóhoz lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0024d-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="0024d-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="0024d-150">-StorageAutogrow</span></span>
<span data-ttu-id="0024d-151">A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="0024d-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="0024d-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="0024d-152">-StorageInMb</span></span>
<span data-ttu-id="0024d-153">Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="0024d-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="0024d-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0024d-154">-SubscriptionId</span></span>
<span data-ttu-id="0024d-155">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="0024d-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0024d-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="0024d-156">-Tag</span></span>
<span data-ttu-id="0024d-157">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="0024d-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0024d-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0024d-158">-Confirm</span></span>
<span data-ttu-id="0024d-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0024d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0024d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0024d-160">-WhatIf</span></span>
<span data-ttu-id="0024d-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0024d-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0024d-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0024d-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0024d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0024d-163">CommonParameters</span></span>
<span data-ttu-id="0024d-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0024d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0024d-165">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0024d-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0024d-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0024d-166">INPUTS</span></span>

### <span data-ttu-id="0024d-167">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0024d-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0024d-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0024d-168">OUTPUTS</span></span>

### <span data-ttu-id="0024d-169">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0024d-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0024d-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0024d-170">NOTES</span></span>

<span data-ttu-id="0024d-171">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0024d-171">ALIASES</span></span>

<span data-ttu-id="0024d-172">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="0024d-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0024d-173">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0024d-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0024d-174">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0024d-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0024d-175">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0024d-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="0024d-176">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0024d-177">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0024d-178">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0024d-179">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0024d-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0024d-180">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0024d-181">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0024d-182">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="0024d-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="0024d-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0024d-184">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0024d-185">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0024d-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0024d-186">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0024d-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0024d-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0024d-187">RELATED LINKS</span></span>

