---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 092e109de5fd38fcad924886f55d918a91e12aed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003894"
---
# <span data-ttu-id="aaebf-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="aaebf-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="aaebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaebf-102">SYNOPSIS</span></span>
<span data-ttu-id="aaebf-103">Visszaállíthatja a MariaDB-t egy meglévő MariaDB-ről.</span><span class="sxs-lookup"><span data-stu-id="aaebf-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="aaebf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aaebf-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aaebf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aaebf-105">DESCRIPTION</span></span>
<span data-ttu-id="aaebf-106">Visszaállíthatja a MariaDB-t egy meglévő MariaDB-ről.</span><span class="sxs-lookup"><span data-stu-id="aaebf-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="aaebf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aaebf-107">EXAMPLES</span></span>

### <span data-ttu-id="aaebf-108">1. példa: A PointInTime MariaDB visszaállítása kiszolgálónév szerint.</span><span class="sxs-lookup"><span data-stu-id="aaebf-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="aaebf-109">Ez a parancs visszaállít egy PointInTime MariaDB-t kiszolgálónév szerint.</span><span class="sxs-lookup"><span data-stu-id="aaebf-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="aaebf-110">2. példa: PointInTime MariaDB-objektum visszaállítása kiszolgálói objektum alapján</span><span class="sxs-lookup"><span data-stu-id="aaebf-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="aaebf-111">Ez a parancs visszaállít egy PointInTime MariaDB kiszolgálói objektumot.</span><span class="sxs-lookup"><span data-stu-id="aaebf-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="aaebf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaebf-112">PARAMETERS</span></span>

### <span data-ttu-id="aaebf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaebf-113">-AsJob</span></span>
<span data-ttu-id="aaebf-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="aaebf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="aaebf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaebf-115">-DefaultProfile</span></span>
<span data-ttu-id="aaebf-116">régió DefaultParameters Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaebf-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaebf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaebf-117">-InputObject</span></span>
<span data-ttu-id="aaebf-118">Az a forráskiszolgáló-objektum, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="aaebf-118">The source server object to restore from.</span></span>
<span data-ttu-id="aaebf-119">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="aaebf-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaebf-120">-Location</span><span class="sxs-lookup"><span data-stu-id="aaebf-120">-Location</span></span>
<span data-ttu-id="aaebf-121">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="aaebf-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="aaebf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aaebf-122">-Name</span></span>
<span data-ttu-id="aaebf-123">Az a kiszolgálónév, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="aaebf-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="aaebf-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aaebf-124">-NoWait</span></span>
<span data-ttu-id="aaebf-125">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="aaebf-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aaebf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaebf-126">-ResourceGroupName</span></span>
<span data-ttu-id="aaebf-127">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aaebf-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aaebf-128">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="aaebf-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aaebf-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="aaebf-129">-RestorePointInTime</span></span>
<span data-ttu-id="aaebf-130">region PointInTimeRestore The location the resource resides in.</span><span class="sxs-lookup"><span data-stu-id="aaebf-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaebf-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aaebf-131">-ServerName</span></span>
<span data-ttu-id="aaebf-132">A forráskiszolgáló neve, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="aaebf-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="aaebf-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaebf-133">-SubscriptionId</span></span>
<span data-ttu-id="aaebf-134">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="aaebf-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aaebf-135">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="aaebf-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aaebf-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="aaebf-136">-Tag</span></span>
<span data-ttu-id="aaebf-137">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="aaebf-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="aaebf-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaebf-138">-Confirm</span></span>
<span data-ttu-id="aaebf-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aaebf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaebf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaebf-140">-WhatIf</span></span>
<span data-ttu-id="aaebf-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aaebf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaebf-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aaebf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaebf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaebf-143">CommonParameters</span></span>
<span data-ttu-id="aaebf-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaebf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaebf-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaebf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaebf-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaebf-146">INPUTS</span></span>

### <span data-ttu-id="aaebf-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="aaebf-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="aaebf-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaebf-148">OUTPUTS</span></span>

### <span data-ttu-id="aaebf-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="aaebf-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="aaebf-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aaebf-150">NOTES</span></span>

<span data-ttu-id="aaebf-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aaebf-151">ALIASES</span></span>

<span data-ttu-id="aaebf-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="aaebf-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aaebf-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="aaebf-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaebf-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aaebf-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aaebf-155">INPUTOBJECT: Az a <IServer> forráskiszolgáló-objektum, amelyből vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="aaebf-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="aaebf-156">`Location <String>`: Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="aaebf-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="aaebf-157">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="aaebf-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="aaebf-158">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="aaebf-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="aaebf-159">`[AdministratorLogin <String>]`: A kiszolgáló rendszergazdai bejelentkezési neve.</span><span class="sxs-lookup"><span data-stu-id="aaebf-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="aaebf-160">Csak a kiszolgáló létrehozásakor lehet megadni (és a létrehozáshoz szükséges).</span><span class="sxs-lookup"><span data-stu-id="aaebf-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="aaebf-161">`[EarliestRestoreDate <DateTime?>]`: Legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="aaebf-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="aaebf-162">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljes tartományneve.</span><span class="sxs-lookup"><span data-stu-id="aaebf-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="aaebf-163">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="aaebf-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="aaebf-164">Ezt a "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="aaebf-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="aaebf-165">`[MasterServerId <String>]`: A replikakiszolgáló főkiszolgáló-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aaebf-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="aaebf-166">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által lehetséges replikapéldányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="aaebf-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="aaebf-167">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="aaebf-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="aaebf-168">`[SkuCapacity <Int32?>]`: A kiszolgáló számítási egységeit képviselő fel-/kiskála kapacitás.</span><span class="sxs-lookup"><span data-stu-id="aaebf-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="aaebf-169">`[SkuFamily <String>]`: A hardver család.</span><span class="sxs-lookup"><span data-stu-id="aaebf-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="aaebf-170">`[SkuName <String>]`: A termékváltozat neve, általában a tier + family + cores (szint + család + cores) neve, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="aaebf-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="aaebf-171">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezendő méretkód.</span><span class="sxs-lookup"><span data-stu-id="aaebf-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="aaebf-172">`[SkuTier <SkuTier?>]`: Az adott termékváltozat rétege, például alapszintű.</span><span class="sxs-lookup"><span data-stu-id="aaebf-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="aaebf-173">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="aaebf-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="aaebf-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági mentési megőrzési napok a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="aaebf-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="aaebf-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a georedundáns vagy ne a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="aaebf-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="aaebf-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="aaebf-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="aaebf-177">`[StorageProfileStorageMb <Int32?>]`: A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="aaebf-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="aaebf-178">`[UserVisibleState <ServerState?>]`: A kiszolgáló felhasználó által látható állapota.</span><span class="sxs-lookup"><span data-stu-id="aaebf-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="aaebf-179">`[Version <ServerVersion?>]`: Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="aaebf-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="aaebf-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaebf-180">RELATED LINKS</span></span>

