---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025268"
---
# <span data-ttu-id="2c606-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="2c606-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="2c606-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c606-102">SYNOPSIS</span></span>
<span data-ttu-id="2c606-103">A MariaDB kapcsolati karakterláncának beszerzése egy adott keretrendszerben.</span><span class="sxs-lookup"><span data-stu-id="2c606-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="2c606-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c606-104">SYNTAX</span></span>

### <span data-ttu-id="2c606-105">Kiszolgálónév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c606-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c606-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="2c606-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c606-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c606-107">DESCRIPTION</span></span>
<span data-ttu-id="2c606-108">A MariaDB kapcsolati karakterláncának beszerzése egy adott keretrendszerben.</span><span class="sxs-lookup"><span data-stu-id="2c606-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="2c606-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2c606-109">EXAMPLES</span></span>

### <span data-ttu-id="2c606-110">Példa 1: a MariaDB kapcsolati karakterláncának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2c606-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="2c606-111">Ez a parancs a MariaDB kapcsolati karakterláncát kapja.</span><span class="sxs-lookup"><span data-stu-id="2c606-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="2c606-112">2. példa: a MariaDB kapcsolati karakterláncának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2c606-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="2c606-113">Ez a parancs a MariaDB kapcsolati karakterláncát kapja.</span><span class="sxs-lookup"><span data-stu-id="2c606-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="2c606-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c606-114">PARAMETERS</span></span>

### <span data-ttu-id="2c606-115">-Client</span><span class="sxs-lookup"><span data-stu-id="2c606-115">-Client</span></span>
<span data-ttu-id="2c606-116">Ügyfél típusának csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="2c606-116">Connect client type</span></span>

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

### <span data-ttu-id="2c606-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c606-117">-DefaultProfile</span></span>
<span data-ttu-id="2c606-118">terület: az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetések DefaultParameters.</span><span class="sxs-lookup"><span data-stu-id="2c606-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c606-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c606-119">-InputObject</span></span>
<span data-ttu-id="2c606-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c606-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c606-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c606-121">-Name</span></span>
<span data-ttu-id="2c606-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="2c606-122">The name of the server.</span></span>

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

### <span data-ttu-id="2c606-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c606-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c606-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2c606-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="2c606-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c606-125">-SubscriptionId</span></span>
<span data-ttu-id="2c606-126">Az előfizetési azonosító az összes szolgáltatási hívás URI-ja része</span><span class="sxs-lookup"><span data-stu-id="2c606-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="2c606-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c606-127">CommonParameters</span></span>
<span data-ttu-id="2c606-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c606-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c606-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c606-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c606-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c606-130">INPUTS</span></span>

### <span data-ttu-id="2c606-131">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="2c606-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="2c606-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c606-132">OUTPUTS</span></span>

### <span data-ttu-id="2c606-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2c606-133">System.String</span></span>

## <span data-ttu-id="2c606-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c606-134">NOTES</span></span>

<span data-ttu-id="2c606-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2c606-135">ALIASES</span></span>

<span data-ttu-id="2c606-136">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="2c606-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2c606-137">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2c606-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c606-138">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="2c606-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2c606-139">INPUTOBJECT <IServer> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="2c606-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="2c606-140">`Location <String>`: Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="2c606-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="2c606-141">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="2c606-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="2c606-142">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="2c606-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2c606-143">`[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2c606-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="2c606-144">Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="2c606-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="2c606-145">`[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="2c606-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="2c606-146">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.</span><span class="sxs-lookup"><span data-stu-id="2c606-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="2c606-147">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="2c606-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="2c606-148">A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.</span><span class="sxs-lookup"><span data-stu-id="2c606-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="2c606-149">`[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c606-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="2c606-150">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.</span><span class="sxs-lookup"><span data-stu-id="2c606-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="2c606-151">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="2c606-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="2c606-152">`[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2c606-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="2c606-153">`[SkuFamily <String>]`: A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="2c606-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="2c606-154">`[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2c606-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="2c606-155">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.</span><span class="sxs-lookup"><span data-stu-id="2c606-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="2c606-156">`[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="2c606-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="2c606-157">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="2c606-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="2c606-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2c606-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="2c606-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="2c606-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="2c606-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2c606-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="2c606-161">`[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2c606-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="2c606-162">`[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="2c606-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="2c606-163">`[Version <ServerVersion?>]`: Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="2c606-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="2c606-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c606-164">RELATED LINKS</span></span>

