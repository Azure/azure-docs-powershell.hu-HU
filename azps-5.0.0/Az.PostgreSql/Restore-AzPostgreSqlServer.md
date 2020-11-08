---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: c9e4134b6787f78442a18836c15ce190c3e685d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187559"
---
# <span data-ttu-id="f41cb-101">Restore-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="f41cb-101">Restore-AzPostgreSqlServer</span></span>

## <span data-ttu-id="f41cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f41cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f41cb-103">Kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="f41cb-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="f41cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f41cb-104">SYNTAX</span></span>

### <span data-ttu-id="f41cb-105">GeoRestore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f41cb-105">GeoRestore (Default)</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f41cb-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="f41cb-106">PointInTimeRestore</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f41cb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f41cb-107">DESCRIPTION</span></span>
<span data-ttu-id="f41cb-108">Kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="f41cb-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="f41cb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f41cb-109">EXAMPLES</span></span>

### <span data-ttu-id="f41cb-110">1. példa: a PostgreSql-kiszolgáló visszaállítása a GeoReplica visszaállításával</span><span class="sxs-lookup"><span data-stu-id="f41cb-110">Example 1: Restore PostgreSql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f41cb-111">Ez a parancsmag visszaállítja a PostgreSql-kiszolgálót a GeoReplica visszaállításával.</span><span class="sxs-lookup"><span data-stu-id="f41cb-111">This cmdlet restores PostgreSql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="f41cb-112">2. példa: a PostgreSql-kiszolgáló visszaállítása a PointInTime visszaállításával</span><span class="sxs-lookup"><span data-stu-id="f41cb-112">Example 2: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f41cb-113">Ezek a parancsmagok a PostgreSql szervert a PointInTime Restore használatával állítják vissza.</span><span class="sxs-lookup"><span data-stu-id="f41cb-113">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="f41cb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f41cb-114">PARAMETERS</span></span>

### <span data-ttu-id="f41cb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f41cb-115">-AsJob</span></span>
<span data-ttu-id="f41cb-116">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="f41cb-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="f41cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41cb-117">-DefaultProfile</span></span>
<span data-ttu-id="f41cb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f41cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f41cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f41cb-119">-InputObject</span></span>
<span data-ttu-id="f41cb-120">A forrás kiszolgálói objektum, amelyből vissza szeretne térni.</span><span class="sxs-lookup"><span data-stu-id="f41cb-120">The source server object to restore from.</span></span>
<span data-ttu-id="f41cb-121">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f41cb-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f41cb-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="f41cb-122">-Location</span></span>
<span data-ttu-id="f41cb-123">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="f41cb-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f41cb-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f41cb-124">-Name</span></span>
<span data-ttu-id="f41cb-125">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f41cb-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41cb-126">-Várva</span><span class="sxs-lookup"><span data-stu-id="f41cb-126">-NoWait</span></span>
<span data-ttu-id="f41cb-127">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="f41cb-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="f41cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="f41cb-129">Az erőforrást tartalmazó erőforráscsoport neve az Azure Resource Manager API-ból vagy a portálról szerzi be ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="f41cb-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41cb-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="f41cb-130">-RestorePointInTime</span></span>
<span data-ttu-id="f41cb-131">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="f41cb-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41cb-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="f41cb-132">-Sku</span></span>
<span data-ttu-id="f41cb-133">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f41cb-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="f41cb-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f41cb-134">-SubscriptionId</span></span>
<span data-ttu-id="f41cb-135">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f41cb-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41cb-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="f41cb-136">-Tag</span></span>
<span data-ttu-id="f41cb-137">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="f41cb-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f41cb-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="f41cb-138">-UseGeoRestore</span></span>
<span data-ttu-id="f41cb-139">A Geo mód használata a visszaállításhoz</span><span class="sxs-lookup"><span data-stu-id="f41cb-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41cb-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="f41cb-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="f41cb-141">A PointInTime üzemmód használata a visszaállításhoz</span><span class="sxs-lookup"><span data-stu-id="f41cb-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41cb-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f41cb-142">-Confirm</span></span>
<span data-ttu-id="f41cb-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f41cb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f41cb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f41cb-144">-WhatIf</span></span>
<span data-ttu-id="f41cb-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f41cb-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f41cb-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f41cb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f41cb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41cb-147">CommonParameters</span></span>
<span data-ttu-id="f41cb-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f41cb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41cb-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f41cb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41cb-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f41cb-150">INPUTS</span></span>

### <span data-ttu-id="f41cb-151">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="f41cb-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f41cb-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f41cb-152">OUTPUTS</span></span>

### <span data-ttu-id="f41cb-153">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="f41cb-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f41cb-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f41cb-154">NOTES</span></span>

<span data-ttu-id="f41cb-155">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f41cb-155">ALIASES</span></span>

<span data-ttu-id="f41cb-156">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f41cb-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f41cb-157">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f41cb-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f41cb-158">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f41cb-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f41cb-159">INPUTOBJECT <IServer> : a Source Server objektum, amelyből vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="f41cb-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="f41cb-160">`Location <String>`: Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="f41cb-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="f41cb-161">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="f41cb-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="f41cb-162">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="f41cb-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f41cb-163">`[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="f41cb-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="f41cb-164">Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="f41cb-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="f41cb-165">`[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="f41cb-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="f41cb-166">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.</span><span class="sxs-lookup"><span data-stu-id="f41cb-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="f41cb-167">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="f41cb-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="f41cb-168">A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.</span><span class="sxs-lookup"><span data-stu-id="f41cb-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="f41cb-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amelyen látható, hogy a kiszolgáló engedélyezve van-e az infrastruktúra titkosítása.</span><span class="sxs-lookup"><span data-stu-id="f41cb-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="f41cb-170">`[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f41cb-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="f41cb-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Minimális TLS-verzió érvényesítése a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="f41cb-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="f41cb-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: A kiszolgálón engedélyezve van-e a nyilvános hálózatokhoz való hozzáférés.</span><span class="sxs-lookup"><span data-stu-id="f41cb-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="f41cb-173">Az érték nem kötelező, de ha be van kapcsolva, "engedélyezve" vagy "Letiltva" állapotban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f41cb-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="f41cb-174">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.</span><span class="sxs-lookup"><span data-stu-id="f41cb-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="f41cb-175">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="f41cb-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="f41cb-176">`[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f41cb-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="f41cb-177">`[SkuFamily <String>]`: A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="f41cb-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="f41cb-178">`[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f41cb-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="f41cb-179">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.</span><span class="sxs-lookup"><span data-stu-id="f41cb-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="f41cb-180">`[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="f41cb-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="f41cb-181">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="f41cb-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="f41cb-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="f41cb-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="f41cb-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="f41cb-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="f41cb-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f41cb-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="f41cb-185">`[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="f41cb-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="f41cb-186">`[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="f41cb-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="f41cb-187">`[Version <ServerVersion?>]`: Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="f41cb-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="f41cb-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f41cb-188">RELATED LINKS</span></span>

