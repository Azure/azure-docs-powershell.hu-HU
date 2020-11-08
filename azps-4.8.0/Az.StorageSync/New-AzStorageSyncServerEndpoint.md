---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017500"
---
# <span data-ttu-id="e9b43-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9b43-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="e9b43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9b43-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b43-103">Ez a parancs létrehoz egy új kiszolgálói végpontot egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e9b43-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="e9b43-104">Ez a beállítás lehetővé teszi a kiszolgálón megadott elérési út szinkronizálását a fájlok más végpontokkal való szinkronizálásának megkezdéséhez a szinkronizálás csoportban.</span><span class="sxs-lookup"><span data-stu-id="e9b43-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="e9b43-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9b43-105">SYNTAX</span></span>

### <span data-ttu-id="e9b43-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9b43-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b43-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b43-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b43-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b43-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9b43-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9b43-109">DESCRIPTION</span></span>
<span data-ttu-id="e9b43-110">Ez a parancs létrehoz egy új kiszolgálói végpontot egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e9b43-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="e9b43-111">Ez a beállítás lehetővé teszi a kiszolgálón megadott elérési út szinkronizálását a fájlok más végpontokkal való szinkronizálásának megkezdéséhez a szinkronizálás csoportban.</span><span class="sxs-lookup"><span data-stu-id="e9b43-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="e9b43-112">Ha a szinkronizálási csoportban már vannak fájlok, és az újonnan hozzáadott hely is tartalmaz fájlokat, az egyeztetési folyamat megkísérli annak megállapítását, hogy a fájlok valójában ugyanazok-e, mint az egyéb végpontokon.</span><span class="sxs-lookup"><span data-stu-id="e9b43-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="e9b43-113">A névterek egyesítése és egyeztetése megkönnyíti az ütközéses fájlok megelőzését.</span><span class="sxs-lookup"><span data-stu-id="e9b43-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="e9b43-114">Ha más kiszolgálói végpontokon is vannak fájlok, akkor ez a beállítás gyakran jobb, ha egy üres helyről van szó ebben a kiszolgálón, így a felhőből származó fájlok a gyors katasztrófa-helyreállítás nevű automatikus eljárásban jutnak el a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="e9b43-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="e9b43-115">A program először szinkronizálja a névterek metaadatait, majd letölti az egyes fájlok adatfolyamát.</span><span class="sxs-lookup"><span data-stu-id="e9b43-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="e9b43-116">Ha egy felhasználó vagy egy alkalmazás letöltési sorrendtől kéri a fájlt, a program az Access-kérésnek megfelelő prioritással fogja visszahívni a fájlt.</span><span class="sxs-lookup"><span data-stu-id="e9b43-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="e9b43-117">A kiszolgáló végpontján tetszés szerint megadhatja, hogy az adott végpont a felhőből származó fájlok teljes készletének gyorsítótára legyen-e.</span><span class="sxs-lookup"><span data-stu-id="e9b43-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="e9b43-118">Ha a Felhőbeli adatréteget használja, a fájl tartalma letöltés a beállított Felhőbeli adatkorlátozási házirendek által meghatározott pontra fog megjelenni.</span><span class="sxs-lookup"><span data-stu-id="e9b43-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="e9b43-119">Példák</span><span class="sxs-lookup"><span data-stu-id="e9b43-119">EXAMPLES</span></span>

### <span data-ttu-id="e9b43-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e9b43-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="e9b43-121">A parancs létrehoz egy új kiszolgálói végpontot egy regisztrált kiszolgálón, és beszúrja egy szinkronizálási csoportba.</span><span class="sxs-lookup"><span data-stu-id="e9b43-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="e9b43-122">Így az egyéb végpontok topológiájának része, és a fájl metaadatai és a tartalmak is azonnal elkezdenek szinkronizálni a szinkronizálás csoportban végpontként hivatkozott helyek között.</span><span class="sxs-lookup"><span data-stu-id="e9b43-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="e9b43-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9b43-123">PARAMETERS</span></span>

### <span data-ttu-id="e9b43-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9b43-124">-AsJob</span></span>
<span data-ttu-id="e9b43-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e9b43-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9b43-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="e9b43-126">-CloudTiering</span></span>
<span data-ttu-id="e9b43-127">Felhőbeli adatmeghatározás paraméter</span><span class="sxs-lookup"><span data-stu-id="e9b43-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="e9b43-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b43-128">-DefaultProfile</span></span>
<span data-ttu-id="e9b43-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9b43-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9b43-130">-Name</span></span>
<span data-ttu-id="e9b43-131">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="e9b43-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="e9b43-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="e9b43-133">Felhőbe minősített adatérték paraméter</span><span class="sxs-lookup"><span data-stu-id="e9b43-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="e9b43-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="e9b43-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="e9b43-135">Felhőalapú minősített adatfájl-megosztás URI-paramétere</span><span class="sxs-lookup"><span data-stu-id="e9b43-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="e9b43-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="e9b43-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="e9b43-137">Helyi gyorsítótári mód paraméter</span><span class="sxs-lookup"><span data-stu-id="e9b43-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="e9b43-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="e9b43-138">-localCacheMode</span></span>
<span data-ttu-id="e9b43-139">Helyi gyorsítótári mód paraméter</span><span class="sxs-lookup"><span data-stu-id="e9b43-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="e9b43-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e9b43-140">-ParentObject</span></span>
<span data-ttu-id="e9b43-141">SyncGroup objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="e9b43-141">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b43-142">-ParentResourceId</span></span>
<span data-ttu-id="e9b43-143">A SyncGroup szülő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e9b43-143">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b43-144">-ResourceGroupName</span></span>
<span data-ttu-id="e9b43-145">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e9b43-145">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="e9b43-146">-ServerLocalPath</span></span>
<span data-ttu-id="e9b43-147">A kiszolgáló helyi elérési útja paraméter</span><span class="sxs-lookup"><span data-stu-id="e9b43-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="e9b43-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b43-148">-ServerResourceId</span></span>
<span data-ttu-id="e9b43-149">RegisteredServer erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e9b43-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="e9b43-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e9b43-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="e9b43-151">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="e9b43-151">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b43-152">-SyncGroupName</span></span>
<span data-ttu-id="e9b43-153">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="e9b43-153">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="e9b43-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="e9b43-155">A Days paraméternél régebbi fájlok</span><span class="sxs-lookup"><span data-stu-id="e9b43-155">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="e9b43-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="e9b43-157">Mennyiségi szabad terület százalékos értéke</span><span class="sxs-lookup"><span data-stu-id="e9b43-157">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b43-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e9b43-158">-Confirm</span></span>
<span data-ttu-id="e9b43-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9b43-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b43-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b43-160">-WhatIf</span></span>
<span data-ttu-id="e9b43-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e9b43-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9b43-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9b43-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b43-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b43-163">CommonParameters</span></span>
<span data-ttu-id="e9b43-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9b43-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b43-165">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b43-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b43-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b43-166">INPUTS</span></span>

### <span data-ttu-id="e9b43-167">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e9b43-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="e9b43-168">System. String</span><span class="sxs-lookup"><span data-stu-id="e9b43-168">System.String</span></span>

## <span data-ttu-id="e9b43-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b43-169">OUTPUTS</span></span>

### <span data-ttu-id="e9b43-170">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9b43-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="e9b43-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9b43-171">NOTES</span></span>

## <span data-ttu-id="e9b43-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9b43-172">RELATED LINKS</span></span>
