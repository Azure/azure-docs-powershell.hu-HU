---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024688"
---
# <span data-ttu-id="8ba93-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="8ba93-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="8ba93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ba93-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba93-103">Kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="8ba93-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="8ba93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ba93-104">SYNTAX</span></span>

### <span data-ttu-id="8ba93-105">GeoRestore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ba93-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ba93-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="8ba93-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8ba93-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ba93-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba93-108">Kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="8ba93-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="8ba93-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8ba93-109">EXAMPLES</span></span>

### <span data-ttu-id="8ba93-110">1. példa: a MySql-kiszolgáló visszaállítása a GeoReplica visszaállításával</span><span class="sxs-lookup"><span data-stu-id="8ba93-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8ba93-111">Ez a parancsmag visszaállítja a MySql szervert a GeoReplica visszaállításával.</span><span class="sxs-lookup"><span data-stu-id="8ba93-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="8ba93-112">2. példa: a MySql-kiszolgáló visszaállítása a PointInTime visszaállításával</span><span class="sxs-lookup"><span data-stu-id="8ba93-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8ba93-113">Ezek a parancsmagok a MySql szervert a PointInTime Restore használatával állítják vissza.</span><span class="sxs-lookup"><span data-stu-id="8ba93-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="8ba93-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ba93-114">PARAMETERS</span></span>

### <span data-ttu-id="8ba93-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ba93-115">-AsJob</span></span>
<span data-ttu-id="8ba93-116">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="8ba93-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="8ba93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba93-117">-DefaultProfile</span></span>
<span data-ttu-id="8ba93-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ba93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba93-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba93-119">-InputObject</span></span>
<span data-ttu-id="8ba93-120">A forrás kiszolgálói objektum, amelyből vissza szeretne térni.</span><span class="sxs-lookup"><span data-stu-id="8ba93-120">The source server object to restore from.</span></span>
<span data-ttu-id="8ba93-121">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8ba93-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba93-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="8ba93-122">-Location</span></span>
<span data-ttu-id="8ba93-123">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="8ba93-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8ba93-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ba93-124">-Name</span></span>
<span data-ttu-id="8ba93-125">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="8ba93-125">The name of the server.</span></span>

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

### <span data-ttu-id="8ba93-126">-Várva</span><span class="sxs-lookup"><span data-stu-id="8ba93-126">-NoWait</span></span>
<span data-ttu-id="8ba93-127">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="8ba93-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8ba93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba93-128">-ResourceGroupName</span></span>
<span data-ttu-id="8ba93-129">Az erőforrást tartalmazó erőforráscsoport neve az Azure Resource Manager API-ból vagy a portálról szerzi be ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="8ba93-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8ba93-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="8ba93-130">-RestorePointInTime</span></span>
<span data-ttu-id="8ba93-131">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="8ba93-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8ba93-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="8ba93-132">-Sku</span></span>
<span data-ttu-id="8ba93-133">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8ba93-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8ba93-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ba93-134">-SubscriptionId</span></span>
<span data-ttu-id="8ba93-135">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="8ba93-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8ba93-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="8ba93-136">-Tag</span></span>
<span data-ttu-id="8ba93-137">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="8ba93-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8ba93-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="8ba93-138">-UseGeoRestore</span></span>
<span data-ttu-id="8ba93-139">A Geo mód használata a visszaállításhoz</span><span class="sxs-lookup"><span data-stu-id="8ba93-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="8ba93-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="8ba93-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="8ba93-141">A PointInTime üzemmód használata a visszaállításhoz</span><span class="sxs-lookup"><span data-stu-id="8ba93-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="8ba93-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ba93-142">-Confirm</span></span>
<span data-ttu-id="8ba93-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ba93-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba93-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba93-144">-WhatIf</span></span>
<span data-ttu-id="8ba93-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ba93-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba93-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ba93-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba93-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba93-147">CommonParameters</span></span>
<span data-ttu-id="8ba93-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ba93-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba93-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8ba93-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba93-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba93-150">INPUTS</span></span>

### <span data-ttu-id="8ba93-151">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="8ba93-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8ba93-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba93-152">OUTPUTS</span></span>

### <span data-ttu-id="8ba93-153">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="8ba93-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8ba93-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ba93-154">NOTES</span></span>

<span data-ttu-id="8ba93-155">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8ba93-155">ALIASES</span></span>

<span data-ttu-id="8ba93-156">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="8ba93-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ba93-157">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8ba93-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ba93-158">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8ba93-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ba93-159">INPUTOBJECT <IServer> : a Source Server objektum, amelyből vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="8ba93-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="8ba93-160">`Location <String>`: Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="8ba93-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="8ba93-161">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="8ba93-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="8ba93-162">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="8ba93-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8ba93-163">`[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8ba93-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="8ba93-164">Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="8ba93-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="8ba93-165">`[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="8ba93-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="8ba93-166">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.</span><span class="sxs-lookup"><span data-stu-id="8ba93-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="8ba93-167">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="8ba93-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="8ba93-168">A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.</span><span class="sxs-lookup"><span data-stu-id="8ba93-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="8ba93-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amelyen látható, hogy a kiszolgáló engedélyezve van-e az infrastruktúra titkosítása.</span><span class="sxs-lookup"><span data-stu-id="8ba93-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="8ba93-170">`[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ba93-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="8ba93-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Minimális TLS-verzió érvényesítése a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8ba93-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="8ba93-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: A kiszolgálón engedélyezve van-e a nyilvános hálózatokhoz való hozzáférés.</span><span class="sxs-lookup"><span data-stu-id="8ba93-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="8ba93-173">Az érték nem kötelező, de ha be van kapcsolva, "engedélyezve" vagy "Letiltva" állapotban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8ba93-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="8ba93-174">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.</span><span class="sxs-lookup"><span data-stu-id="8ba93-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="8ba93-175">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="8ba93-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="8ba93-176">`[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8ba93-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="8ba93-177">`[SkuFamily <String>]`: A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="8ba93-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="8ba93-178">`[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8ba93-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="8ba93-179">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.</span><span class="sxs-lookup"><span data-stu-id="8ba93-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="8ba93-180">`[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="8ba93-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="8ba93-181">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="8ba93-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="8ba93-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8ba93-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="8ba93-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="8ba93-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="8ba93-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8ba93-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="8ba93-185">`[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8ba93-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="8ba93-186">`[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="8ba93-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="8ba93-187">`[Version <ServerVersion?>]`: Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="8ba93-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="8ba93-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ba93-188">RELATED LINKS</span></span>

