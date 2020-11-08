---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024494"
---
# <span data-ttu-id="bd916-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="bd916-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="bd916-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd916-102">SYNOPSIS</span></span>
<span data-ttu-id="bd916-103">A kapcsolati karakterlánc beszerzése az ügyfél-kapcsolat szolgáltatója szerint.</span><span class="sxs-lookup"><span data-stu-id="bd916-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bd916-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd916-104">SYNTAX</span></span>

### <span data-ttu-id="bd916-105">Get (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd916-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bd916-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bd916-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd916-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd916-107">DESCRIPTION</span></span>
<span data-ttu-id="bd916-108">A kapcsolati karakterlánc beszerzése az ügyfél-kapcsolat szolgáltatója szerint.</span><span class="sxs-lookup"><span data-stu-id="bd916-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bd916-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bd916-109">EXAMPLES</span></span>

### <span data-ttu-id="bd916-110">Példa 1: PostgreSql-kiszolgáló kapcsolódási karakterláncának beolvasása az erőforráscsoport és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="bd916-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="bd916-111">Ez a parancsmag a PostgreSql Server Connection karakterláncot az erőforráscsoport és a kiszolgálónév alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bd916-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="bd916-112">2. példa: PostgreSql-kiszolgáló kapcsolati karakterláncának beolvasása identitás szerint</span><span class="sxs-lookup"><span data-stu-id="bd916-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="bd916-113">Ez a parancsmag identitással kapja meg a PostgreSql-kiszolgáló kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="bd916-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="bd916-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd916-114">PARAMETERS</span></span>

### <span data-ttu-id="bd916-115">-Client</span><span class="sxs-lookup"><span data-stu-id="bd916-115">-Client</span></span>
<span data-ttu-id="bd916-116">Ügyfél-kapcsolat szolgáltatója.</span><span class="sxs-lookup"><span data-stu-id="bd916-116">Client connection provider.</span></span>

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

### <span data-ttu-id="bd916-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd916-117">-DefaultProfile</span></span>
<span data-ttu-id="bd916-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd916-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd916-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd916-119">-InputObject</span></span>
<span data-ttu-id="bd916-120">A Source Server objektum a replika létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="bd916-120">The source server object to create replica from.</span></span>
<span data-ttu-id="bd916-121">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="bd916-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd916-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd916-122">-Name</span></span>
<span data-ttu-id="bd916-123">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="bd916-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd916-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd916-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd916-125">Az erőforrást tartalmazó erőforráscsoport neve az Azure Resource Manager API-ból vagy a portálról szerzi be ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="bd916-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd916-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd916-126">-SubscriptionId</span></span>
<span data-ttu-id="bd916-127">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="bd916-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd916-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd916-128">CommonParameters</span></span>
<span data-ttu-id="bd916-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd916-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd916-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bd916-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd916-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd916-131">INPUTS</span></span>

### <span data-ttu-id="bd916-132">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="bd916-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bd916-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd916-133">OUTPUTS</span></span>

### <span data-ttu-id="bd916-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bd916-134">System.String</span></span>

## <span data-ttu-id="bd916-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd916-135">NOTES</span></span>

<span data-ttu-id="bd916-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bd916-136">ALIASES</span></span>

<span data-ttu-id="bd916-137">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="bd916-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd916-138">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="bd916-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd916-139">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="bd916-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd916-140">INPUTOBJECT <IServer> : a Source Server objektum, amelyből replika hozható létre.</span><span class="sxs-lookup"><span data-stu-id="bd916-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="bd916-141">`Location <String>`: Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="bd916-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="bd916-142">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="bd916-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="bd916-143">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="bd916-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bd916-144">`[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="bd916-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="bd916-145">Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="bd916-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="bd916-146">`[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="bd916-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="bd916-147">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.</span><span class="sxs-lookup"><span data-stu-id="bd916-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="bd916-148">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="bd916-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="bd916-149">A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.</span><span class="sxs-lookup"><span data-stu-id="bd916-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="bd916-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amelyen látható, hogy a kiszolgáló engedélyezve van-e az infrastruktúra titkosítása.</span><span class="sxs-lookup"><span data-stu-id="bd916-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="bd916-151">`[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd916-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="bd916-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Minimális TLS-verzió érvényesítése a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="bd916-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="bd916-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: A kiszolgálón engedélyezve van-e a nyilvános hálózatokhoz való hozzáférés.</span><span class="sxs-lookup"><span data-stu-id="bd916-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="bd916-154">Az érték nem kötelező, de ha be van kapcsolva, "engedélyezve" vagy "Letiltva" állapotban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bd916-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="bd916-155">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.</span><span class="sxs-lookup"><span data-stu-id="bd916-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="bd916-156">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="bd916-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="bd916-157">`[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bd916-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="bd916-158">`[SkuFamily <String>]`: A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="bd916-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="bd916-159">`[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bd916-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="bd916-160">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.</span><span class="sxs-lookup"><span data-stu-id="bd916-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="bd916-161">`[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="bd916-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="bd916-162">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="bd916-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="bd916-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="bd916-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="bd916-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="bd916-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="bd916-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="bd916-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="bd916-166">`[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="bd916-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="bd916-167">`[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="bd916-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="bd916-168">`[Version <ServerVersion?>]`: Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="bd916-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="bd916-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd916-169">RELATED LINKS</span></span>

