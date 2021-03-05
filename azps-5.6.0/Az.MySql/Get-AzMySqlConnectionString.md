---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: c85ece43045144d0befd6a6ed1e7ac1d7431796f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010453"
---
# <span data-ttu-id="9cf6e-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="9cf6e-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="9cf6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cf6e-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf6e-103">Szerezze be a kapcsolati karakterláncot az ügyfélkapcsolatszolgáltatónak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="9cf6e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cf6e-104">SYNTAX</span></span>

### <span data-ttu-id="9cf6e-105">Bejő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cf6e-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9cf6e-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9cf6e-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf6e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cf6e-107">DESCRIPTION</span></span>
<span data-ttu-id="9cf6e-108">Szerezze be a kapcsolati karakterláncot az ügyfélkapcsolatszolgáltatónak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="9cf6e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cf6e-109">EXAMPLES</span></span>

### <span data-ttu-id="9cf6e-110">1. példa: A MySql-kiszolgáló kapcsolati karakterláncának lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="9cf6e-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="9cf6e-111">Ez a parancsmag a MySql-kiszolgáló kapcsolati karakterláncát erőforráscsoport és kiszolgálónév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="9cf6e-112">2. példa: A MySql-kiszolgáló kapcsolati karakterláncának lekérte identitás szerint</span><span class="sxs-lookup"><span data-stu-id="9cf6e-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="9cf6e-113">Ez a parancsmag identitás szerint kapja meg a MySql-kiszolgáló kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="9cf6e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cf6e-114">PARAMETERS</span></span>

### <span data-ttu-id="9cf6e-115">-Client</span><span class="sxs-lookup"><span data-stu-id="9cf6e-115">-Client</span></span>
<span data-ttu-id="9cf6e-116">Ügyfélkapcsolat-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-116">Client connection provider.</span></span>

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

### <span data-ttu-id="9cf6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf6e-117">-DefaultProfile</span></span>
<span data-ttu-id="9cf6e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cf6e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cf6e-119">-InputObject</span></span>
<span data-ttu-id="9cf6e-120">A kapcsolati karakterlánc kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-120">The server for the connection string.</span></span>
<span data-ttu-id="9cf6e-121">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf6e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9cf6e-122">-Name</span></span>
<span data-ttu-id="9cf6e-123">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-123">The name of the server.</span></span>

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

### <span data-ttu-id="9cf6e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf6e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9cf6e-125">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9cf6e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cf6e-126">-SubscriptionId</span></span>
<span data-ttu-id="9cf6e-127">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9cf6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf6e-128">CommonParameters</span></span>
<span data-ttu-id="9cf6e-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf6e-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cf6e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf6e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cf6e-131">INPUTS</span></span>

### <span data-ttu-id="9cf6e-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="9cf6e-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="9cf6e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cf6e-133">OUTPUTS</span></span>

### <span data-ttu-id="9cf6e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9cf6e-134">System.String</span></span>

## <span data-ttu-id="9cf6e-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cf6e-135">NOTES</span></span>

<span data-ttu-id="9cf6e-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9cf6e-136">ALIASES</span></span>

<span data-ttu-id="9cf6e-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9cf6e-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9cf6e-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cf6e-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9cf6e-140">INPUTOBJECT: <IServer> A kapcsolati karakterlánc kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-140">INPUTOBJECT <IServer>: The server for the connection string.</span></span>
  - <span data-ttu-id="9cf6e-141">`Location <String>`: Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="9cf6e-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="9cf6e-142">`[Tag <ITrackedResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-142">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="9cf6e-143">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9cf6e-144">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="9cf6e-145">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="9cf6e-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="9cf6e-146">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="9cf6e-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="9cf6e-147">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="9cf6e-148">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="9cf6e-149">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="9cf6e-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amely azt mutatja, hogy a kiszolgáló engedélyezte-e az infrastruktúra-titkosítást.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="9cf6e-151">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="9cf6e-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Csak minimális Tls-verzió legyen érvényes a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="9cf6e-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Hogy engedélyezett-e a nyilvános hálózati hozzáférés ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="9cf6e-154">Az érték megadása nem kötelező, de ha be van engedélyezve, akkor "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="9cf6e-155">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="9cf6e-156">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="9cf6e-157">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="9cf6e-158">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="9cf6e-159">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="9cf6e-160">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="9cf6e-161">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="9cf6e-162">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="9cf6e-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="9cf6e-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy ne a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="9cf6e-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="9cf6e-166">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="9cf6e-167">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="9cf6e-168">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="9cf6e-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="9cf6e-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cf6e-169">RELATED LINKS</span></span>

