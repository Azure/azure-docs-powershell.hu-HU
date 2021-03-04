---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: 5aed092485bf90418f467a2857716496f2979454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936697"
---
# <span data-ttu-id="eb68b-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="eb68b-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="eb68b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb68b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb68b-103">Új másolatot hoz létre egy meglévő adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="eb68b-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="eb68b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb68b-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eb68b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb68b-105">DESCRIPTION</span></span>
<span data-ttu-id="eb68b-106">Új másolatot hoz létre egy meglévő adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="eb68b-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="eb68b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb68b-107">EXAMPLES</span></span>

### <span data-ttu-id="eb68b-108">1. példa: Új PostgreSql-kiszolgálói másolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="eb68b-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="eb68b-109">Ez a parancsmag létrehoz egy új PostgreSql-kiszolgálói másolatot.</span><span class="sxs-lookup"><span data-stu-id="eb68b-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="eb68b-110">2. példa: Új PostgreSql-kiszolgálói másolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="eb68b-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="eb68b-111">Ez a parancsmag létrehoz egy új PostgreSql-kiszolgálói másolatot.</span><span class="sxs-lookup"><span data-stu-id="eb68b-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="eb68b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb68b-112">PARAMETERS</span></span>

### <span data-ttu-id="eb68b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb68b-113">-AsJob</span></span>
<span data-ttu-id="eb68b-114">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="eb68b-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="eb68b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb68b-115">-DefaultProfile</span></span>
<span data-ttu-id="eb68b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb68b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb68b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="eb68b-117">-Location</span></span>
<span data-ttu-id="eb68b-118">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="eb68b-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="eb68b-119">-Master</span><span class="sxs-lookup"><span data-stu-id="eb68b-119">-Master</span></span>
<span data-ttu-id="eb68b-120">Az a forráskiszolgáló-objektum, amelyből másolatot kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="eb68b-120">The source server object to create replica from.</span></span>
<span data-ttu-id="eb68b-121">Ennek létrehozásához a FŐtulajdonságok MEGJEGYZÉSEK szakaszában és egy kivonattábla létrehozásában is részt kell látnia.</span><span class="sxs-lookup"><span data-stu-id="eb68b-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb68b-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eb68b-122">-NoWait</span></span>
<span data-ttu-id="eb68b-123">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="eb68b-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="eb68b-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="eb68b-124">-ReplicaName</span></span>
<span data-ttu-id="eb68b-125">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="eb68b-125">The name of the server.</span></span>

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

### <span data-ttu-id="eb68b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb68b-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb68b-127">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="eb68b-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="eb68b-128">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="eb68b-128">-Sku</span></span>
<span data-ttu-id="eb68b-129">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="eb68b-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="eb68b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb68b-130">-SubscriptionId</span></span>
<span data-ttu-id="eb68b-131">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="eb68b-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="eb68b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb68b-132">-Confirm</span></span>
<span data-ttu-id="eb68b-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eb68b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb68b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb68b-134">-WhatIf</span></span>
<span data-ttu-id="eb68b-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eb68b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb68b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb68b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb68b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb68b-137">CommonParameters</span></span>
<span data-ttu-id="eb68b-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb68b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb68b-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb68b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb68b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb68b-140">INPUTS</span></span>

### <span data-ttu-id="eb68b-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="eb68b-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="eb68b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb68b-142">OUTPUTS</span></span>

### <span data-ttu-id="eb68b-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="eb68b-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="eb68b-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb68b-144">NOTES</span></span>

<span data-ttu-id="eb68b-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eb68b-145">ALIASES</span></span>

<span data-ttu-id="eb68b-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="eb68b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb68b-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="eb68b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb68b-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb68b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb68b-149">MESTER: <IServer> Az a forráskiszolgáló-objektum, amelyből másolatot kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="eb68b-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="eb68b-150">`Location <String>`: Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="eb68b-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="eb68b-151">`[Tag <ITrackedResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="eb68b-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="eb68b-152">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="eb68b-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="eb68b-153">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="eb68b-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="eb68b-154">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="eb68b-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="eb68b-155">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="eb68b-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="eb68b-156">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="eb68b-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="eb68b-157">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="eb68b-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="eb68b-158">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="eb68b-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="eb68b-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amely azt mutatja, hogy a kiszolgáló engedélyezte-e az infrastruktúra-titkosítást.</span><span class="sxs-lookup"><span data-stu-id="eb68b-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="eb68b-160">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb68b-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="eb68b-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Csak minimális Tls-verzió legyen érvényes a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="eb68b-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="eb68b-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Hogy engedélyezett-e a nyilvános hálózati hozzáférés ehhez a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="eb68b-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="eb68b-163">Az érték megadása nem kötelező, de ha be van engedélyezve, akkor "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="eb68b-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="eb68b-164">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="eb68b-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="eb68b-165">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="eb68b-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="eb68b-166">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="eb68b-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="eb68b-167">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="eb68b-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="eb68b-168">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="eb68b-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="eb68b-169">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="eb68b-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="eb68b-170">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="eb68b-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="eb68b-171">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="eb68b-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="eb68b-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="eb68b-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="eb68b-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy ne a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="eb68b-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="eb68b-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="eb68b-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="eb68b-175">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="eb68b-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="eb68b-176">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="eb68b-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="eb68b-177">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="eb68b-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="eb68b-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb68b-178">RELATED LINKS</span></span>

