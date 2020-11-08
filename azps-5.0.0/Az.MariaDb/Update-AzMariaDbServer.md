---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195800"
---
# <span data-ttu-id="ec166-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="ec166-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="ec166-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec166-102">SYNOPSIS</span></span>
<span data-ttu-id="ec166-103">Frissít egy meglévő kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="ec166-103">Updates an existing server.</span></span>
<span data-ttu-id="ec166-104">A kérelem törzse tartalmazhat egyet a normál kiszolgálói definícióban szereplő tulajdonságok közül.</span><span class="sxs-lookup"><span data-stu-id="ec166-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="ec166-105">Ha a kiszolgálói paramétereket (például wait_timeout vagy net_retry_count) szeretné használni, használja a Update-AzMariaDbConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="ec166-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="ec166-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec166-106">SYNTAX</span></span>

### <span data-ttu-id="ec166-107">Kiszolgálónév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec166-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec166-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="ec166-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec166-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec166-109">DESCRIPTION</span></span>
<span data-ttu-id="ec166-110">Frissít egy meglévő kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="ec166-110">Updates an existing server.</span></span>
<span data-ttu-id="ec166-111">A kérelem törzse tartalmazhat egyet a normál kiszolgálói definícióban szereplő tulajdonságok közül.</span><span class="sxs-lookup"><span data-stu-id="ec166-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="ec166-112">Ha a kiszolgálói paramétereket (például wait_timeout vagy net_retry_count) szeretné használni, használja a Update-AzMariaDbConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="ec166-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="ec166-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ec166-113">EXAMPLES</span></span>

### <span data-ttu-id="ec166-114">Példa 1: a MariaDB frissítése</span><span class="sxs-lookup"><span data-stu-id="ec166-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="ec166-115">Ez a parancs frissíti a MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ec166-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="ec166-116">2. példa: a MariaDB frissítése</span><span class="sxs-lookup"><span data-stu-id="ec166-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="ec166-117">Ez a parancs frissíti a MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ec166-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="ec166-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec166-118">PARAMETERS</span></span>

### <span data-ttu-id="ec166-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ec166-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ec166-120">A rendszergazdai bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="ec166-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="ec166-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec166-121">-AsJob</span></span>
<span data-ttu-id="ec166-122">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="ec166-122">Run the command as a job</span></span>

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

### <span data-ttu-id="ec166-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ec166-123">-BackupRetentionDay</span></span>
<span data-ttu-id="ec166-124">A kiszolgáló biztonságimásolat-adatmegőrzési napjai</span><span class="sxs-lookup"><span data-stu-id="ec166-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="ec166-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec166-125">-DefaultProfile</span></span>
<span data-ttu-id="ec166-126">terület: az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetések DefaultParameters.</span><span class="sxs-lookup"><span data-stu-id="ec166-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec166-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="ec166-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="ec166-128">Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="ec166-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="ec166-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec166-129">-InputObject</span></span>
<span data-ttu-id="ec166-130">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec166-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec166-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec166-131">-Name</span></span>
<span data-ttu-id="ec166-132">MariaDB-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="ec166-132">MariaDB server name</span></span>

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

### <span data-ttu-id="ec166-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="ec166-133">-NoWait</span></span>
<span data-ttu-id="ec166-134">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="ec166-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec166-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="ec166-135">-ReplicationRole</span></span>
<span data-ttu-id="ec166-136">A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="ec166-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="ec166-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec166-137">-ResourceGroupName</span></span>
<span data-ttu-id="ec166-138">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="ec166-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="ec166-139">-Sku</span></span>
<span data-ttu-id="ec166-140">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ec166-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ec166-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="ec166-141">-SslEnforcement</span></span>
<span data-ttu-id="ec166-142">Engedélyezze az SSL-kényszerítést, vagy ne a csatlakozás a kiszolgálóhoz lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ec166-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="ec166-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="ec166-143">-StorageAutogrow</span></span>
<span data-ttu-id="ec166-144">A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ec166-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="ec166-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ec166-145">-StorageInMb</span></span>
<span data-ttu-id="ec166-146">Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ec166-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="ec166-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec166-147">-SubscriptionId</span></span>
<span data-ttu-id="ec166-148">Az előfizetési azonosító az összes szolgáltatási hívás URI-ja része</span><span class="sxs-lookup"><span data-stu-id="ec166-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="ec166-149">-Címke</span><span class="sxs-lookup"><span data-stu-id="ec166-149">-Tag</span></span>
<span data-ttu-id="ec166-150">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="ec166-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ec166-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec166-151">-Confirm</span></span>
<span data-ttu-id="ec166-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec166-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec166-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec166-153">-WhatIf</span></span>
<span data-ttu-id="ec166-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec166-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec166-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec166-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec166-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec166-156">CommonParameters</span></span>
<span data-ttu-id="ec166-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec166-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec166-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec166-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec166-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec166-159">INPUTS</span></span>

### <span data-ttu-id="ec166-160">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="ec166-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ec166-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec166-161">OUTPUTS</span></span>

### <span data-ttu-id="ec166-162">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="ec166-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ec166-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec166-163">NOTES</span></span>

<span data-ttu-id="ec166-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ec166-164">ALIASES</span></span>

<span data-ttu-id="ec166-165">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="ec166-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec166-166">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ec166-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec166-167">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ec166-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec166-168">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ec166-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec166-169">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ec166-170">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ec166-171">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ec166-172">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ec166-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec166-173">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ec166-174">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ec166-175">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="ec166-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ec166-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ec166-177">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ec166-178">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="ec166-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ec166-179">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ec166-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ec166-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec166-180">RELATED LINKS</span></span>

