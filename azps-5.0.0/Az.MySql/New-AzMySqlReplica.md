---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 5e5d83266dd86ccaf0bd5037c6af01f8b1846a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195101"
---
# <span data-ttu-id="48cd2-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="48cd2-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="48cd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="48cd2-103">Új replikát hoz létre egy meglévő adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="48cd2-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="48cd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48cd2-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="48cd2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="48cd2-106">Új replikát hoz létre egy meglévő adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="48cd2-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="48cd2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="48cd2-108">Példa 1: új MySql kiszolgálói replika létrehozása</span><span class="sxs-lookup"><span data-stu-id="48cd2-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="48cd2-109">Ez a parancsmag létrehoz egy új MySql-kiszolgáló replikát.</span><span class="sxs-lookup"><span data-stu-id="48cd2-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="48cd2-110">2. példa: új MySql Server-replika létrehozása</span><span class="sxs-lookup"><span data-stu-id="48cd2-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="48cd2-111">Ezt a parancsmagot a paraméter-főkiszolgáló (inputobject) nevű parancsmag hozza létre új, MySql kiszolgálói replikát.</span><span class="sxs-lookup"><span data-stu-id="48cd2-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="48cd2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48cd2-112">PARAMETERS</span></span>

### <span data-ttu-id="48cd2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48cd2-113">-AsJob</span></span>
<span data-ttu-id="48cd2-114">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="48cd2-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="48cd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cd2-115">-DefaultProfile</span></span>
<span data-ttu-id="48cd2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48cd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48cd2-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="48cd2-117">-Location</span></span>
<span data-ttu-id="48cd2-118">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="48cd2-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="48cd2-119">-Master</span><span class="sxs-lookup"><span data-stu-id="48cd2-119">-Master</span></span>
<span data-ttu-id="48cd2-120">A Source Server objektum a replika létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="48cd2-120">The source server object to create replica from.</span></span>
<span data-ttu-id="48cd2-121">A kivitelezéshez tekintse meg a FŐADAT-tulajdonságok megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="48cd2-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48cd2-122">-Várva</span><span class="sxs-lookup"><span data-stu-id="48cd2-122">-NoWait</span></span>
<span data-ttu-id="48cd2-123">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="48cd2-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="48cd2-124">– Replika</span><span class="sxs-lookup"><span data-stu-id="48cd2-124">-Replica</span></span>
<span data-ttu-id="48cd2-125">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="48cd2-125">The name of the server.</span></span>

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

### <span data-ttu-id="48cd2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48cd2-126">-ResourceGroupName</span></span>
<span data-ttu-id="48cd2-127">Az erőforrást tartalmazó erőforráscsoport neve az Azure Resource Manager API-ból vagy a portálról szerzi be ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="48cd2-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="48cd2-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="48cd2-128">-Sku</span></span>
<span data-ttu-id="48cd2-129">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="48cd2-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="48cd2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48cd2-130">-SubscriptionId</span></span>
<span data-ttu-id="48cd2-131">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="48cd2-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="48cd2-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48cd2-132">-Confirm</span></span>
<span data-ttu-id="48cd2-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48cd2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48cd2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48cd2-134">-WhatIf</span></span>
<span data-ttu-id="48cd2-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48cd2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48cd2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48cd2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48cd2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cd2-137">CommonParameters</span></span>
<span data-ttu-id="48cd2-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48cd2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cd2-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48cd2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cd2-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48cd2-140">INPUTS</span></span>

### <span data-ttu-id="48cd2-141">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="48cd2-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="48cd2-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48cd2-142">OUTPUTS</span></span>

### <span data-ttu-id="48cd2-143">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="48cd2-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="48cd2-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48cd2-144">NOTES</span></span>

<span data-ttu-id="48cd2-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="48cd2-145">ALIASES</span></span>

<span data-ttu-id="48cd2-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="48cd2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48cd2-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="48cd2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48cd2-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="48cd2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48cd2-149">MESTERALAKZAT <IServer> : a Source Server objektum, amelyből replika hozható létre.</span><span class="sxs-lookup"><span data-stu-id="48cd2-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="48cd2-150">`Location <String>`: Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="48cd2-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="48cd2-151">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="48cd2-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="48cd2-152">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="48cd2-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="48cd2-153">`[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="48cd2-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="48cd2-154">Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="48cd2-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="48cd2-155">`[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="48cd2-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="48cd2-156">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.</span><span class="sxs-lookup"><span data-stu-id="48cd2-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="48cd2-157">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="48cd2-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="48cd2-158">A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.</span><span class="sxs-lookup"><span data-stu-id="48cd2-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="48cd2-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amelyen látható, hogy a kiszolgáló engedélyezve van-e az infrastruktúra titkosítása.</span><span class="sxs-lookup"><span data-stu-id="48cd2-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="48cd2-160">`[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.</span><span class="sxs-lookup"><span data-stu-id="48cd2-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="48cd2-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Minimális TLS-verzió érvényesítése a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="48cd2-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="48cd2-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: A kiszolgálón engedélyezve van-e a nyilvános hálózatokhoz való hozzáférés.</span><span class="sxs-lookup"><span data-stu-id="48cd2-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="48cd2-163">Az érték nem kötelező, de ha be van kapcsolva, "engedélyezve" vagy "Letiltva" állapotban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="48cd2-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="48cd2-164">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.</span><span class="sxs-lookup"><span data-stu-id="48cd2-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="48cd2-165">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="48cd2-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="48cd2-166">`[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="48cd2-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="48cd2-167">`[SkuFamily <String>]`: A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="48cd2-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="48cd2-168">`[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="48cd2-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="48cd2-169">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.</span><span class="sxs-lookup"><span data-stu-id="48cd2-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="48cd2-170">`[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="48cd2-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="48cd2-171">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="48cd2-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="48cd2-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="48cd2-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="48cd2-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="48cd2-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="48cd2-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="48cd2-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="48cd2-175">`[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="48cd2-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="48cd2-176">`[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="48cd2-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="48cd2-177">`[Version <ServerVersion?>]`: Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="48cd2-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="48cd2-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48cd2-178">RELATED LINKS</span></span>

