---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobincrementalcopy
schema: 2.0.0
ms.openlocfilehash: 3007dadcdca2494a3f0412fbb4caead3421d2bf9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850949"
---
# <span data-ttu-id="f71a2-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="f71a2-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="f71a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f71a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f71a2-103">Egy növekményes másolási művelet elindítása egy blob-pillanatképből a megadott rendeltetési lapra blob-ra.</span><span class="sxs-lookup"><span data-stu-id="f71a2-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f71a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f71a2-104">SYNTAX</span></span>

### <span data-ttu-id="f71a2-105">ContainerInstance (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f71a2-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f71a2-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="f71a2-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f71a2-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="f71a2-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f71a2-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="f71a2-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f71a2-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="f71a2-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f71a2-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="f71a2-110">DESCRIPTION</span></span>
<span data-ttu-id="f71a2-111">Egy növekményes másolási művelet elindítása egy blob-pillanatképből a megadott rendeltetési lapra blob-ra.</span><span class="sxs-lookup"><span data-stu-id="f71a2-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="f71a2-112">További információ a funkcióról https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="f71a2-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="f71a2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f71a2-113">EXAMPLES</span></span>

### <span data-ttu-id="f71a2-114">1. példa: a növekményes másolási művelet elindítása blob-név és pillanatkép-időpont szerint</span><span class="sxs-lookup"><span data-stu-id="f71a2-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="f71a2-115">Ez a parancs a növekményes másolási műveletet a blob-név és a pillanatkép-idő segítségével indítja el.</span><span class="sxs-lookup"><span data-stu-id="f71a2-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="f71a2-116">2. példa: a növekményes másolási művelet elindítása a Source URI-val</span><span class="sxs-lookup"><span data-stu-id="f71a2-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="f71a2-117">Ez a parancs a növekményes másolási műveletet a forrás URI azonosítóval indítja el.</span><span class="sxs-lookup"><span data-stu-id="f71a2-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="f71a2-118">3. példa: a növekményes másolási művelet elindítása a GetAzureStorageContainer származó tároló-csővezetéken</span><span class="sxs-lookup"><span data-stu-id="f71a2-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="f71a2-119">Ez a parancs a növekményes másolási műveletet a GetAzureStorageContainer-ról tároló csővezetéken keresztül indítja el.</span><span class="sxs-lookup"><span data-stu-id="f71a2-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="f71a2-120">Példa 4: a növekményes másolási művelet elindítása a CloudPageBlob objektumról a cél blob-ra blob néven</span><span class="sxs-lookup"><span data-stu-id="f71a2-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="f71a2-121">Ez a parancs a növekményes másolási műveletet a CloudPageBlob objektumról a cél blobra, a blob nevű névvel indítja el.</span><span class="sxs-lookup"><span data-stu-id="f71a2-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="f71a2-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f71a2-122">PARAMETERS</span></span>

### <span data-ttu-id="f71a2-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="f71a2-123">-AbsoluteUri</span></span>
<span data-ttu-id="f71a2-124">Az abszolút URI a forráshoz.</span><span class="sxs-lookup"><span data-stu-id="f71a2-124">Absolute Uri to the source.</span></span> <span data-ttu-id="f71a2-125">Felhívjuk a figyelmét arra, hogy a hitelesítő adatokat meg kell adni az URI-ban, ha a forrás szükséges.</span><span class="sxs-lookup"><span data-stu-id="f71a2-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="f71a2-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f71a2-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f71a2-127">Az ügyféloldali kérelmek maximális végrehajtási ideje másodpercben.</span><span class="sxs-lookup"><span data-stu-id="f71a2-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="f71a2-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f71a2-128">-CloudBlob</span></span>
<span data-ttu-id="f71a2-129">CloudBlob objektum az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="f71a2-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="f71a2-130">Létrehozhatja vagy használhatja Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f71a2-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f71a2-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f71a2-131">-CloudBlobContainer</span></span>
<span data-ttu-id="f71a2-132">CloudBlobContainer objektum az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="f71a2-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="f71a2-133">Létrehozhatja vagy használhatja Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f71a2-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f71a2-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f71a2-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f71a2-135">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="f71a2-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="f71a2-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="f71a2-136">The default value is 10.</span></span>

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

