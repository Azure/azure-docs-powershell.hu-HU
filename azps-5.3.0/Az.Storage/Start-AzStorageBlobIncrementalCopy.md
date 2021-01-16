---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376080"
---
# <span data-ttu-id="a2e9d-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="a2e9d-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="a2e9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e9d-103">Növekményes másolási művelet indítása lap blob-pillanatfelvételből a megadott céllap blobba.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="a2e9d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2e9d-104">SYNTAX</span></span>

### <span data-ttu-id="a2e9d-105">ContainerInstance (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2e9d-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e9d-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="a2e9d-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e9d-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="a2e9d-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e9d-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="a2e9d-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e9d-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="a2e9d-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e9d-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2e9d-110">DESCRIPTION</span></span>
<span data-ttu-id="a2e9d-111">Növekményes másolási művelet indítása lap blob-pillanatfelvételből a megadott céllap blobba.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="a2e9d-112">A funkcióról a következőben olvashat https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob bővebben: .</span><span class="sxs-lookup"><span data-stu-id="a2e9d-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="a2e9d-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2e9d-113">EXAMPLES</span></span>

### <span data-ttu-id="a2e9d-114">1. példa: Növekményes másolási művelet indítása blobnév és pillanatkép-idő szerint</span><span class="sxs-lookup"><span data-stu-id="a2e9d-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="a2e9d-115">Ez a parancs elindítja a Növekményes másolási műveletet blobnév és pillanatkép-idő szerint</span><span class="sxs-lookup"><span data-stu-id="a2e9d-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="a2e9d-116">2. példa: Növekményes másolási művelet kezdése a forrás uri használatával</span><span class="sxs-lookup"><span data-stu-id="a2e9d-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="a2e9d-117">Ez a parancs elindítja a Növekményes másolási műveletet a forrás uri használatával</span><span class="sxs-lookup"><span data-stu-id="a2e9d-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="a2e9d-118">3. példa: Növekményes másolási művelet kezdése a GetAzureStorageContainerből származó tároló prognózis használatával</span><span class="sxs-lookup"><span data-stu-id="a2e9d-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="a2e9d-119">Ez a parancs elindítja a Növekményes másolási műveletet a GetAzureStorageContainerből származó tároló prognózis használatával</span><span class="sxs-lookup"><span data-stu-id="a2e9d-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="a2e9d-120">4. példa: Növekményes másolási művelet indítása CloudPageBlob-objektumból cél blobnévvel</span><span class="sxs-lookup"><span data-stu-id="a2e9d-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="a2e9d-121">Ez a parancs elindítja a Növekményes másolási műveletet a CloudPageBlob objektumból a cél blobnévvel</span><span class="sxs-lookup"><span data-stu-id="a2e9d-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="a2e9d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2e9d-122">PARAMETERS</span></span>

### <span data-ttu-id="a2e9d-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="a2e9d-123">-AbsoluteUri</span></span>
<span data-ttu-id="a2e9d-124">Abszolút Uri a forráshoz.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-124">Absolute Uri to the source.</span></span> <span data-ttu-id="a2e9d-125">Ne feledje, hogy a hitelesítő adatokat meg kell adni az Uri azonosítóban, ha a forrás megköveteli.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a2e9d-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a2e9d-127">Az ügyféloldali maximális végrehajtási idő másodpercben az egyes kérések esetén.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-127">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a2e9d-128">-CloudBlob</span></span>
<span data-ttu-id="a2e9d-129">CloudBlob-objektum az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="a2e9d-130">Létrehozhatja, vagy használhatja Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a2e9d-131">-CloudBlobContainer</span></span>
<span data-ttu-id="a2e9d-132">CloudBlobContainer-objektum az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="a2e9d-133">Létrehozhatja, vagy használhatja Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a2e9d-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a2e9d-135">Az egyidejű aszinkron feladatok teljes mennyisége.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="a2e9d-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-136">The default value is 10.</span></span>

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

### <span data-ttu-id="a2e9d-137">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a2e9d-137">-Context</span></span>
<span data-ttu-id="a2e9d-138">Forrás Azure-tárterület környezete.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-138">Source Azure Storage Context.</span></span> <span data-ttu-id="a2e9d-139">A parancsmagot New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e9d-140">-DefaultProfile</span></span>
<span data-ttu-id="a2e9d-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="a2e9d-142">-DestBlob</span></span>
<span data-ttu-id="a2e9d-143">Cél blobneve</span><span class="sxs-lookup"><span data-stu-id="a2e9d-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="a2e9d-144">-DestCloudBlob</span></span>
<span data-ttu-id="a2e9d-145">Destination CloudBlob objektum</span><span class="sxs-lookup"><span data-stu-id="a2e9d-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="a2e9d-146">-DestContainer</span></span>
<span data-ttu-id="a2e9d-147">Céltároló neve</span><span class="sxs-lookup"><span data-stu-id="a2e9d-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="a2e9d-148">-DestContext</span></span>
<span data-ttu-id="a2e9d-149">Cél Azure-tárterület környezete.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="a2e9d-150">A parancsmagot New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-150">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a2e9d-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a2e9d-152">A kiszolgáló másodpercek alatt időkorrektaidőt ad az egyes kérések számára.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-152">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="a2e9d-153">-SrcBlob</span></span>
<span data-ttu-id="a2e9d-154">Forráslap blobneve.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a2e9d-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="a2e9d-156">A forráslap blob-pillanatképének ideje.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="a2e9d-157">-SrcContainer</span></span>
<span data-ttu-id="a2e9d-158">Forrástároló neve</span><span class="sxs-lookup"><span data-stu-id="a2e9d-158">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9d-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2e9d-159">-Confirm</span></span>
<span data-ttu-id="a2e9d-160">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e9d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e9d-161">-WhatIf</span></span>
<span data-ttu-id="a2e9d-162">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2e9d-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e9d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e9d-164">CommonParameters</span></span>
<span data-ttu-id="a2e9d-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2e9d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e9d-166">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e9d-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e9d-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2e9d-167">INPUTS</span></span>

### <span data-ttu-id="a2e9d-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="a2e9d-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="a2e9d-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a2e9d-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a2e9d-170">System.String</span><span class="sxs-lookup"><span data-stu-id="a2e9d-170">System.String</span></span>

### <span data-ttu-id="a2e9d-171">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2e9d-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a2e9d-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e9d-172">OUTPUTS</span></span>

### <span data-ttu-id="a2e9d-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a2e9d-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a2e9d-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2e9d-174">NOTES</span></span>

## <span data-ttu-id="a2e9d-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2e9d-175">RELATED LINKS</span></span>
