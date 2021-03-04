---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 95807621ffb054610a5778872db243eea50a7efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927073"
---
# <span data-ttu-id="577e0-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="577e0-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="577e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577e0-102">SYNOPSIS</span></span>
<span data-ttu-id="577e0-103">Kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="577e0-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="577e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="577e0-104">SYNTAX</span></span>

### <span data-ttu-id="577e0-105">GeoRestore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="577e0-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="577e0-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="577e0-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="577e0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="577e0-107">DESCRIPTION</span></span>
<span data-ttu-id="577e0-108">Kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="577e0-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="577e0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="577e0-109">EXAMPLES</span></span>

### <span data-ttu-id="577e0-110">1. példa: A MySql-kiszolgáló visszaállítása a GeoReplica restore használatával</span><span class="sxs-lookup"><span data-stu-id="577e0-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="577e0-111">Ez a parancsmag a GeoReplica restore használatával visszaállítja a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="577e0-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="577e0-112">2. példa: A MySql-kiszolgáló visszaállítása a PointInTime-visszaállítás használatával</span><span class="sxs-lookup"><span data-stu-id="577e0-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="577e0-113">Ezek a parancsmagok visszaállítják a MySql-kiszolgálót a PointInTime Restore használatával.</span><span class="sxs-lookup"><span data-stu-id="577e0-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="577e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="577e0-114">PARAMETERS</span></span>

### <span data-ttu-id="577e0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="577e0-115">-AsJob</span></span>
<span data-ttu-id="577e0-116">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="577e0-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="577e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577e0-117">-DefaultProfile</span></span>
<span data-ttu-id="577e0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="577e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="577e0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="577e0-119">-InputObject</span></span>
<span data-ttu-id="577e0-120">Az a forráskiszolgáló-objektum, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="577e0-120">The source server object to restore from.</span></span>
<span data-ttu-id="577e0-121">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="577e0-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="577e0-122">-Location</span><span class="sxs-lookup"><span data-stu-id="577e0-122">-Location</span></span>
<span data-ttu-id="577e0-123">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="577e0-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="577e0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="577e0-124">-Name</span></span>
<span data-ttu-id="577e0-125">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="577e0-125">The name of the server.</span></span>

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

### <span data-ttu-id="577e0-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="577e0-126">-NoWait</span></span>
<span data-ttu-id="577e0-127">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="577e0-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="577e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="577e0-129">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="577e0-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="577e0-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="577e0-130">-RestorePointInTime</span></span>
<span data-ttu-id="577e0-131">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="577e0-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="577e0-132">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="577e0-132">-Sku</span></span>
<span data-ttu-id="577e0-133">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="577e0-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="577e0-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="577e0-134">-SubscriptionId</span></span>
<span data-ttu-id="577e0-135">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="577e0-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="577e0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="577e0-136">-Tag</span></span>
<span data-ttu-id="577e0-137">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="577e0-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="577e0-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="577e0-138">-UseGeoRestore</span></span>
<span data-ttu-id="577e0-139">Visszaállítás geomód használatával</span><span class="sxs-lookup"><span data-stu-id="577e0-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="577e0-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="577e0-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="577e0-141">A PointInTime mód használata visszaállításhoz</span><span class="sxs-lookup"><span data-stu-id="577e0-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="577e0-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="577e0-142">-Confirm</span></span>
<span data-ttu-id="577e0-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="577e0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577e0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577e0-144">-WhatIf</span></span>
<span data-ttu-id="577e0-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="577e0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577e0-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="577e0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577e0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577e0-147">CommonParameters</span></span>
<span data-ttu-id="577e0-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577e0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577e0-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="577e0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577e0-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="577e0-150">INPUTS</span></span>

### <span data-ttu-id="577e0-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="577e0-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="577e0-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="577e0-152">OUTPUTS</span></span>

### <span data-ttu-id="577e0-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="577e0-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="577e0-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="577e0-154">NOTES</span></span>

<span data-ttu-id="577e0-155">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="577e0-155">ALIASES</span></span>

<span data-ttu-id="577e0-156">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="577e0-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="577e0-157">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="577e0-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="577e0-158">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="577e0-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="577e0-159">INPUTOBJECT: Az a <IServer> forráskiszolgáló-objektum, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="577e0-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="577e0-160">`Location <String>`: Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="577e0-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="577e0-161">`[Tag <ITrackedResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="577e0-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="577e0-162">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="577e0-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="577e0-163">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="577e0-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="577e0-164">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="577e0-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="577e0-165">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="577e0-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="577e0-166">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="577e0-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="577e0-167">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="577e0-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="577e0-168">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="577e0-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="577e0-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amely azt mutatja, hogy a kiszolgáló engedélyezte-e az infrastruktúra-titkosítást.</span><span class="sxs-lookup"><span data-stu-id="577e0-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="577e0-170">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="577e0-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="577e0-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Csak minimális Tls-verzió legyen érvényes a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="577e0-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="577e0-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Hogy engedélyezett-e a nyilvános hálózati hozzáférés ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="577e0-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="577e0-173">Az érték megadása nem kötelező, de ha be van engedélyezve, akkor "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="577e0-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="577e0-174">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="577e0-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="577e0-175">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="577e0-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="577e0-176">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="577e0-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="577e0-177">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="577e0-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="577e0-178">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="577e0-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="577e0-179">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="577e0-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="577e0-180">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="577e0-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="577e0-181">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="577e0-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="577e0-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="577e0-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="577e0-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy ne a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="577e0-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="577e0-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="577e0-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="577e0-185">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="577e0-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="577e0-186">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="577e0-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="577e0-187">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="577e0-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="577e0-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="577e0-188">RELATED LINKS</span></span>

