---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366644"
---
# <span data-ttu-id="4b9c3-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b9c3-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="4b9c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9c3-103">Ez a parancs új kiszolgáló végpontot hoz létre egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="4b9c3-104">Ez lehetővé teszi, hogy a kiszolgálón megadott elérési út elindítsa a fájlok szinkronizálását a szinkronizálási csoport más végpontjaival.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="4b9c3-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b9c3-105">SYNTAX</span></span>

### <span data-ttu-id="4b9c3-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b9c3-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b9c3-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b9c3-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b9c3-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b9c3-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b9c3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b9c3-109">DESCRIPTION</span></span>
<span data-ttu-id="4b9c3-110">Ez a parancs új kiszolgáló végpontot hoz létre egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="4b9c3-111">Ez lehetővé teszi, hogy a kiszolgálón megadott elérési út elindítsa a fájlok szinkronizálását a szinkronizálási csoport más végpontjaival.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="4b9c3-112">Ha a szinkronizálási csoportban már vannak fájlok más végpontok, és ez az újonnan hozzáadott hely is tartalmaz fájlokat, egy egyeztetési folyamat megpróbálja megállapítani, hogy a fájlok valójában ugyanazok-e a mappákban, mint a többi végponton.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="4b9c3-113">A névterek egyesítése és egyeztetése segít megelőzni az ütköző fájlokat.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="4b9c3-114">Ha más kiszolgálói végpontok is tartalmaznak fájlokat, gyakran jobb, ha először egy üres helyet ad meg ezen a kiszolgálón, hogy a felhőből származó fájlok egy gyors katasztrófa-helyreállítás néven nevezett automatikus folyamatban leküldenek a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="4b9c3-115">A névtér metaadatait először a rendszer először szinkronizálja, majd letölti az egyes fájlok adatfolyamát.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="4b9c3-116">Ha egy felhasználó vagy alkalmazás a letöltési megrendelésen túl kér egy fájlt, a rendszer prioritással visszahívja a fájlt, hogy megfeleljen a hozzáférési kérésnek.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="4b9c3-117">Ezen a kiszolgálói végponton szükség esetén felhőszintű rétegezés használatával megállapíthatja, hogy a végpontnak kellene-e a felhőből származó fájlok teljes halmazának gyorsítótáraként lennie.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="4b9c3-118">Ha felhőszintű rétegezést használ, akkor a fájltartalom letöltése a beállítható felhőréteg-házirendek által meghatározott ponton leáll.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="4b9c3-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b9c3-119">EXAMPLES</span></span>

### <span data-ttu-id="4b9c3-120">1. példa</span><span class="sxs-lookup"><span data-stu-id="4b9c3-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="4b9c3-121">Ez a parancs létrehoz egy új kiszolgáló végpontot egy regisztrált kiszolgálón, és beszúrja azt egy szinkronizálási csoportba.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="4b9c3-122">Ez a módszer a többi végpont topológiájának része, a fájl metaadatai és tartalmai pedig azonnal elkezdenek szinkronizálni a szinkronizálási csoport végpontjaiként hivatkozott összes hely között.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="4b9c3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b9c3-123">PARAMETERS</span></span>

### <span data-ttu-id="4b9c3-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b9c3-124">-AsJob</span></span>
<span data-ttu-id="4b9c3-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4b9c3-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b9c3-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="4b9c3-126">-CloudTiering</span></span>
<span data-ttu-id="4b9c3-127">Felhőszintű rétegezés paramétere</span><span class="sxs-lookup"><span data-stu-id="4b9c3-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="4b9c3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9c3-128">-DefaultProfile</span></span>
<span data-ttu-id="4b9c3-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b9c3-130">-Name</span><span class="sxs-lookup"><span data-stu-id="4b9c3-130">-Name</span></span>
<span data-ttu-id="4b9c3-131">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="4b9c3-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="4b9c3-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="4b9c3-133">Cloud Seeded Data Parameter</span><span class="sxs-lookup"><span data-stu-id="4b9c3-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="4b9c3-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="4b9c3-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="4b9c3-135">Cloud Seeded Data File Share Uri Parameter</span><span class="sxs-lookup"><span data-stu-id="4b9c3-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="4b9c3-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="4b9c3-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="4b9c3-137">Local cache mode Parameter</span><span class="sxs-lookup"><span data-stu-id="4b9c3-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="4b9c3-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="4b9c3-138">-localCacheMode</span></span>
<span data-ttu-id="4b9c3-139">Local cache mode Parameter</span><span class="sxs-lookup"><span data-stu-id="4b9c3-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="4b9c3-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4b9c3-140">-ParentObject</span></span>
<span data-ttu-id="4b9c3-141">SyncGroup-objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="4b9c3-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4b9c3-142">-ParentResourceId</span></span>
<span data-ttu-id="4b9c3-143">SyncGroup szülőerőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4b9c3-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="4b9c3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b9c3-144">-ResourceGroupName</span></span>
<span data-ttu-id="4b9c3-145">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="4b9c3-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="4b9c3-146">-ServerLocalPath</span></span>
<span data-ttu-id="4b9c3-147">Kiszolgáló helyi elérési útvonalának paramétere</span><span class="sxs-lookup"><span data-stu-id="4b9c3-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="4b9c3-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="4b9c3-148">-ServerResourceId</span></span>
<span data-ttu-id="4b9c3-149">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="4b9c3-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="4b9c3-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4b9c3-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="4b9c3-151">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4b9c3-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4b9c3-152">-SyncGroupName</span></span>
<span data-ttu-id="4b9c3-153">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4b9c3-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4b9c3-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="4b9c3-155">A napnál régebbi tier fájlok paramétere</span><span class="sxs-lookup"><span data-stu-id="4b9c3-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="4b9c3-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="4b9c3-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="4b9c3-157">Volume Free Space Percent Parameter</span><span class="sxs-lookup"><span data-stu-id="4b9c3-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="4b9c3-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b9c3-158">-Confirm</span></span>
<span data-ttu-id="4b9c3-159">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b9c3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b9c3-160">-WhatIf</span></span>
<span data-ttu-id="4b9c3-161">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b9c3-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b9c3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9c3-163">CommonParameters</span></span>
<span data-ttu-id="4b9c3-164">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9c3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9c3-165">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b9c3-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9c3-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b9c3-166">INPUTS</span></span>

### <span data-ttu-id="4b9c3-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4b9c3-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="4b9c3-168">System.String</span><span class="sxs-lookup"><span data-stu-id="4b9c3-168">System.String</span></span>

## <span data-ttu-id="4b9c3-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b9c3-169">OUTPUTS</span></span>

### <span data-ttu-id="4b9c3-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b9c3-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4b9c3-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b9c3-171">NOTES</span></span>

## <span data-ttu-id="4b9c3-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b9c3-172">RELATED LINKS</span></span>
