---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: d55ffe30554c70b9d7b8fa1ed90380c6a5b181cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011429"
---
# <span data-ttu-id="e74f8-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="e74f8-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="e74f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e74f8-102">SYNOPSIS</span></span>
<span data-ttu-id="e74f8-103">Ezzel a paranccsal manuálisan elindíthatja a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="e74f8-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="e74f8-104">Meg lehet célzottan a teljes megosztásra, almappára vagy fájlkészletre.</span><span class="sxs-lookup"><span data-stu-id="e74f8-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="e74f8-105">Legfeljebb 10 000 elem észlelhető.</span><span class="sxs-lookup"><span data-stu-id="e74f8-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="e74f8-106">Ha ön ismeri a módosítások hatókörét, a parancs végrehajtását a névtér bizonyos részeire korlátozhatja, így a változások észlelése gyorsan befejeződhet a 10 000 elemes korláton belül.</span><span class="sxs-lookup"><span data-stu-id="e74f8-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="e74f8-107">A Invoke-AzStorageSyncChangeDetection parancsmag nem észleli a következő módosításokat az Azure-fájlmegosztásban:</span><span class="sxs-lookup"><span data-stu-id="e74f8-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="e74f8-108">Törölt fájlok.</span><span class="sxs-lookup"><span data-stu-id="e74f8-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="e74f8-109">Azok a fájlok, amelyek átkerültek a megosztásból.</span><span class="sxs-lookup"><span data-stu-id="e74f8-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="e74f8-110">Az azonos nevű törölt és létrehozott fájlok.</span><span class="sxs-lookup"><span data-stu-id="e74f8-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="e74f8-111">Ezeket a módosításokat a program észleli a [módosításészlelési feladat futtatásakor.](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection)</span><span class="sxs-lookup"><span data-stu-id="e74f8-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="e74f8-112">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e74f8-112">SYNTAX</span></span>

### <span data-ttu-id="e74f8-113">StringAndDirectoryParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e74f8-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74f8-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="e74f8-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74f8-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="e74f8-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74f8-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="e74f8-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74f8-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="e74f8-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74f8-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="e74f8-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e74f8-119">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e74f8-119">DESCRIPTION</span></span>
<span data-ttu-id="e74f8-120">Az Azure File Sync rendszeres időközönként ellenőrzi a névteret egy szinkronizált Azure-fájlmegosztáson belül a fájlmegosztáson a szinkronizáláson kívül más módon történt módosítások után. A cél az, hogy azonosítsa ezeket a módosításokat, és végül szinkronizálja őket a csatlakoztatott kiszolgálókkal.</span><span class="sxs-lookup"><span data-stu-id="e74f8-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="e74f8-121">Ezzel a paranccsal manuálisan elindíthatja a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="e74f8-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="e74f8-122">Meg lehet célzottan a teljes megosztásra, almappára vagy fájlkészletre.</span><span class="sxs-lookup"><span data-stu-id="e74f8-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="e74f8-123">Ha ön ismeri a módosítások hatókörét, a parancs végrehajtását a névtér bizonyos részeire korlátozhatja, így a változások észlelése gyorsan befejeződhet, és a 10 000 elemes korláton belülre eshet.</span><span class="sxs-lookup"><span data-stu-id="e74f8-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="e74f8-124">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e74f8-124">EXAMPLES</span></span>

