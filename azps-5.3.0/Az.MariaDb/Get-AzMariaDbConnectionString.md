---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380728"
---
# <span data-ttu-id="39265-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="39265-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="39265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39265-102">SYNOPSIS</span></span>
<span data-ttu-id="39265-103">A MariaDB kapcsolati karakterláncának lekérte egy adott keretrendszerben.</span><span class="sxs-lookup"><span data-stu-id="39265-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="39265-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39265-104">SYNTAX</span></span>

### <span data-ttu-id="39265-105">ServerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39265-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39265-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="39265-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="39265-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39265-107">DESCRIPTION</span></span>
<span data-ttu-id="39265-108">A MariaDB kapcsolati karakterláncának lekérte egy adott keretrendszerben.</span><span class="sxs-lookup"><span data-stu-id="39265-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="39265-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39265-109">EXAMPLES</span></span>

### <span data-ttu-id="39265-110">1. példa: A MariaDB kapcsolati karakterláncának lekérte</span><span class="sxs-lookup"><span data-stu-id="39265-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="39265-111">Ez a parancs a MariaDB kapcsolati karakterláncot kapja.</span><span class="sxs-lookup"><span data-stu-id="39265-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="39265-112">2. példa: A MariaDB kapcsolati karakterláncának lekérte</span><span class="sxs-lookup"><span data-stu-id="39265-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="39265-113">Ez a parancs a MariaDB kapcsolati karakterláncot kapja.</span><span class="sxs-lookup"><span data-stu-id="39265-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="39265-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39265-114">PARAMETERS</span></span>

### <span data-ttu-id="39265-115">-Client</span><span class="sxs-lookup"><span data-stu-id="39265-115">-Client</span></span>
<span data-ttu-id="39265-116">Ügyféltípus csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="39265-116">Connect client type</span></span>

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

### <span data-ttu-id="39265-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39265-117">-DefaultProfile</span></span>
<span data-ttu-id="39265-118">régió DefaultParameters Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39265-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39265-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39265-119">-InputObject</span></span>
<span data-ttu-id="39265-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="39265-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39265-121">-Name</span><span class="sxs-lookup"><span data-stu-id="39265-121">-Name</span></span>
<span data-ttu-id="39265-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="39265-122">The name of the server.</span></span>

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

### <span data-ttu-id="39265-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39265-123">-ResourceGroupName</span></span>
<span data-ttu-id="39265-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39265-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="39265-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39265-125">-SubscriptionId</span></span>
<span data-ttu-id="39265-126">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része</span><span class="sxs-lookup"><span data-stu-id="39265-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="39265-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39265-127">CommonParameters</span></span>
<span data-ttu-id="39265-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39265-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39265-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39265-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39265-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39265-130">INPUTS</span></span>

### <span data-ttu-id="39265-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="39265-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="39265-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39265-132">OUTPUTS</span></span>

### <span data-ttu-id="39265-133">System.String</span><span class="sxs-lookup"><span data-stu-id="39265-133">System.String</span></span>

## <span data-ttu-id="39265-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39265-134">NOTES</span></span>

<span data-ttu-id="39265-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="39265-135">ALIASES</span></span>

<span data-ttu-id="39265-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="39265-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39265-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="39265-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39265-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39265-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39265-139">INPUTOBJECT: <IServer> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="39265-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="39265-140">`Location <String>`: Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="39265-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="39265-141">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="39265-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="39265-142">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="39265-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="39265-143">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="39265-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="39265-144">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="39265-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="39265-145">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="39265-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="39265-146">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="39265-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="39265-147">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="39265-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="39265-148">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="39265-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="39265-149">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="39265-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="39265-150">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="39265-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="39265-151">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="39265-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="39265-152">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="39265-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="39265-153">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="39265-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="39265-154">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="39265-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="39265-155">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="39265-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="39265-156">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="39265-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="39265-157">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="39265-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="39265-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="39265-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="39265-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy a nem kiszolgálói biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="39265-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="39265-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="39265-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="39265-161">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="39265-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="39265-162">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="39265-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="39265-163">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="39265-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="39265-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39265-164">RELATED LINKS</span></span>

