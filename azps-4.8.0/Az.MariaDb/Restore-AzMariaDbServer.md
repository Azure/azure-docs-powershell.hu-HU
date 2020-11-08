---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025262"
---
# <span data-ttu-id="5cc49-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="5cc49-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="5cc49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cc49-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc49-103">MariaDB visszaállítása meglévő MariaDB</span><span class="sxs-lookup"><span data-stu-id="5cc49-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="5cc49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cc49-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5cc49-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cc49-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc49-106">MariaDB visszaállítása meglévő MariaDB</span><span class="sxs-lookup"><span data-stu-id="5cc49-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="5cc49-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5cc49-107">EXAMPLES</span></span>

### <span data-ttu-id="5cc49-108">Példa 1: PointInTime-MariaDB visszaállítása kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="5cc49-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5cc49-109">Ez a parancs a PointInTime-MariaDB a kiszolgálónév szerint állítja vissza.</span><span class="sxs-lookup"><span data-stu-id="5cc49-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="5cc49-110">2. példa: PointInTime-MariaDB visszaállítása kiszolgálói objektum szerint</span><span class="sxs-lookup"><span data-stu-id="5cc49-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5cc49-111">Ez a parancs a PointInTime-MariaDB a kiszolgálón lévő objektum szerint állítja vissza.</span><span class="sxs-lookup"><span data-stu-id="5cc49-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="5cc49-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cc49-112">PARAMETERS</span></span>

### <span data-ttu-id="5cc49-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cc49-113">-AsJob</span></span>
<span data-ttu-id="5cc49-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5cc49-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5cc49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc49-115">-DefaultProfile</span></span>
<span data-ttu-id="5cc49-116">terület: az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetések DefaultParameters.</span><span class="sxs-lookup"><span data-stu-id="5cc49-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cc49-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cc49-117">-InputObject</span></span>
<span data-ttu-id="5cc49-118">A forrás kiszolgálói objektum, amelyből vissza szeretne térni.</span><span class="sxs-lookup"><span data-stu-id="5cc49-118">The source server object to restore from.</span></span>
<span data-ttu-id="5cc49-119">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5cc49-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cc49-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="5cc49-120">-Location</span></span>
<span data-ttu-id="5cc49-121">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="5cc49-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="5cc49-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5cc49-122">-Name</span></span>
<span data-ttu-id="5cc49-123">A cél-kiszolgáló neve, amelyet vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="5cc49-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="5cc49-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="5cc49-124">-NoWait</span></span>
<span data-ttu-id="5cc49-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5cc49-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5cc49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc49-126">-ResourceGroupName</span></span>
<span data-ttu-id="5cc49-127">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5cc49-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5cc49-128">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="5cc49-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5cc49-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="5cc49-129">-RestorePointInTime</span></span>
<span data-ttu-id="5cc49-130">területi PointInTimeRestore: az a hely, ahol az erőforrás lakik.</span><span class="sxs-lookup"><span data-stu-id="5cc49-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="5cc49-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5cc49-131">-ServerName</span></span>
<span data-ttu-id="5cc49-132">A forráskiszolgáló neve, amelyet vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="5cc49-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="5cc49-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cc49-133">-SubscriptionId</span></span>
<span data-ttu-id="5cc49-134">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="5cc49-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5cc49-135">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="5cc49-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5cc49-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="5cc49-136">-Tag</span></span>
<span data-ttu-id="5cc49-137">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="5cc49-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="5cc49-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5cc49-138">-Confirm</span></span>
<span data-ttu-id="5cc49-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cc49-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc49-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc49-140">-WhatIf</span></span>
<span data-ttu-id="5cc49-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5cc49-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc49-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cc49-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc49-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc49-143">CommonParameters</span></span>
<span data-ttu-id="5cc49-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cc49-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc49-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5cc49-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc49-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cc49-146">INPUTS</span></span>

### <span data-ttu-id="5cc49-147">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="5cc49-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5cc49-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cc49-148">OUTPUTS</span></span>

### <span data-ttu-id="5cc49-149">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="5cc49-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5cc49-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cc49-150">NOTES</span></span>

<span data-ttu-id="5cc49-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5cc49-151">ALIASES</span></span>

<span data-ttu-id="5cc49-152">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="5cc49-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cc49-153">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5cc49-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cc49-154">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5cc49-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cc49-155">INPUTOBJECT <IServer> : a Source Server objektum, amelyből vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="5cc49-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="5cc49-156">`Location <String>`: Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="5cc49-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="5cc49-157">`[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="5cc49-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="5cc49-158">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="5cc49-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5cc49-159">`[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5cc49-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="5cc49-160">Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="5cc49-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="5cc49-161">`[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)</span><span class="sxs-lookup"><span data-stu-id="5cc49-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="5cc49-162">`[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.</span><span class="sxs-lookup"><span data-stu-id="5cc49-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="5cc49-163">`[IdentityType <IdentityType?>]`: Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="5cc49-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="5cc49-164">A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.</span><span class="sxs-lookup"><span data-stu-id="5cc49-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="5cc49-165">`[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5cc49-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="5cc49-166">`[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.</span><span class="sxs-lookup"><span data-stu-id="5cc49-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="5cc49-167">`[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.</span><span class="sxs-lookup"><span data-stu-id="5cc49-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="5cc49-168">`[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5cc49-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="5cc49-169">`[SkuFamily <String>]`: A hardver családja.</span><span class="sxs-lookup"><span data-stu-id="5cc49-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="5cc49-170">`[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5cc49-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="5cc49-171">`[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.</span><span class="sxs-lookup"><span data-stu-id="5cc49-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="5cc49-172">`[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).</span><span class="sxs-lookup"><span data-stu-id="5cc49-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="5cc49-173">`[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="5cc49-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="5cc49-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5cc49-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="5cc49-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="5cc49-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="5cc49-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5cc49-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="5cc49-177">`[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5cc49-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="5cc49-178">`[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="5cc49-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="5cc49-179">`[Version <ServerVersion?>]`: Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="5cc49-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="5cc49-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cc49-180">RELATED LINKS</span></span>

