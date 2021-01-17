---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351125"
---
# <span data-ttu-id="53c77-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="53c77-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="53c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c77-102">SYNOPSIS</span></span>
<span data-ttu-id="53c77-103">Létrehozza egy MariaDB-kiszolgáló másolatát.</span><span class="sxs-lookup"><span data-stu-id="53c77-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="53c77-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53c77-104">SYNTAX</span></span>

### <span data-ttu-id="53c77-105">ServerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53c77-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53c77-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="53c77-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="53c77-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53c77-107">DESCRIPTION</span></span>
<span data-ttu-id="53c77-108">Létrehozza egy MariaDB-kiszolgáló másolatát.</span><span class="sxs-lookup"><span data-stu-id="53c77-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="53c77-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53c77-109">EXAMPLES</span></span>

### <span data-ttu-id="53c77-110">1. példa: Másolat létrehozása a MariaDB-hez</span><span class="sxs-lookup"><span data-stu-id="53c77-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="53c77-111">Ez a parancs létrehoz egy másodpéldányt egy MariaDB-hez.</span><span class="sxs-lookup"><span data-stu-id="53c77-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="53c77-112">2. példa: Másolat létrehozása a MariaDB-hez</span><span class="sxs-lookup"><span data-stu-id="53c77-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="53c77-113">Ez a parancs létrehoz egy másodpéldányt egy MariaDB-hez.</span><span class="sxs-lookup"><span data-stu-id="53c77-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="53c77-114">3. példa: Másolat létrehozása a MariaDB-hez</span><span class="sxs-lookup"><span data-stu-id="53c77-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="53c77-115">Ez a paraméter inputobject paramétert is kezelő parancs létrehoz egy adatbázis-másolatot, amely paraméter inputobject paraméterrel van megadva egy MariaDB-hez.</span><span class="sxs-lookup"><span data-stu-id="53c77-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="53c77-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53c77-116">PARAMETERS</span></span>

### <span data-ttu-id="53c77-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53c77-117">-AsJob</span></span>
<span data-ttu-id="53c77-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="53c77-118">Run the command as a job</span></span>

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

### <span data-ttu-id="53c77-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c77-119">-DefaultProfile</span></span>
<span data-ttu-id="53c77-120">régió DefaultParameters Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53c77-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c77-121">-Location</span><span class="sxs-lookup"><span data-stu-id="53c77-121">-Location</span></span>
<span data-ttu-id="53c77-122">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="53c77-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="53c77-123">-Master</span><span class="sxs-lookup"><span data-stu-id="53c77-123">-Master</span></span>
<span data-ttu-id="53c77-124">Az a forráskiszolgáló-objektum, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="53c77-124">The source server object to restore from.</span></span>
<span data-ttu-id="53c77-125">Ennek létrehozásához a FŐtulajdonságok MEGJEGYZÉSEK szakaszában és egy kivonattábla létrehozásában is részt kell látnia.</span><span class="sxs-lookup"><span data-stu-id="53c77-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53c77-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="53c77-126">-MasterName</span></span>
<span data-ttu-id="53c77-127">A MariaDB-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="53c77-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="53c77-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="53c77-128">-NoWait</span></span>
<span data-ttu-id="53c77-129">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="53c77-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="53c77-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="53c77-130">-ReplicaName</span></span>
<span data-ttu-id="53c77-131">Replikanév.</span><span class="sxs-lookup"><span data-stu-id="53c77-131">Replica name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c77-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c77-132">-ResourceGroupName</span></span>
<span data-ttu-id="53c77-133">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="53c77-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="53c77-134">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="53c77-134">-Sku</span></span>
<span data-ttu-id="53c77-135">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="53c77-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="53c77-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53c77-136">-SubscriptionId</span></span>
<span data-ttu-id="53c77-137">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="53c77-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="53c77-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="53c77-138">-Tag</span></span>
<span data-ttu-id="53c77-139">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="53c77-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="53c77-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53c77-140">-Confirm</span></span>
<span data-ttu-id="53c77-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53c77-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c77-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c77-142">-WhatIf</span></span>
<span data-ttu-id="53c77-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53c77-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c77-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53c77-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c77-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c77-145">CommonParameters</span></span>
<span data-ttu-id="53c77-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c77-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c77-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53c77-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c77-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53c77-148">INPUTS</span></span>

### <span data-ttu-id="53c77-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="53c77-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="53c77-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53c77-150">OUTPUTS</span></span>

### <span data-ttu-id="53c77-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="53c77-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="53c77-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53c77-152">NOTES</span></span>

<span data-ttu-id="53c77-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="53c77-153">ALIASES</span></span>

<span data-ttu-id="53c77-154">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="53c77-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53c77-155">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="53c77-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53c77-156">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53c77-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53c77-157">MESTER: <IServer> Az a forráskiszolgáló-objektum, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="53c77-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="53c77-158">`Location <String>`: Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="53c77-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="53c77-159">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="53c77-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="53c77-160">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="53c77-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="53c77-161">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="53c77-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="53c77-162">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="53c77-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="53c77-163">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="53c77-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="53c77-164">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="53c77-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="53c77-165">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="53c77-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="53c77-166">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="53c77-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="53c77-167">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53c77-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="53c77-168">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="53c77-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="53c77-169">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="53c77-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="53c77-170">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="53c77-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="53c77-171">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="53c77-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="53c77-172">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="53c77-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="53c77-173">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="53c77-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="53c77-174">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="53c77-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="53c77-175">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="53c77-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="53c77-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="53c77-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="53c77-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy ne a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="53c77-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="53c77-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="53c77-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="53c77-179">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="53c77-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="53c77-180">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="53c77-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="53c77-181">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="53c77-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="53c77-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53c77-182">RELATED LINKS</span></span>

