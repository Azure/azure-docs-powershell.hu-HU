---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194358"
---
# <span data-ttu-id="6a1a1-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="6a1a1-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="6a1a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1a1-103">Egy MariaDB-kiszolgáló replikáját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="6a1a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a1a1-104">SYNTAX</span></span>

### <span data-ttu-id="6a1a1-105">Kiszolgálónév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a1a1-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a1a1-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="6a1a1-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6a1a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a1a1-107">DESCRIPTION</span></span>
<span data-ttu-id="6a1a1-108">Egy MariaDB-kiszolgáló replikáját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="6a1a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6a1a1-109">EXAMPLES</span></span>

### <span data-ttu-id="6a1a1-110">Példa 1: replika db létrehozása MariaDB</span><span class="sxs-lookup"><span data-stu-id="6a1a1-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6a1a1-111">A parancs létrehoz egy MariaDB a replika dB-t.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="6a1a1-112">2. példa: a replika db létrehozása egy MariaDB</span><span class="sxs-lookup"><span data-stu-id="6a1a1-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6a1a1-113">A parancs létrehoz egy MariaDB a replika dB-t.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="6a1a1-114">3. példa: a replika db létrehozása MariaDB</span><span class="sxs-lookup"><span data-stu-id="6a1a1-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6a1a1-115">Ez a parancs a inputobject paraméterrel létrehoz egy replika dB-t a MariaDB paraméter inputobject.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="6a1a1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a1a1-116">PARAMETERS</span></span>

### <span data-ttu-id="6a1a1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a1a1-117">-AsJob</span></span>
<span data-ttu-id="6a1a1-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="6a1a1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6a1a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1a1-119">-DefaultProfile</span></span>
<span data-ttu-id="6a1a1-120">terület: az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetések DefaultParameters.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a1a1-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="6a1a1-121">-Location</span></span>
<span data-ttu-id="6a1a1-122">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="6a1a1-123">-Master</span><span class="sxs-lookup"><span data-stu-id="6a1a1-123">-Master</span></span>
<span data-ttu-id="6a1a1-124">A forrás kiszolgálói objektum, amelyből vissza szeretne térni.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-124">The source server object to restore from.</span></span>
<span data-ttu-id="6a1a1-125">A kivitelezéshez tekintse meg a FŐADAT-tulajdonságok megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a1a1-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="6a1a1-126">-MasterName</span></span>
<span data-ttu-id="6a1a1-127">MariaDB-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="6a1a1-128">-Várva</span><span class="sxs-lookup"><span data-stu-id="6a1a1-128">-NoWait</span></span>
<span data-ttu-id="6a1a1-129">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="6a1a1-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a1a1-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="6a1a1-130">-ReplicaName</span></span>
<span data-ttu-id="6a1a1-131">Replika neve.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-131">Replica name.</span></span>

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

### <span data-ttu-id="6a1a1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a1a1-132">-ResourceGroupName</span></span>
<span data-ttu-id="6a1a1-133">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6a1a1-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="6a1a1-134">-Sku</span></span>
<span data-ttu-id="6a1a1-135">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6a1a1-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a1a1-136">-SubscriptionId</span></span>
<span data-ttu-id="6a1a1-137">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a1a1-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="6a1a1-138">-Tag</span></span>
<span data-ttu-id="6a1a1-139">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6a1a1-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a1a1-140">-Confirm</span></span>
<span data-ttu-id="6a1a1-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a1a1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a1a1-142">-WhatIf</span></span>
<span data-ttu-id="6a1a1-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a1a1-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a1a1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1a1-145">CommonParameters</span></span>
<span data-ttu-id="6a1a1-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a1a1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1a1-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1a1-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a1a1-148">INPUTS</span></span>

### <span data-ttu-id="6a1a1-149">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="6a1a1-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="6a1a1-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a1a1-150">OUTPUTS</span></span>

### <span data-ttu-id="6a1a1-151">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="6a1a1-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="6a1a1-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a1a1-152">NOTES</span></span>

<span data-ttu-id="6a1a1-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6a1a1-153">ALIASES</span></span>

<span data-ttu-id="6a1a1-154">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6a1a1-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a1a1-155">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a1a1-156">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a1a1-157">MESTERALAKZAT <IServer> : a forráskiszolgáló-objektum, amelyről vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="6a1a1-158">`Location <String>`: Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="6a1a1-159">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="6a1a1-160">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6a1a1-161">`[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="6a1a1-162">Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="6a1a1-163">`[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="6a1a1-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="6a1a1-164">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="6a1a1-165">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="6a1a1-166">A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="6a1a1-167">`[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="6a1a1-168">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="6a1a1-169">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="6a1a1-170">`[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="6a1a1-171">`[SkuFamily <String>]`: A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="6a1a1-172">`[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="6a1a1-173">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="6a1a1-174">`[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="6a1a1-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="6a1a1-175">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="6a1a1-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="6a1a1-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="6a1a1-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="6a1a1-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="6a1a1-179">`[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="6a1a1-180">`[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="6a1a1-181">`[Version <ServerVersion?>]`: Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="6a1a1-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="6a1a1-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a1a1-182">RELATED LINKS</span></span>

