---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc15650b9a3cf16b1448b5e971669fbd37733b94
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490332"
---
# <span data-ttu-id="b7fe9-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="b7fe9-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="b7fe9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fe9-103">Egy növekményes másolási művelet elindítása egy blob-pillanatképből a megadott rendeltetési lapra blob-ra.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="b7fe9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7fe9-104">SYNTAX</span></span>

### <span data-ttu-id="b7fe9-105">ContainerInstance (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7fe9-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b7fe9-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="b7fe9-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b7fe9-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="b7fe9-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b7fe9-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="b7fe9-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b7fe9-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="b7fe9-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b7fe9-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7fe9-110">DESCRIPTION</span></span>
<span data-ttu-id="b7fe9-111">Egy növekményes másolási művelet elindítása egy blob-pillanatképből a megadott rendeltetési lapra blob-ra.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="b7fe9-112">További információ a funkcióról https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="b7fe9-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="b7fe9-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b7fe9-113">EXAMPLES</span></span>

### <span data-ttu-id="b7fe9-114">1. példa: a növekményes másolási művelet elindítása blob-név és pillanatkép-időpont szerint</span><span class="sxs-lookup"><span data-stu-id="b7fe9-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="b7fe9-115">Ez a parancs a növekményes másolási műveletet a blob-név és a pillanatkép-idő segítségével indítja el.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="b7fe9-116">2. példa: a növekményes másolási művelet elindítása a Source URI-val</span><span class="sxs-lookup"><span data-stu-id="b7fe9-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="b7fe9-117">Ez a parancs a növekményes másolási műveletet a forrás URI azonosítóval indítja el.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="b7fe9-118">3. példa: a növekményes másolási művelet elindítása a GetAzureStorageContainer származó tároló-csővezetéken</span><span class="sxs-lookup"><span data-stu-id="b7fe9-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="b7fe9-119">Ez a parancs a növekményes másolási műveletet a GetAzureStorageContainer-ról tároló csővezetéken keresztül indítja el.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="b7fe9-120">Példa 4: a növekményes másolási művelet elindítása a CloudPageBlob objektumról a cél blob-ra blob néven</span><span class="sxs-lookup"><span data-stu-id="b7fe9-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="b7fe9-121">Ez a parancs a növekményes másolási műveletet a CloudPageBlob objektumról a cél blobra, a blob nevű névvel indítja el.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="b7fe9-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7fe9-122">PARAMETERS</span></span>

### <span data-ttu-id="b7fe9-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="b7fe9-123">-AbsoluteUri</span></span>
<span data-ttu-id="b7fe9-124">Az abszolút URI a forráshoz.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-124">Absolute Uri to the source.</span></span>
<span data-ttu-id="b7fe9-125">Felhívjuk a figyelmét arra, hogy a hitelesítő adatokat meg kell adni az URI-ban, ha a forrás szükséges.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7fe9-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b7fe9-127">Az ügyféloldali kérelmek maximális végrehajtási ideje másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-127">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b7fe9-128">-CloudBlob</span></span>
<span data-ttu-id="b7fe9-129">CloudBlob objektum az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-129">CloudBlob object from Azure Storage Client library.</span></span>
<span data-ttu-id="b7fe9-130">Létrehozhatja vagy használhatja Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b7fe9-131">-CloudBlobContainer</span></span>
<span data-ttu-id="b7fe9-132">CloudBlobContainer objektum az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-132">CloudBlobContainer object from Azure Storage Client library.</span></span>
<span data-ttu-id="b7fe9-133">Létrehozhatja vagy használhatja Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b7fe9-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b7fe9-135">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="b7fe9-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-136">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-137">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b7fe9-137">-Context</span></span>
<span data-ttu-id="b7fe9-138">Forrás Azure Storage Context.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-138">Source Azure Storage Context.</span></span>
<span data-ttu-id="b7fe9-139">New-AzureStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="b7fe9-140">-DestBlob</span></span>
<span data-ttu-id="b7fe9-141">A cél blob neve</span><span class="sxs-lookup"><span data-stu-id="b7fe9-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="b7fe9-142">-DestCloudBlob</span></span>
<span data-ttu-id="b7fe9-143">Cél CloudBlob objektum</span><span class="sxs-lookup"><span data-stu-id="b7fe9-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="b7fe9-144">-DestContainer</span></span>
<span data-ttu-id="b7fe9-145">Cél tárolójának neve</span><span class="sxs-lookup"><span data-stu-id="b7fe9-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-146">-DestContext</span><span class="sxs-lookup"><span data-stu-id="b7fe9-146">-DestContext</span></span>
<span data-ttu-id="b7fe9-147">Cél Azure tárolási környezet</span><span class="sxs-lookup"><span data-stu-id="b7fe9-147">Destination Azure Storage Context.</span></span>
<span data-ttu-id="b7fe9-148">New-AzureStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7fe9-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b7fe9-150">A kiszolgáló az egyes kérésekhez másodpercben megadott időpontot.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-150">The server time out for each request in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="b7fe9-151">-SrcBlob</span></span>
<span data-ttu-id="b7fe9-152">A forrás lap blob neve.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="b7fe9-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="b7fe9-154">A forrás lap blob-pillanatfelvételének ideje.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="b7fe9-155">-SrcContainer</span></span>
<span data-ttu-id="b7fe9-156">A forrás tároló neve</span><span class="sxs-lookup"><span data-stu-id="b7fe9-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7fe9-157">-Confirm</span></span>
<span data-ttu-id="b7fe9-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fe9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7fe9-159">-WhatIf</span></span>
<span data-ttu-id="b7fe9-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7fe9-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7fe9-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b7fe9-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7fe9-162">INPUTS</span></span>

### <span data-ttu-id="b7fe9-163">Microsoft. WindowsAzure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="b7fe9-163">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="b7fe9-164">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer System. String Microsoft. WindowsAzure. Command. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7fe9-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="b7fe9-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7fe9-165">OUTPUTS</span></span>

### <span data-ttu-id="b7fe9-166">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b7fe9-166">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b7fe9-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7fe9-167">NOTES</span></span>

## <span data-ttu-id="b7fe9-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7fe9-168">RELATED LINKS</span></span>