### <span data-ttu-id="e74f8-125">1. példa</span><span class="sxs-lookup"><span data-stu-id="e74f8-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="e74f8-126">Ebben a példában a változások észlelése egy szinkronizált Azure-fájlmegosztás "Adatok" és "Reporting\Templates" könyvtárában fut.</span><span class="sxs-lookup"><span data-stu-id="e74f8-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="e74f8-127">Minden elérési út az Azure-fájlmegosztás névterének gyökerénél van.</span><span class="sxs-lookup"><span data-stu-id="e74f8-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="e74f8-128">2. példa</span><span class="sxs-lookup"><span data-stu-id="e74f8-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="e74f8-129">Ebben a példában a változások észlelése olyan fájlkészlethez fut, amelyről a parancs hívója tudomása szerint módosult.</span><span class="sxs-lookup"><span data-stu-id="e74f8-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="e74f8-130">A cél az, hogy az Azure fájlszinkronizálás észlelje és szinkronizálja ezeket a módosításokat is.</span><span class="sxs-lookup"><span data-stu-id="e74f8-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="e74f8-131">3. példa</span><span class="sxs-lookup"><span data-stu-id="e74f8-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="e74f8-132">Ebben a példában a változások észlelése a "Examples" (Példák) címtárban fut, és rekurzívan észleli az alkönyvtárak változásait.</span><span class="sxs-lookup"><span data-stu-id="e74f8-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="e74f8-133">Ne feledje, hogy a parancsmag nem fog működni, ha az elérési út 10 000-nél több elemet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e74f8-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="e74f8-134">Ha az elérési út több mint 10 000 elemet tartalmaz, futtassa a parancsot a névtér al részein.</span><span class="sxs-lookup"><span data-stu-id="e74f8-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="e74f8-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e74f8-135">PARAMETERS</span></span>

### <span data-ttu-id="e74f8-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e74f8-136">-AsJob</span></span>
<span data-ttu-id="e74f8-137">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e74f8-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e74f8-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e74f8-138">-DefaultProfile</span></span>
<span data-ttu-id="e74f8-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e74f8-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e74f8-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="e74f8-140">-DirectoryPath</span></span>
<span data-ttu-id="e74f8-141">Címtár, amelyben a változások észlelése történik.</span><span class="sxs-lookup"><span data-stu-id="e74f8-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="e74f8-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e74f8-142">-InputObject</span></span>
<span data-ttu-id="e74f8-143">CloudEndpoint-objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="e74f8-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="e74f8-144">-Name</span><span class="sxs-lookup"><span data-stu-id="e74f8-144">-Name</span></span>
<span data-ttu-id="e74f8-145">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="e74f8-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="e74f8-146">A név guid azonosító, nem pedig a portálon megjelenő rövid név.</span><span class="sxs-lookup"><span data-stu-id="e74f8-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="e74f8-147">A CloudEndpointName lekérte a Get-AzStorageSyncCloudEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e74f8-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e74f8-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e74f8-148">-PassThru</span></span>
<span data-ttu-id="e74f8-149">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="e74f8-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e74f8-150">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="e74f8-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e74f8-151">-Path</span><span class="sxs-lookup"><span data-stu-id="e74f8-151">-Path</span></span>
<span data-ttu-id="e74f8-152">A módosítás észlelésének elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e74f8-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="e74f8-153">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="e74f8-153">-Recursive</span></span>
<span data-ttu-id="e74f8-154">Annak jelzése, hogy a címtárváltozások észlelése rekurzív-e.</span><span class="sxs-lookup"><span data-stu-id="e74f8-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="e74f8-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e74f8-155">-ResourceGroupName</span></span>
<span data-ttu-id="e74f8-156">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e74f8-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="e74f8-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e74f8-157">-ResourceId</span></span>
<span data-ttu-id="e74f8-158">CloudEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="e74f8-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="e74f8-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e74f8-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="e74f8-160">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="e74f8-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e74f8-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e74f8-161">-SyncGroupName</span></span>
<span data-ttu-id="e74f8-162">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="e74f8-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="e74f8-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e74f8-163">-Confirm</span></span>
<span data-ttu-id="e74f8-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e74f8-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e74f8-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e74f8-165">-WhatIf</span></span>
<span data-ttu-id="e74f8-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e74f8-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e74f8-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e74f8-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e74f8-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e74f8-168">CommonParameters</span></span>
<span data-ttu-id="e74f8-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e74f8-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e74f8-170">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e74f8-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e74f8-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e74f8-171">INPUTS</span></span>

### <span data-ttu-id="e74f8-172">System.String</span><span class="sxs-lookup"><span data-stu-id="e74f8-172">System.String</span></span>

### <span data-ttu-id="e74f8-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e74f8-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="e74f8-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e74f8-174">OUTPUTS</span></span>

### <span data-ttu-id="e74f8-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="e74f8-175">System.Void</span></span>

## <span data-ttu-id="e74f8-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e74f8-176">NOTES</span></span>

## <span data-ttu-id="e74f8-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e74f8-177">RELATED LINKS</span></span>
