---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: a990b168fcaf32deffd495b5eeb0f9a813f2f093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839086"
---
# <span data-ttu-id="cc938-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cc938-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="cc938-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc938-102">SYNOPSIS</span></span>
<span data-ttu-id="cc938-103">Elindítja a blob másolását.</span><span class="sxs-lookup"><span data-stu-id="cc938-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="cc938-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc938-104">SYNTAX</span></span>

### <span data-ttu-id="cc938-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc938-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc938-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="cc938-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc938-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="cc938-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc938-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cc938-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc938-109">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="cc938-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc938-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="cc938-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc938-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="cc938-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc938-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="cc938-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc938-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="cc938-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc938-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="cc938-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc938-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc938-115">DESCRIPTION</span></span>
<span data-ttu-id="cc938-116">A **Start-AzStorageBlobCopy** parancsmag a blob másolását indítja el.</span><span class="sxs-lookup"><span data-stu-id="cc938-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="cc938-117">Példák</span><span class="sxs-lookup"><span data-stu-id="cc938-117">EXAMPLES</span></span>

### <span data-ttu-id="cc938-118">Példa 1: elnevezett blob másolása</span><span class="sxs-lookup"><span data-stu-id="cc938-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="cc938-119">Ez a parancs elindítja a ContosoPlanning2015 nevű blob másolati műveletét a ContosoUploads nevű tárolótól a ContosoArchives nevű tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="cc938-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="cc938-120">2. példa: tároló beszerzése a másolandó festékfoltok megadásához</span><span class="sxs-lookup"><span data-stu-id="cc938-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="cc938-121">Ez a parancs a ContosoUploads nevű tárolót a **Get-AzStorageContainer** parancsmaggal kapja meg, majd a tárolót átadja az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="cc938-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cc938-122">Ez a parancsmag elindítja a ContosoPlanning2015 nevű blob másolási műveletét.</span><span class="sxs-lookup"><span data-stu-id="cc938-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="cc938-123">Az előző parancsmag a forrás tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="cc938-124">A *DestContainer* paraméter a ContosoArchives adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="cc938-125">3. példa: az összes blobot beolvashatja egy tárolóba, és a vágólapra másolhatja őket</span><span class="sxs-lookup"><span data-stu-id="cc938-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="cc938-126">Ez a parancs a ContosoUploads nevű tárolóban lévő blobokat a **Get-AzStorageBlob** parancsmag használatával kapja meg, majd a csővezeték-kezelő segítségével átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cc938-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cc938-127">Ez a parancsmag elindítja a festékfoltok másolási műveletét a ContosoArchives nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="cc938-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="cc938-128">Példa 4: objektumként megadott blob másolása</span><span class="sxs-lookup"><span data-stu-id="cc938-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="cc938-129">Az első parancs a ContosoPlanning2015 nevű blobot kapja a ContosoUploads nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="cc938-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="cc938-130">A parancs az objektumot a $SrcBlob változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc938-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="cc938-131">A második parancs a ContosoPlanning2015Archived nevű blobot kapja a ContosoArchives nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="cc938-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="cc938-132">A parancs az objektumot a $DestBlob változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc938-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="cc938-133">Az utolsó parancs elindítja a másolási műveletet a forrás tárolóból a cél tárolóba.</span><span class="sxs-lookup"><span data-stu-id="cc938-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="cc938-134">A parancs normál képpont-jelöléssel adja meg a $SrcBlob **ICloudBlob** objektumait és a $DestBlob Blobs-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="cc938-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="cc938-135">Példa 5: blob másolása egy URI-ról</span><span class="sxs-lookup"><span data-stu-id="cc938-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="cc938-136">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a kulcsot a $Context változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc938-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="cc938-137">A második parancs átmásolja a fájlt a megadott URI-ról a ContosoArchive nevű tároló ContosoPlanning nevű blob-webhelyére.</span><span class="sxs-lookup"><span data-stu-id="cc938-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="cc938-138">A parancs a másolási műveletet a $Contextban tárolt környezetben indítja el.</span><span class="sxs-lookup"><span data-stu-id="cc938-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="cc938-139">Példa 6: a blokk blob másolása a cél tárolóba egy új blob nevű névvel, valamint a cél blob-StandardBlobTier beállítása archívumként RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="cc938-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Archive
```

<span data-ttu-id="cc938-140">Ez a parancs elindítja a blokk blob másolási műveletét a cél tárolóba egy új blob nevű névvel, és beállítja a cél blob-StandardBlobTier az archívumként RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="cc938-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>

## <span data-ttu-id="cc938-141">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc938-141">PARAMETERS</span></span>

### <span data-ttu-id="cc938-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="cc938-142">-AbsoluteUri</span></span>
<span data-ttu-id="cc938-143">Annak a fájlnak az abszolút URI-azonosítóját adja meg, amelyet az Azure Storage blob-ba szeretne másolni.</span><span class="sxs-lookup"><span data-stu-id="cc938-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="cc938-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cc938-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cc938-145">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="cc938-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cc938-146">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="cc938-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cc938-147">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="cc938-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cc938-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc938-148">-CloudBlob</span></span>
<span data-ttu-id="cc938-149">Egy **CloudBlob** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cc938-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="cc938-150">**CloudBlob** objektum beolvasásához használja az Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc938-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cc938-151">-CloudBlobContainer</span></span>
<span data-ttu-id="cc938-152">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="cc938-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="cc938-153">Ez a parancsmag a paraméter által megadott tárolóból másolja a blobot.</span><span class="sxs-lookup"><span data-stu-id="cc938-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="cc938-154">**CloudBlobContainer** objektum beolvasásához használja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc938-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="cc938-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cc938-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cc938-156">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cc938-157">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="cc938-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cc938-158">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="cc938-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cc938-159">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="cc938-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cc938-160">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="cc938-160">The default value is 10.</span></span>

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

### <span data-ttu-id="cc938-161">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cc938-161">-Context</span></span>
<span data-ttu-id="cc938-162">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cc938-163">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc938-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="cc938-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc938-164">-DefaultProfile</span></span>
<span data-ttu-id="cc938-165">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc938-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc938-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="cc938-166">-DestBlob</span></span>
<span data-ttu-id="cc938-167">A cél blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-167">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="cc938-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc938-168">-DestCloudBlob</span></span>
<span data-ttu-id="cc938-169">A cél **CloudBlob** objektum megadása</span><span class="sxs-lookup"><span data-stu-id="cc938-169">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="cc938-170">-DestContainer</span></span>
<span data-ttu-id="cc938-171">A cél tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-171">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-172">-DestContext</span><span class="sxs-lookup"><span data-stu-id="cc938-172">-DestContext</span></span>
<span data-ttu-id="cc938-173">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cc938-174">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc938-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cc938-175">-Force</span><span class="sxs-lookup"><span data-stu-id="cc938-175">-Force</span></span>
<span data-ttu-id="cc938-176">Jelzi, hogy ez a parancsmag felülírja a cél blobját, nem kell megerősítést kérnie.</span><span class="sxs-lookup"><span data-stu-id="cc938-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cc938-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="cc938-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="cc938-178">Prémium oldal blob-réteg</span><span class="sxs-lookup"><span data-stu-id="cc938-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-179">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="cc938-179">-RehydratePriority</span></span>
<span data-ttu-id="cc938-180">BLOB-RehydratePriority letiltása</span><span class="sxs-lookup"><span data-stu-id="cc938-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="cc938-181">Annak a prioritásnak a meghatározása, amellyel az archivált blobot újrahidratálja.</span><span class="sxs-lookup"><span data-stu-id="cc938-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="cc938-182">Az érvényes értékek: magas/normál.</span><span class="sxs-lookup"><span data-stu-id="cc938-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cc938-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cc938-184">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="cc938-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="cc938-185">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="cc938-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="cc938-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="cc938-186">-SrcBlob</span></span>
<span data-ttu-id="cc938-187">A forrás blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-187">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="cc938-188">-SrcContainer</span></span>
<span data-ttu-id="cc938-189">A forrás tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-189">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="cc938-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="cc938-190">-SrcDir</span></span>
<span data-ttu-id="cc938-191">Egy **CloudFileDirectory** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cc938-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="cc938-192">-SrcFile</span></span>
<span data-ttu-id="cc938-193">Egy **CloudFile** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cc938-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="cc938-194">Létrehozhatja vagy használhatja Get-AzStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc938-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="cc938-195">-SrcFilePath</span></span>
<span data-ttu-id="cc938-196">A forrás-vagy a forrás-megosztás relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-196">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="cc938-197">-SrcShare</span></span>
<span data-ttu-id="cc938-198">Egy **CloudFileShare** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cc938-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="cc938-199">Létrehozhatja vagy használhatja Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc938-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-200">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="cc938-200">-SrcShareName</span></span>
<span data-ttu-id="cc938-201">A forrás megosztása nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc938-201">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-202">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="cc938-202">-StandardBlobTier</span></span>
<span data-ttu-id="cc938-203">BLOB-szint letiltása: az érvényes értékek a meleg/hűvös/Archívek.</span><span class="sxs-lookup"><span data-stu-id="cc938-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="cc938-204">Részletes tudnivalók https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="cc938-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="cc938-205">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc938-205">-Confirm</span></span>
<span data-ttu-id="cc938-206">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc938-206">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc938-207">-WhatIf</span></span>
<span data-ttu-id="cc938-208">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc938-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc938-209">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc938-209">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc938-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc938-210">CommonParameters</span></span>
<span data-ttu-id="cc938-211">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc938-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc938-212">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc938-212">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc938-213">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc938-213">INPUTS</span></span>

### <span data-ttu-id="cc938-214">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc938-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="cc938-215">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cc938-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="cc938-216">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="cc938-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="cc938-217">System. String</span><span class="sxs-lookup"><span data-stu-id="cc938-217">System.String</span></span>

### <span data-ttu-id="cc938-218">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc938-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cc938-219">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc938-219">OUTPUTS</span></span>

### <span data-ttu-id="cc938-220">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cc938-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="cc938-221">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc938-221">NOTES</span></span>

## <span data-ttu-id="cc938-222">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc938-222">RELATED LINKS</span></span>

[<span data-ttu-id="cc938-223">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="cc938-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="cc938-224">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cc938-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
