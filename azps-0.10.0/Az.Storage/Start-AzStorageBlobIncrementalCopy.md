---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 28d0c33a1aa74b5c5f69670622cc12c48810906f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842834"
---
# <span data-ttu-id="be8ab-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="be8ab-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="be8ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="be8ab-103">Egy növekményes másolási művelet elindítása egy blob-pillanatképből a megadott rendeltetési lapra blob-ra.</span><span class="sxs-lookup"><span data-stu-id="be8ab-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="be8ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be8ab-104">SYNTAX</span></span>

### <span data-ttu-id="be8ab-105">ContainerInstance (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be8ab-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8ab-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="be8ab-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8ab-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="be8ab-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8ab-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="be8ab-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8ab-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="be8ab-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be8ab-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="be8ab-110">DESCRIPTION</span></span>
<span data-ttu-id="be8ab-111">Egy növekményes másolási művelet elindítása egy blob-pillanatképből a megadott rendeltetési lapra blob-ra.</span><span class="sxs-lookup"><span data-stu-id="be8ab-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="be8ab-112">További információ a funkcióról https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="be8ab-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="be8ab-113">Példák</span><span class="sxs-lookup"><span data-stu-id="be8ab-113">EXAMPLES</span></span>

### <span data-ttu-id="be8ab-114">1. példa: a növekményes másolási művelet elindítása blob-név és pillanatkép-időpont szerint</span><span class="sxs-lookup"><span data-stu-id="be8ab-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="be8ab-115">Ez a parancs a növekményes másolási műveletet a blob-név és a pillanatkép-idő segítségével indítja el.</span><span class="sxs-lookup"><span data-stu-id="be8ab-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="be8ab-116">2. példa: a növekményes másolási művelet elindítása a Source URI-val</span><span class="sxs-lookup"><span data-stu-id="be8ab-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="be8ab-117">Ez a parancs a növekményes másolási műveletet a forrás URI azonosítóval indítja el.</span><span class="sxs-lookup"><span data-stu-id="be8ab-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="be8ab-118">3. példa: a növekményes másolási művelet elindítása a GetAzureStorageContainer származó tároló-csővezetéken</span><span class="sxs-lookup"><span data-stu-id="be8ab-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="be8ab-119">Ez a parancs a növekményes másolási műveletet a GetAzureStorageContainer-ról tároló csővezetéken keresztül indítja el.</span><span class="sxs-lookup"><span data-stu-id="be8ab-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="be8ab-120">Példa 4: a növekményes másolási művelet elindítása a CloudPageBlob objektumról a cél blob-ra blob néven</span><span class="sxs-lookup"><span data-stu-id="be8ab-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="be8ab-121">Ez a parancs a növekményes másolási műveletet a CloudPageBlob objektumról a cél blobra, a blob nevű névvel indítja el.</span><span class="sxs-lookup"><span data-stu-id="be8ab-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="be8ab-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be8ab-122">PARAMETERS</span></span>

### <span data-ttu-id="be8ab-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="be8ab-123">-AbsoluteUri</span></span>
<span data-ttu-id="be8ab-124">Az abszolút URI a forráshoz.</span><span class="sxs-lookup"><span data-stu-id="be8ab-124">Absolute Uri to the source.</span></span> <span data-ttu-id="be8ab-125">Felhívjuk a figyelmét arra, hogy a hitelesítő adatokat meg kell adni az URI-ban, ha a forrás szükséges.</span><span class="sxs-lookup"><span data-stu-id="be8ab-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="be8ab-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="be8ab-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="be8ab-127">Az ügyféloldali kérelmek maximális végrehajtási ideje másodpercben.</span><span class="sxs-lookup"><span data-stu-id="be8ab-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="be8ab-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="be8ab-128">-CloudBlob</span></span>
<span data-ttu-id="be8ab-129">CloudBlob objektum az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="be8ab-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="be8ab-130">Létrehozhatja vagy használhatja Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="be8ab-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be8ab-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="be8ab-131">-CloudBlobContainer</span></span>
<span data-ttu-id="be8ab-132">CloudBlobContainer objektum az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="be8ab-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="be8ab-133">Létrehozhatja vagy használhatja Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="be8ab-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be8ab-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="be8ab-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="be8ab-135">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="be8ab-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="be8ab-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="be8ab-136">The default value is 10.</span></span>

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

