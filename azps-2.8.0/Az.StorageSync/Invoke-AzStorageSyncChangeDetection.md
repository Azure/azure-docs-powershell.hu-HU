---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839875"
---
# <span data-ttu-id="d5183-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="d5183-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="d5183-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5183-102">SYNOPSIS</span></span>
<span data-ttu-id="d5183-103">Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="d5183-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="d5183-104">A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet.</span><span class="sxs-lookup"><span data-stu-id="d5183-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="d5183-105">A 10 000-es módosítások maximális száma észlelhető.</span><span class="sxs-lookup"><span data-stu-id="d5183-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="d5183-106">Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető, és egy 10 000-módosítási korláton belül.</span><span class="sxs-lookup"><span data-stu-id="d5183-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="d5183-107">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5183-107">SYNTAX</span></span>

### <span data-ttu-id="d5183-108">StringAndDirectoryParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5183-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5183-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5183-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5183-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5183-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5183-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5183-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5183-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5183-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5183-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5183-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5183-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5183-114">DESCRIPTION</span></span>
<span data-ttu-id="d5183-115">Időnként az Azure-fájlok szinkronizálása az Azure-fájlmegosztás részeként ellenőrzi, hogy a fájlok megosztása más módon történt-e a szinkronizáláshoz. A cél a módosítások és a hozzájuk kapcsolódó kiszolgálók szinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="d5183-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="d5183-116">Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="d5183-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="d5183-117">A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet.</span><span class="sxs-lookup"><span data-stu-id="d5183-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="d5183-118">Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető, és egy 10 000-módosítási korláton belül.</span><span class="sxs-lookup"><span data-stu-id="d5183-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="d5183-119">Példák</span><span class="sxs-lookup"><span data-stu-id="d5183-119">EXAMPLES</span></span>

### <span data-ttu-id="d5183-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5183-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="d5183-121">Ebben a példában a változtatások észlelését az Azure-fájlmegosztás szinkronizálási "Data" és "Reporting\Templates" könyvtára futtatja.</span><span class="sxs-lookup"><span data-stu-id="d5183-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="d5183-122">Az összes útvonal az Azure-fájlmegosztás névterének gyökeréhez viszonyított.</span><span class="sxs-lookup"><span data-stu-id="d5183-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="d5183-123">2. példa</span><span class="sxs-lookup"><span data-stu-id="d5183-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="d5183-124">Ebben a példában a hívó által ismert fájlok halmazát a program módosította.</span><span class="sxs-lookup"><span data-stu-id="d5183-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="d5183-125">A cél az Azure-fájlok szinkronizálása a módosítások észlelésével és szinkronizálásával is.</span><span class="sxs-lookup"><span data-stu-id="d5183-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="d5183-126">3. példa</span><span class="sxs-lookup"><span data-stu-id="d5183-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="d5183-127">Ebben a példában az észlelési funkció a "példák" könyvtárba kerül, és rekurzívan észleli a változásokat az alkönyvtárakban.</span><span class="sxs-lookup"><span data-stu-id="d5183-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="d5183-128">Tartsa szem előtt, hogy a parancs a 10 000-os módosításokat csak az automatikus megszakítás után észleli.</span><span class="sxs-lookup"><span data-stu-id="d5183-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="d5183-129">Ha úgy gondolja, hogy több mint 10 000-módosítás történt, futtassa a parancsot a névtér alrészein.</span><span class="sxs-lookup"><span data-stu-id="d5183-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="d5183-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5183-130">PARAMETERS</span></span>

### <span data-ttu-id="d5183-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5183-131">-AsJob</span></span>
<span data-ttu-id="d5183-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d5183-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5183-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5183-133">-DefaultProfile</span></span>
<span data-ttu-id="d5183-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5183-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5183-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="d5183-135">-DirectoryPath</span></span>
<span data-ttu-id="d5183-136">Annak a könyvtárnak a helye, ahol a változások észlelése történik.</span><span class="sxs-lookup"><span data-stu-id="d5183-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="d5183-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5183-137">-InputObject</span></span>
<span data-ttu-id="d5183-138">CloudEndpoint objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="d5183-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d5183-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5183-139">-Name</span></span>
<span data-ttu-id="d5183-140">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="d5183-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="d5183-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5183-141">-PassThru</span></span>
<span data-ttu-id="d5183-142">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="d5183-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="d5183-143">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="d5183-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="d5183-144">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d5183-144">-Path</span></span>
<span data-ttu-id="d5183-145">Az a hely, ahol a változások észlelése történik.</span><span class="sxs-lookup"><span data-stu-id="d5183-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="d5183-146">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="d5183-146">-Recursive</span></span>
<span data-ttu-id="d5183-147">Annak jelzése, hogy a címtár-módosítási észlelés rekurzív-e.</span><span class="sxs-lookup"><span data-stu-id="d5183-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="d5183-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5183-148">-ResourceGroupName</span></span>
<span data-ttu-id="d5183-149">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d5183-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="d5183-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5183-150">-ResourceId</span></span>
<span data-ttu-id="d5183-151">CloudEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d5183-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="d5183-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d5183-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="d5183-153">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="d5183-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d5183-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d5183-154">-SyncGroupName</span></span>
<span data-ttu-id="d5183-155">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="d5183-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d5183-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5183-156">-Confirm</span></span>
<span data-ttu-id="d5183-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5183-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5183-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5183-158">-WhatIf</span></span>
<span data-ttu-id="d5183-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5183-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5183-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5183-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5183-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5183-161">CommonParameters</span></span>
<span data-ttu-id="d5183-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5183-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5183-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5183-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5183-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5183-164">INPUTS</span></span>

### <span data-ttu-id="d5183-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d5183-165">System.String</span></span>

### <span data-ttu-id="d5183-166">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5183-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="d5183-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5183-167">OUTPUTS</span></span>

### <span data-ttu-id="d5183-168">System. Void</span><span class="sxs-lookup"><span data-stu-id="d5183-168">System.Void</span></span>

## <span data-ttu-id="d5183-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5183-169">NOTES</span></span>

## <span data-ttu-id="d5183-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5183-170">RELATED LINKS</span></span>
