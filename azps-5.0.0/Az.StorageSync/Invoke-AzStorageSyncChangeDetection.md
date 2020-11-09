---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: f76a399d9d2e592bbea10a9e304d8f6875eea227
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302916"
---
# <span data-ttu-id="43582-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="43582-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="43582-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43582-102">SYNOPSIS</span></span>
<span data-ttu-id="43582-103">Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="43582-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="43582-104">A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet.</span><span class="sxs-lookup"><span data-stu-id="43582-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="43582-105">Legfeljebb 10 000 elemet lehet észlelni.</span><span class="sxs-lookup"><span data-stu-id="43582-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="43582-106">Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető a 10 000-elemen belül.</span><span class="sxs-lookup"><span data-stu-id="43582-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="43582-107">Az Invoke-AzStorageSyncChangeDetection parancsmag nem észleli az Azure-fájlmegosztás alábbi módosításait:</span><span class="sxs-lookup"><span data-stu-id="43582-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="43582-108">Törölt fájlok.</span><span class="sxs-lookup"><span data-stu-id="43582-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="43582-109">A megosztásból áthelyezett fájlok.</span><span class="sxs-lookup"><span data-stu-id="43582-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="43582-110">Azok a fájlok, amelyeket töröltek és ugyanazzal a névvel hoztak létre.</span><span class="sxs-lookup"><span data-stu-id="43582-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="43582-111">Ezek a módosítások akkor észlelhetők, ha a [változtatás észlelése feladat](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) fut.</span><span class="sxs-lookup"><span data-stu-id="43582-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) runs.</span></span>

## <span data-ttu-id="43582-112">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43582-112">SYNTAX</span></span>

### <span data-ttu-id="43582-113">StringAndDirectoryParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43582-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43582-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="43582-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43582-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="43582-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43582-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="43582-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43582-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="43582-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43582-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="43582-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43582-119">Leírás</span><span class="sxs-lookup"><span data-stu-id="43582-119">DESCRIPTION</span></span>
<span data-ttu-id="43582-120">Időnként az Azure-fájlok szinkronizálása az Azure-fájlmegosztás részeként ellenőrzi, hogy a fájlok megosztása más módon történt-e a szinkronizáláshoz. A cél a módosítások és a hozzájuk kapcsolódó kiszolgálók szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="43582-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="43582-121">Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="43582-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="43582-122">A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet.</span><span class="sxs-lookup"><span data-stu-id="43582-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="43582-123">Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető a 10 000-elemek korlátozásán belül.</span><span class="sxs-lookup"><span data-stu-id="43582-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="43582-124">Példák</span><span class="sxs-lookup"><span data-stu-id="43582-124">EXAMPLES</span></span>

### <span data-ttu-id="43582-125">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43582-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="43582-126">Ebben a példában a változtatások észlelését az Azure-fájlmegosztás szinkronizálási "Data" és "Reporting\Templates" könyvtára futtatja.</span><span class="sxs-lookup"><span data-stu-id="43582-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="43582-127">Az összes útvonal az Azure-fájlmegosztás névterének gyökeréhez viszonyított.</span><span class="sxs-lookup"><span data-stu-id="43582-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="43582-128">2. példa</span><span class="sxs-lookup"><span data-stu-id="43582-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="43582-129">Ebben a példában a hívó által ismert fájlok halmazát a program módosította.</span><span class="sxs-lookup"><span data-stu-id="43582-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="43582-130">A cél az Azure-fájlok szinkronizálása a módosítások észlelésével és szinkronizálásával is.</span><span class="sxs-lookup"><span data-stu-id="43582-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="43582-131">3. példa</span><span class="sxs-lookup"><span data-stu-id="43582-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="43582-132">Ebben a példában az észlelési funkció a "példák" könyvtárba kerül, és rekurzívan észleli a változásokat az alkönyvtárakban.</span><span class="sxs-lookup"><span data-stu-id="43582-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="43582-133">Tartsa szem előtt, hogy a parancsmag sikertelen lesz, ha az elérési út több mint 10 000 elemet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="43582-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="43582-134">Ha az elérési út több mint 10 000 elemet tartalmaz, futtassa a parancsot a névtér alrészein.</span><span class="sxs-lookup"><span data-stu-id="43582-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="43582-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43582-135">PARAMETERS</span></span>

### <span data-ttu-id="43582-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43582-136">-AsJob</span></span>
<span data-ttu-id="43582-137">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43582-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43582-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43582-138">-DefaultProfile</span></span>
<span data-ttu-id="43582-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43582-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43582-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="43582-140">-DirectoryPath</span></span>
<span data-ttu-id="43582-141">Annak a könyvtárnak a helye, ahol a változások észlelése történik.</span><span class="sxs-lookup"><span data-stu-id="43582-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="43582-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43582-142">-InputObject</span></span>
<span data-ttu-id="43582-143">CloudEndpoint objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="43582-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="43582-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43582-144">-Name</span></span>
<span data-ttu-id="43582-145">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="43582-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="43582-146">A név egy globálisan egyedi azonosító, nem a portálon megjelenő felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="43582-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="43582-147">A CloudEndpointName megszerzéséhez használja az Get-AzStorageSyncCloudEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="43582-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="43582-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43582-148">-PassThru</span></span>
<span data-ttu-id="43582-149">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="43582-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="43582-150">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="43582-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="43582-151">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="43582-151">-Path</span></span>
<span data-ttu-id="43582-152">Az a hely, ahol a változások észlelése történik.</span><span class="sxs-lookup"><span data-stu-id="43582-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="43582-153">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="43582-153">-Recursive</span></span>
<span data-ttu-id="43582-154">Annak jelzése, hogy a címtár-módosítási észlelés rekurzív-e.</span><span class="sxs-lookup"><span data-stu-id="43582-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="43582-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43582-155">-ResourceGroupName</span></span>
<span data-ttu-id="43582-156">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="43582-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="43582-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43582-157">-ResourceId</span></span>
<span data-ttu-id="43582-158">CloudEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="43582-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="43582-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="43582-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="43582-160">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="43582-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="43582-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="43582-161">-SyncGroupName</span></span>
<span data-ttu-id="43582-162">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="43582-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="43582-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43582-163">-Confirm</span></span>
<span data-ttu-id="43582-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43582-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43582-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43582-165">-WhatIf</span></span>
<span data-ttu-id="43582-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43582-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43582-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43582-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43582-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43582-168">CommonParameters</span></span>
<span data-ttu-id="43582-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43582-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43582-170">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43582-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43582-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43582-171">INPUTS</span></span>

### <span data-ttu-id="43582-172">System. String</span><span class="sxs-lookup"><span data-stu-id="43582-172">System.String</span></span>

### <span data-ttu-id="43582-173">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43582-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="43582-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43582-174">OUTPUTS</span></span>

### <span data-ttu-id="43582-175">System. Void</span><span class="sxs-lookup"><span data-stu-id="43582-175">System.Void</span></span>

## <span data-ttu-id="43582-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43582-176">NOTES</span></span>

## <span data-ttu-id="43582-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43582-177">RELATED LINKS</span></span>