### <span data-ttu-id="be8ab-137">-Környezet</span><span class="sxs-lookup"><span data-stu-id="be8ab-137">-Context</span></span>
<span data-ttu-id="be8ab-138">Forrás Azure Storage Context.</span><span class="sxs-lookup"><span data-stu-id="be8ab-138">Source Azure Storage Context.</span></span> <span data-ttu-id="be8ab-139">New-AzStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="be8ab-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="be8ab-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8ab-140">-DefaultProfile</span></span>
<span data-ttu-id="be8ab-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be8ab-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8ab-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="be8ab-142">-DestBlob</span></span>
<span data-ttu-id="be8ab-143">A cél blob neve</span><span class="sxs-lookup"><span data-stu-id="be8ab-143">Destination blob name</span></span>

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

### <span data-ttu-id="be8ab-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="be8ab-144">-DestCloudBlob</span></span>
<span data-ttu-id="be8ab-145">Cél CloudBlob objektum</span><span class="sxs-lookup"><span data-stu-id="be8ab-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8ab-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="be8ab-146">-DestContainer</span></span>
<span data-ttu-id="be8ab-147">Cél tárolójának neve</span><span class="sxs-lookup"><span data-stu-id="be8ab-147">Destination container name</span></span>

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

### <span data-ttu-id="be8ab-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="be8ab-148">-DestContext</span></span>
<span data-ttu-id="be8ab-149">Cél Azure tárolási környezet</span><span class="sxs-lookup"><span data-stu-id="be8ab-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="be8ab-150">New-AzStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="be8ab-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="be8ab-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="be8ab-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="be8ab-152">A kiszolgáló az egyes kérésekhez másodpercben megadott időpontot.</span><span class="sxs-lookup"><span data-stu-id="be8ab-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="be8ab-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="be8ab-153">-SrcBlob</span></span>
<span data-ttu-id="be8ab-154">A forrás lap blob neve.</span><span class="sxs-lookup"><span data-stu-id="be8ab-154">Source page blob name.</span></span>

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

### <span data-ttu-id="be8ab-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="be8ab-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="be8ab-156">A forrás lap blob-pillanatfelvételének ideje.</span><span class="sxs-lookup"><span data-stu-id="be8ab-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="be8ab-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="be8ab-157">-SrcContainer</span></span>
<span data-ttu-id="be8ab-158">A forrás tároló neve</span><span class="sxs-lookup"><span data-stu-id="be8ab-158">Source Container name</span></span>

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

### <span data-ttu-id="be8ab-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="be8ab-159">-Confirm</span></span>
<span data-ttu-id="be8ab-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="be8ab-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be8ab-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be8ab-161">-WhatIf</span></span>
<span data-ttu-id="be8ab-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="be8ab-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be8ab-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be8ab-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be8ab-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8ab-164">CommonParameters</span></span>
<span data-ttu-id="be8ab-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be8ab-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8ab-166">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be8ab-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8ab-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be8ab-167">INPUTS</span></span>

### <span data-ttu-id="be8ab-168">Microsoft. WindowsAz. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="be8ab-168">Microsoft.WindowsAz.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="be8ab-169">Microsoft. WindowsAz. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="be8ab-169">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="be8ab-170">System. String</span><span class="sxs-lookup"><span data-stu-id="be8ab-170">System.String</span></span>

### <span data-ttu-id="be8ab-171">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="be8ab-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="be8ab-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be8ab-172">OUTPUTS</span></span>

### <span data-ttu-id="be8ab-173">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="be8ab-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="be8ab-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be8ab-174">NOTES</span></span>

## <span data-ttu-id="be8ab-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be8ab-175">RELATED LINKS</span></span>
