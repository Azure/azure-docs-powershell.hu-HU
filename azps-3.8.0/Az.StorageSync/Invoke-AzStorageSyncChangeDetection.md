---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013134"
---
# <span data-ttu-id="673ed-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="673ed-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="673ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="673ed-102">SYNOPSIS</span></span>
<span data-ttu-id="673ed-103">Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="673ed-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="673ed-104">A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet.</span><span class="sxs-lookup"><span data-stu-id="673ed-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="673ed-105">Legfeljebb 10 000 elemet lehet észlelni.</span><span class="sxs-lookup"><span data-stu-id="673ed-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="673ed-106">Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető a 10 000-elemen belül.</span><span class="sxs-lookup"><span data-stu-id="673ed-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="673ed-107">Az Invoke-AzStorageSyncChangeDetection parancsmag nem észleli az Azure-fájlmegosztás által törölt fájlokat.</span><span class="sxs-lookup"><span data-stu-id="673ed-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="673ed-108">Ha a fájlok az Azure-fájlmegosztás során törlődnek, akkor a rendszer észleli őket, amikor a [változások észlelése feladat](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) fut.</span><span class="sxs-lookup"><span data-stu-id="673ed-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="673ed-109">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="673ed-109">SYNTAX</span></span>

### <span data-ttu-id="673ed-110">StringAndDirectoryParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="673ed-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="673ed-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="673ed-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="673ed-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="673ed-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="673ed-113">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="673ed-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="673ed-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="673ed-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="673ed-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="673ed-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="673ed-116">Leírás</span><span class="sxs-lookup"><span data-stu-id="673ed-116">DESCRIPTION</span></span>
<span data-ttu-id="673ed-117">Időnként az Azure-fájlok szinkronizálása az Azure-fájlmegosztás részeként ellenőrzi, hogy a fájlok megosztása más módon történt-e a szinkronizáláshoz. A cél a módosítások és a hozzájuk kapcsolódó kiszolgálók szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="673ed-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="673ed-118">Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="673ed-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="673ed-119">A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet.</span><span class="sxs-lookup"><span data-stu-id="673ed-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="673ed-120">Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető, és egy 10 000-módosítási korláton belül.</span><span class="sxs-lookup"><span data-stu-id="673ed-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="673ed-121">Példák</span><span class="sxs-lookup"><span data-stu-id="673ed-121">EXAMPLES</span></span>

### <span data-ttu-id="673ed-122">Példa 1</span><span class="sxs-lookup"><span data-stu-id="673ed-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="673ed-123">Ebben a példában a változtatások észlelését az Azure-fájlmegosztás szinkronizálási "Data" és "Reporting\Templates" könyvtára futtatja.</span><span class="sxs-lookup"><span data-stu-id="673ed-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="673ed-124">Az összes útvonal az Azure-fájlmegosztás névterének gyökeréhez viszonyított.</span><span class="sxs-lookup"><span data-stu-id="673ed-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="673ed-125">2. példa</span><span class="sxs-lookup"><span data-stu-id="673ed-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="673ed-126">Ebben a példában a hívó által ismert fájlok halmazát a program módosította.</span><span class="sxs-lookup"><span data-stu-id="673ed-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="673ed-127">A cél az Azure-fájlok szinkronizálása a módosítások észlelésével és szinkronizálásával is.</span><span class="sxs-lookup"><span data-stu-id="673ed-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="673ed-128">3. példa</span><span class="sxs-lookup"><span data-stu-id="673ed-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="673ed-129">Ebben a példában az észlelési funkció a "példák" könyvtárba kerül, és rekurzívan észleli a változásokat az alkönyvtárakban.</span><span class="sxs-lookup"><span data-stu-id="673ed-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="673ed-130">Tartsa szem előtt, hogy a parancs a 10 000-os módosításokat csak az automatikus megszakítás után észleli.</span><span class="sxs-lookup"><span data-stu-id="673ed-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="673ed-131">Ha úgy gondolja, hogy több mint 10 000-módosítás történt, futtassa a parancsot a névtér alrészein.</span><span class="sxs-lookup"><span data-stu-id="673ed-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="673ed-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="673ed-132">PARAMETERS</span></span>

### <span data-ttu-id="673ed-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="673ed-133">-AsJob</span></span>
<span data-ttu-id="673ed-134">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="673ed-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="673ed-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="673ed-135">-DefaultProfile</span></span>
<span data-ttu-id="673ed-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="673ed-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="673ed-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="673ed-137">-DirectoryPath</span></span>
<span data-ttu-id="673ed-138">Annak a könyvtárnak a helye, ahol a változások észlelése történik.</span><span class="sxs-lookup"><span data-stu-id="673ed-138">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="673ed-139">-InputObject</span></span>
<span data-ttu-id="673ed-140">CloudEndpoint objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="673ed-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="673ed-141">-Name</span></span>
<span data-ttu-id="673ed-142">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="673ed-142">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="673ed-143">-PassThru</span></span>
<span data-ttu-id="673ed-144">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="673ed-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="673ed-145">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="673ed-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="673ed-146">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="673ed-146">-Path</span></span>
<span data-ttu-id="673ed-147">Az a hely, ahol a változások észlelése történik.</span><span class="sxs-lookup"><span data-stu-id="673ed-147">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-148">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="673ed-148">-Recursive</span></span>
<span data-ttu-id="673ed-149">Annak jelzése, hogy a címtár-módosítási észlelés rekurzív-e.</span><span class="sxs-lookup"><span data-stu-id="673ed-149">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="673ed-150">-ResourceGroupName</span></span>
<span data-ttu-id="673ed-151">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="673ed-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="673ed-152">-ResourceId</span></span>
<span data-ttu-id="673ed-153">CloudEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="673ed-153">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-154">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="673ed-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="673ed-155">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="673ed-155">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="673ed-156">-SyncGroupName</span></span>
<span data-ttu-id="673ed-157">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="673ed-157">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ed-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="673ed-158">-Confirm</span></span>
<span data-ttu-id="673ed-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="673ed-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="673ed-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="673ed-160">-WhatIf</span></span>
<span data-ttu-id="673ed-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="673ed-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="673ed-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="673ed-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="673ed-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673ed-163">CommonParameters</span></span>
<span data-ttu-id="673ed-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="673ed-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="673ed-165">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="673ed-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673ed-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="673ed-166">INPUTS</span></span>

### <span data-ttu-id="673ed-167">System. String</span><span class="sxs-lookup"><span data-stu-id="673ed-167">System.String</span></span>

### <span data-ttu-id="673ed-168">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="673ed-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="673ed-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="673ed-169">OUTPUTS</span></span>

### <span data-ttu-id="673ed-170">System. Void</span><span class="sxs-lookup"><span data-stu-id="673ed-170">System.Void</span></span>

## <span data-ttu-id="673ed-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="673ed-171">NOTES</span></span>

## <span data-ttu-id="673ed-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="673ed-172">RELATED LINKS</span></span>
