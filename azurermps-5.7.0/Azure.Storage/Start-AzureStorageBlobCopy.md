---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
ms.openlocfilehash: 054aa003752c27849c44eb00654313c395c255ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679308"
---
# <span data-ttu-id="87019-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="87019-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="87019-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87019-102">SYNOPSIS</span></span>
<span data-ttu-id="87019-103">Elindítja a blob másolását.</span><span class="sxs-lookup"><span data-stu-id="87019-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87019-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87019-104">SYNTAX</span></span>

### <span data-ttu-id="87019-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87019-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="87019-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="87019-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="87019-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-109">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="87019-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="87019-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="87019-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="87019-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="87019-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87019-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="87019-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87019-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="87019-115">DESCRIPTION</span></span>
<span data-ttu-id="87019-116">A **Start-AzureStorageBlobCopy** parancsmag a blob másolását indítja el.</span><span class="sxs-lookup"><span data-stu-id="87019-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="87019-117">Példák</span><span class="sxs-lookup"><span data-stu-id="87019-117">EXAMPLES</span></span>

### <span data-ttu-id="87019-118">Példa 1: elnevezett blob másolása</span><span class="sxs-lookup"><span data-stu-id="87019-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="87019-119">Ez a parancs elindítja a ContosoPlanning2015 nevű blob másolati műveletét a ContosoUploads nevű tárolótól a ContosoArchives nevű tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="87019-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="87019-120">2. példa: tároló beszerzése a másolandó festékfoltok megadásához</span><span class="sxs-lookup"><span data-stu-id="87019-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="87019-121">Ez a parancs a ContosoUploads nevű tárolót a **Get-AzureStorageContainer** parancsmaggal kapja meg, majd a tárolót átadja az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="87019-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87019-122">Ez a parancsmag elindítja a ContosoPlanning2015 nevű blob másolási műveletét.</span><span class="sxs-lookup"><span data-stu-id="87019-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="87019-123">Az előző parancsmag a forrás tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="87019-124">A *DestContainer* paraméter a ContosoArchives adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="87019-125">3. példa: az összes blobot beolvashatja egy tárolóba, és a vágólapra másolhatja őket</span><span class="sxs-lookup"><span data-stu-id="87019-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="87019-126">Ez a parancs a ContosoUploads nevű tárolóban lévő blobokat a **Get-AzureStorageBlob** parancsmag használatával kapja meg, majd a csővezeték-kezelő segítségével átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="87019-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87019-127">Ez a parancsmag elindítja a festékfoltok másolási műveletét a ContosoArchives nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="87019-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="87019-128">Példa 4: objektumként megadott blob másolása</span><span class="sxs-lookup"><span data-stu-id="87019-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="87019-129">Az első parancs a ContosoPlanning2015 nevű blobot kapja a ContosoUploads nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="87019-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="87019-130">A parancs az objektumot a $SrcBlob változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="87019-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="87019-131">A második parancs a ContosoPlanning2015Archived nevű blobot kapja a ContosoArchives nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="87019-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="87019-132">A parancs az objektumot a $DestBlob változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="87019-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="87019-133">Az utolsó parancs elindítja a másolási műveletet a forrás tárolóból a cél tárolóba.</span><span class="sxs-lookup"><span data-stu-id="87019-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="87019-134">A parancs normál képpont-jelöléssel adja meg a $SrcBlob **ICloudBlob** objektumait és a $DestBlob Blobs-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="87019-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="87019-135">Példa 5: blob másolása egy URI-ról</span><span class="sxs-lookup"><span data-stu-id="87019-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="87019-136">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a kulcsot a $Context változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="87019-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="87019-137">A második parancs átmásolja a fájlt a megadott URI-ról a ContosoArchive nevű tároló ContosoPlanning nevű blob-webhelyére.</span><span class="sxs-lookup"><span data-stu-id="87019-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="87019-138">A parancs a másolási műveletet a $Contextban tárolt környezetben indítja el.</span><span class="sxs-lookup"><span data-stu-id="87019-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="87019-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87019-139">PARAMETERS</span></span>