### <span data-ttu-id="f71a2-137">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f71a2-137">-Context</span></span>
<span data-ttu-id="f71a2-138">Forrás Azure Storage Context.</span><span class="sxs-lookup"><span data-stu-id="f71a2-138">Source Azure Storage Context.</span></span> <span data-ttu-id="f71a2-139">New-AzureStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="f71a2-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f71a2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71a2-140">-DefaultProfile</span></span>
<span data-ttu-id="f71a2-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f71a2-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f71a2-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="f71a2-142">-DestBlob</span></span>
<span data-ttu-id="f71a2-143">A cél blob neve</span><span class="sxs-lookup"><span data-stu-id="f71a2-143">Destination blob name</span></span>

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

### <span data-ttu-id="f71a2-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="f71a2-144">-DestCloudBlob</span></span>
<span data-ttu-id="f71a2-145">Cél CloudBlob objektum</span><span class="sxs-lookup"><span data-stu-id="f71a2-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f71a2-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="f71a2-146">-DestContainer</span></span>
<span data-ttu-id="f71a2-147">Cél tárolójának neve</span><span class="sxs-lookup"><span data-stu-id="f71a2-147">Destination container name</span></span>

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

### <span data-ttu-id="f71a2-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="f71a2-148">-DestContext</span></span>
<span data-ttu-id="f71a2-149">Cél Azure tárolási környezet</span><span class="sxs-lookup"><span data-stu-id="f71a2-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="f71a2-150">New-AzureStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="f71a2-150">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f71a2-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f71a2-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f71a2-152">A kiszolgáló az egyes kérésekhez másodpercben megadott időpontot.</span><span class="sxs-lookup"><span data-stu-id="f71a2-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="f71a2-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="f71a2-153">-SrcBlob</span></span>
<span data-ttu-id="f71a2-154">A forrás lap blob neve.</span><span class="sxs-lookup"><span data-stu-id="f71a2-154">Source page blob name.</span></span>

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

### <span data-ttu-id="f71a2-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="f71a2-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="f71a2-156">A forrás lap blob-pillanatfelvételének ideje.</span><span class="sxs-lookup"><span data-stu-id="f71a2-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="f71a2-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="f71a2-157">-SrcContainer</span></span>
<span data-ttu-id="f71a2-158">A forrás tároló neve</span><span class="sxs-lookup"><span data-stu-id="f71a2-158">Source Container name</span></span>

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

### <span data-ttu-id="f71a2-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f71a2-159">-Confirm</span></span>
<span data-ttu-id="f71a2-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f71a2-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f71a2-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f71a2-161">-WhatIf</span></span>
<span data-ttu-id="f71a2-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f71a2-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f71a2-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f71a2-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f71a2-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71a2-164">CommonParameters</span></span>
<span data-ttu-id="f71a2-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f71a2-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71a2-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f71a2-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71a2-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f71a2-167">INPUTS</span></span>

### <span data-ttu-id="f71a2-168">Microsoft. WindowsAzure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="f71a2-168">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="f71a2-169">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f71a2-169">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="f71a2-170">System. String</span><span class="sxs-lookup"><span data-stu-id="f71a2-170">System.String</span></span>

### <span data-ttu-id="f71a2-171">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f71a2-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f71a2-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f71a2-172">OUTPUTS</span></span>

### <span data-ttu-id="f71a2-173">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f71a2-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="f71a2-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f71a2-174">NOTES</span></span>

## <span data-ttu-id="f71a2-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f71a2-175">RELATED LINKS</span></span>
