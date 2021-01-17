---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378404"
---
# <span data-ttu-id="a7eed-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="a7eed-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="a7eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7eed-102">SYNOPSIS</span></span>
<span data-ttu-id="a7eed-103">Új másolatot hoz létre egy meglévő adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="a7eed-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="a7eed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a7eed-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7eed-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a7eed-105">DESCRIPTION</span></span>
<span data-ttu-id="a7eed-106">Új másolatot hoz létre egy meglévő adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="a7eed-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="a7eed-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a7eed-107">EXAMPLES</span></span>

### <span data-ttu-id="a7eed-108">1. példa: Új PostgreSql-kiszolgálói másolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="a7eed-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a7eed-109">Ez a parancsmag létrehoz egy új PostgreSql-kiszolgálói másolatot.</span><span class="sxs-lookup"><span data-stu-id="a7eed-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="a7eed-110">2. példa: Új PostgreSql-kiszolgálói másolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="a7eed-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a7eed-111">Ez a parancsmag létrehoz egy új PostgreSql-kiszolgálói másolatot.</span><span class="sxs-lookup"><span data-stu-id="a7eed-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="a7eed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7eed-112">PARAMETERS</span></span>

### <span data-ttu-id="a7eed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7eed-113">-AsJob</span></span>
<span data-ttu-id="a7eed-114">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="a7eed-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="a7eed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7eed-115">-DefaultProfile</span></span>
<span data-ttu-id="a7eed-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7eed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7eed-117">-Location</span><span class="sxs-lookup"><span data-stu-id="a7eed-117">-Location</span></span>
<span data-ttu-id="a7eed-118">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="a7eed-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="a7eed-119">-Master</span><span class="sxs-lookup"><span data-stu-id="a7eed-119">-Master</span></span>
<span data-ttu-id="a7eed-120">Az a forráskiszolgáló-objektum, amelyből másolatot kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="a7eed-120">The source server object to create replica from.</span></span>
<span data-ttu-id="a7eed-121">Ennek létrehozásához a FŐtulajdonságok MEGJEGYZÉSEK szakaszában és egy kivonattábla létrehozásában is részt kell látnia.</span><span class="sxs-lookup"><span data-stu-id="a7eed-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7eed-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7eed-122">-NoWait</span></span>
<span data-ttu-id="a7eed-123">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="a7eed-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a7eed-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="a7eed-124">-ReplicaName</span></span>
<span data-ttu-id="a7eed-125">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a7eed-125">The name of the server.</span></span>

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

### <span data-ttu-id="a7eed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7eed-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7eed-127">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="a7eed-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a7eed-128">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="a7eed-128">-Sku</span></span>
<span data-ttu-id="a7eed-129">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a7eed-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="a7eed-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7eed-130">-SubscriptionId</span></span>
<span data-ttu-id="a7eed-131">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="a7eed-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a7eed-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7eed-132">-Confirm</span></span>
<span data-ttu-id="a7eed-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a7eed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7eed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7eed-134">-WhatIf</span></span>
<span data-ttu-id="a7eed-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a7eed-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7eed-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7eed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7eed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7eed-137">CommonParameters</span></span>
<span data-ttu-id="a7eed-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7eed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7eed-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7eed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7eed-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7eed-140">INPUTS</span></span>

### <span data-ttu-id="a7eed-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a7eed-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a7eed-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7eed-142">OUTPUTS</span></span>

### <span data-ttu-id="a7eed-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a7eed-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a7eed-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a7eed-144">NOTES</span></span>

<span data-ttu-id="a7eed-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a7eed-145">ALIASES</span></span>

<span data-ttu-id="a7eed-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a7eed-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7eed-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a7eed-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7eed-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7eed-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7eed-149">MESTER: <IServer> Az a forráskiszolgáló-objektum, amelyből másolatot kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="a7eed-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="a7eed-150">`Location <String>`: Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="a7eed-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="a7eed-151">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="a7eed-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="a7eed-152">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="a7eed-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a7eed-153">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="a7eed-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="a7eed-154">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="a7eed-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="a7eed-155">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="a7eed-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="a7eed-156">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="a7eed-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="a7eed-157">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="a7eed-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="a7eed-158">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="a7eed-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="a7eed-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amely azt mutatja, hogy a kiszolgáló engedélyezte-e az infrastruktúra-titkosítást.</span><span class="sxs-lookup"><span data-stu-id="a7eed-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="a7eed-160">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a7eed-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="a7eed-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Csak minimális Tls-verzió legyen érvényes a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="a7eed-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="a7eed-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Hogy engedélyezett-e a nyilvános hálózati hozzáférés ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="a7eed-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="a7eed-163">Az érték megadása nem kötelező, de ha be van engedélyezve, akkor "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a7eed-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="a7eed-164">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a7eed-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="a7eed-165">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="a7eed-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="a7eed-166">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="a7eed-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="a7eed-167">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="a7eed-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="a7eed-168">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a7eed-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="a7eed-169">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="a7eed-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="a7eed-170">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="a7eed-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="a7eed-171">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="a7eed-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="a7eed-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="a7eed-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="a7eed-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy ne a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="a7eed-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="a7eed-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="a7eed-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="a7eed-175">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="a7eed-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="a7eed-176">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="a7eed-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="a7eed-177">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="a7eed-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="a7eed-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7eed-178">RELATED LINKS</span></span>