### <span data-ttu-id="87019-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="87019-140">-AbsoluteUri</span></span>
<span data-ttu-id="87019-141">Annak a fájlnak az abszolút URI-azonosítóját adja meg, amelyet az Azure Storage blob-ba szeretne másolni.</span><span class="sxs-lookup"><span data-stu-id="87019-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="87019-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87019-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="87019-143">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="87019-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="87019-144">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="87019-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="87019-145">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="87019-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="87019-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="87019-146">-CloudBlob</span></span>
<span data-ttu-id="87019-147">Egy **CloudBlob** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="87019-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="87019-148">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87019-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87019-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="87019-149">-CloudBlobContainer</span></span>
<span data-ttu-id="87019-150">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="87019-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="87019-151">Ez a parancsmag a paraméter által megadott tárolóból másolja a blobot.</span><span class="sxs-lookup"><span data-stu-id="87019-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="87019-152">**CloudBlobContainer** objektum beolvasásához használja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87019-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="87019-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="87019-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="87019-154">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="87019-155">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="87019-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="87019-156">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="87019-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="87019-157">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="87019-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="87019-158">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="87019-158">The default value is 10.</span></span>

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

### <span data-ttu-id="87019-159">-Környezet</span><span class="sxs-lookup"><span data-stu-id="87019-159">-Context</span></span>
<span data-ttu-id="87019-160">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="87019-161">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87019-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="87019-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="87019-162">-DestBlob</span></span>
<span data-ttu-id="87019-163">A cél blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="87019-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="87019-164">-DestCloudBlob</span></span>
<span data-ttu-id="87019-165">A cél **CloudBlob** objektum megadása</span><span class="sxs-lookup"><span data-stu-id="87019-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="87019-166">-DestContainer</span></span>
<span data-ttu-id="87019-167">A cél tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="87019-168">-DestContext</span></span>
<span data-ttu-id="87019-169">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="87019-170">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87019-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="87019-171">-Force</span><span class="sxs-lookup"><span data-stu-id="87019-171">-Force</span></span>
<span data-ttu-id="87019-172">Jelzi, hogy ez a parancsmag felülírja a cél blobját, nem kell megerősítést kérnie.</span><span class="sxs-lookup"><span data-stu-id="87019-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-173">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="87019-173">-PremiumPageBlobTier</span></span>
<span data-ttu-id="87019-174">Prémium oldal blob-réteg</span><span class="sxs-lookup"><span data-stu-id="87019-174">Premium Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87019-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="87019-176">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="87019-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="87019-177">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="87019-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="87019-178">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="87019-178">-SrcBlob</span></span>
<span data-ttu-id="87019-179">A forrás blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-179">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-180">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="87019-180">-SrcContainer</span></span>
<span data-ttu-id="87019-181">A forrás tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-181">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="87019-182">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="87019-182">-SrcDir</span></span>
<span data-ttu-id="87019-183">Egy **CloudFileDirectory** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="87019-183">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-184">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="87019-184">-SrcFile</span></span>
<span data-ttu-id="87019-185">Specifes egy **CloudFile** objektumot az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="87019-185">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="87019-186">Létrehozhatja vagy használhatja Get-AzureStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87019-186">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87019-187">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="87019-187">-SrcFilePath</span></span>
<span data-ttu-id="87019-188">A forrás-vagy a forrás-megosztás relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-188">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-189">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="87019-189">-SrcShare</span></span>
<span data-ttu-id="87019-190">Egy **CloudFileShare** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="87019-190">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="87019-191">Létrehozhatja vagy használhatja Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87019-191">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-192">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="87019-192">-SrcShareName</span></span>
<span data-ttu-id="87019-193">A forrás megosztása nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="87019-193">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87019-194">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87019-194">-Confirm</span></span>
<span data-ttu-id="87019-195">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87019-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87019-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87019-196">-WhatIf</span></span>
<span data-ttu-id="87019-197">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87019-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87019-198">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87019-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87019-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87019-199">CommonParameters</span></span>
<span data-ttu-id="87019-200">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87019-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87019-201">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87019-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87019-202">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87019-202">INPUTS</span></span>

### <span data-ttu-id="87019-203">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="87019-203">CloudBlob</span></span>

<span data-ttu-id="87019-204">A ' CloudBlob ' paraméter az "CloudBlob" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="87019-204">Parameter 'CloudBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="87019-205">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87019-205">IStorageContext</span></span>

<span data-ttu-id="87019-206">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="87019-206">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="87019-207">CloudFile</span><span class="sxs-lookup"><span data-stu-id="87019-207">CloudFile</span></span>

<span data-ttu-id="87019-208">A ' SrcFile ' paraméter az "CloudFile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="87019-208">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="87019-209">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87019-209">OUTPUTS</span></span>

### <span data-ttu-id="87019-210">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="87019-210">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="87019-211">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87019-211">NOTES</span></span>

## <span data-ttu-id="87019-212">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87019-212">RELATED LINKS</span></span>

[<span data-ttu-id="87019-213">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="87019-213">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="87019-214">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="87019-214">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
