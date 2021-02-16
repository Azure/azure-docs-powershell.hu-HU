---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157498"
---
# <span data-ttu-id="cd950-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="cd950-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="cd950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd950-102">SYNOPSIS</span></span>
<span data-ttu-id="cd950-103">A MariaDB kapcsolati karakterláncának lekérte egy adott keretrendszerben.</span><span class="sxs-lookup"><span data-stu-id="cd950-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="cd950-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd950-104">SYNTAX</span></span>

### <span data-ttu-id="cd950-105">ServerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd950-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd950-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="cd950-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd950-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd950-107">DESCRIPTION</span></span>
<span data-ttu-id="cd950-108">A MariaDB kapcsolati karakterláncának lekérte egy adott keretrendszerben.</span><span class="sxs-lookup"><span data-stu-id="cd950-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="cd950-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd950-109">EXAMPLES</span></span>

### <span data-ttu-id="cd950-110">1. példa: A MariaDB kapcsolati karakterláncának lekérte</span><span class="sxs-lookup"><span data-stu-id="cd950-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="cd950-111">Ez a parancs a MariaDB kapcsolati karakterláncot kapja.</span><span class="sxs-lookup"><span data-stu-id="cd950-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="cd950-112">2. példa: A MariaDB kapcsolati karakterláncának lekérte</span><span class="sxs-lookup"><span data-stu-id="cd950-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="cd950-113">Ez a parancs a MariaDB kapcsolati karakterláncot kapja.</span><span class="sxs-lookup"><span data-stu-id="cd950-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="cd950-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd950-114">PARAMETERS</span></span>

### <span data-ttu-id="cd950-115">-Client</span><span class="sxs-lookup"><span data-stu-id="cd950-115">-Client</span></span>
<span data-ttu-id="cd950-116">Ügyféltípus csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="cd950-116">Connect client type</span></span>

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

### <span data-ttu-id="cd950-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd950-117">-DefaultProfile</span></span>
<span data-ttu-id="cd950-118">régió DefaultParameters Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd950-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd950-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd950-119">-InputObject</span></span>
<span data-ttu-id="cd950-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cd950-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd950-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd950-121">-Name</span></span>
<span data-ttu-id="cd950-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="cd950-122">The name of the server.</span></span>

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

### <span data-ttu-id="cd950-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd950-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd950-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd950-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="cd950-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd950-125">-SubscriptionId</span></span>
<span data-ttu-id="cd950-126">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része</span><span class="sxs-lookup"><span data-stu-id="cd950-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="cd950-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd950-127">CommonParameters</span></span>
<span data-ttu-id="cd950-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd950-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd950-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd950-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd950-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd950-130">INPUTS</span></span>

### <span data-ttu-id="cd950-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="cd950-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="cd950-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd950-132">OUTPUTS</span></span>

### <span data-ttu-id="cd950-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cd950-133">System.String</span></span>

## <span data-ttu-id="cd950-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd950-134">NOTES</span></span>

<span data-ttu-id="cd950-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cd950-135">ALIASES</span></span>

<span data-ttu-id="cd950-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="cd950-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd950-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="cd950-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd950-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd950-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd950-139">INPUTOBJECT: <IServer> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="cd950-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="cd950-140">`Location <String>`: Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="cd950-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="cd950-141">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="cd950-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="cd950-142">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="cd950-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cd950-143">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="cd950-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="cd950-144">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="cd950-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="cd950-145">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="cd950-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="cd950-146">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="cd950-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="cd950-147">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="cd950-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="cd950-148">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="cd950-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="cd950-149">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd950-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="cd950-150">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="cd950-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="cd950-151">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="cd950-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="cd950-152">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="cd950-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="cd950-153">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="cd950-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="cd950-154">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cd950-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="cd950-155">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="cd950-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="cd950-156">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="cd950-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="cd950-157">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="cd950-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="cd950-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="cd950-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="cd950-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy ne a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="cd950-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="cd950-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="cd950-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="cd950-161">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="cd950-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="cd950-162">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="cd950-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="cd950-163">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="cd950-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="cd950-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd950-164">RELATED LINKS</span></span>

