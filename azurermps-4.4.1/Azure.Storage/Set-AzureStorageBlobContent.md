---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/a2772c13c7cb665d7485636044c46f8c9222fc68
ms.openlocfilehash: c7acda834cda53a86073692dc6c888ce2803d859
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503356"
---
# <span data-ttu-id="606c0-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="606c0-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="606c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="606c0-102">SYNOPSIS</span></span>
<span data-ttu-id="606c0-103">Egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="606c0-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="606c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="606c0-104">SYNTAX</span></span>

### <span data-ttu-id="606c0-105">SendManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="606c0-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="606c0-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="606c0-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="606c0-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="606c0-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="606c0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="606c0-108">DESCRIPTION</span></span>
<span data-ttu-id="606c0-109">A **set-AzureStorageBlobContent** parancsmag egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="606c0-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="606c0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="606c0-110">EXAMPLES</span></span>

### <span data-ttu-id="606c0-111">1. példa: névvel ellátott fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="606c0-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="606c0-112">Ez a parancs feltölti a PlanningData nevű fájlt egy Planning2015 nevű blobtal.</span><span class="sxs-lookup"><span data-stu-id="606c0-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="606c0-113">2. példa: az aktuális mappa alatti fájlok feltöltése</span><span class="sxs-lookup"><span data-stu-id="606c0-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="606c0-114">Ez a parancs az alapszintű Windows PowerShell-parancsmagot használja Get-ChildItem az aktuális mappában és az almappákban lévő összes fájl letöltéséhez, majd a csővezeték-kezelő használatával átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="606c0-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="606c0-115">A **set-AzureStorageBlobContent** parancsmag a fájlokat a ContosoUploads nevű tárolóba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="606c0-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="606c0-116">3. példa: meglévő blob felülírása</span><span class="sxs-lookup"><span data-stu-id="606c0-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="606c0-117">Ez a parancs a Planning2015 nevű blobot az ContosoUploads-tárolóban kapja meg az Get-AzureStorageBlob parancsmag használatával, majd ezt a blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="606c0-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="606c0-118">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="606c0-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="606c0-119">Ez a parancs nem adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="606c0-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="606c0-120">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="606c0-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="606c0-121">Ha jóváhagyja a parancsot, a parancsmag felülírja a meglévő blobot.</span><span class="sxs-lookup"><span data-stu-id="606c0-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="606c0-122">4. példa: fájlok feltöltése tárolóba a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="606c0-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="606c0-123">Ez a parancs a **Get-AzureStorageContainer** parancsmaggal kezdődően a karakterlánc ContosoUpload kezdődő tárolót kapja, majd az adott blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="606c0-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="606c0-124">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="606c0-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="606c0-125">5. példa: fájl feltöltése a lap blob-ba metaadatokkal és PremiumPageBlobTier mint P10</span><span class="sxs-lookup"><span data-stu-id="606c0-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="606c0-126">Az első parancs létrehoz egy hash-táblázatot, amely egy blob metaadatait tartalmazza, és a hash-táblázatot a $Metadata változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="606c0-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="606c0-127">A második parancs feltölti a ContosoPlanning nevű fájlt a ContosoUploads nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="606c0-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="606c0-128">A blob tartalmazza a $Metadataban tárolt metaadatokat, és a PremiumPageBlobTier a P10.</span><span class="sxs-lookup"><span data-stu-id="606c0-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

## <span data-ttu-id="606c0-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="606c0-129">PARAMETERS</span></span>

### <span data-ttu-id="606c0-130">-BLOB</span><span class="sxs-lookup"><span data-stu-id="606c0-130">-Blob</span></span>
<span data-ttu-id="606c0-131">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="606c0-132">Ez a parancsmag olyan fájlt tölt fel az Azure Storage blob szolgáltatásba, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="606c0-133">-BlobType</span></span>
<span data-ttu-id="606c0-134">A parancsmag által feltöltött blob típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="606c0-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="606c0-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="606c0-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="606c0-136">Letiltása</span><span class="sxs-lookup"><span data-stu-id="606c0-136">Block</span></span>
- <span data-ttu-id="606c0-137">Lap</span><span class="sxs-lookup"><span data-stu-id="606c0-137">Page</span></span>

<span data-ttu-id="606c0-138">Az alapértelmezett érték a blokk.</span><span class="sxs-lookup"><span data-stu-id="606c0-138">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="606c0-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="606c0-140">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="606c0-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="606c0-141">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="606c0-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="606c0-142">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="606c0-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="606c0-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="606c0-143">-CloudBlob</span></span>
<span data-ttu-id="606c0-144">Egy **CloudBlob** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="606c0-145">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="606c0-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="606c0-146">-CloudBlobContainer</span></span>
<span data-ttu-id="606c0-147">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="606c0-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="606c0-148">Ez a parancsmag feltölti a tartalmat a tárolóban lévő blobra, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="606c0-149">**CloudBlobContainer** objektum beolvasásához használja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="606c0-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="606c0-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="606c0-151">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="606c0-152">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="606c0-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="606c0-153">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="606c0-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="606c0-154">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="606c0-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="606c0-155">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="606c0-155">The default value is 10.</span></span>

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

### <span data-ttu-id="606c0-156">-Container</span><span class="sxs-lookup"><span data-stu-id="606c0-156">-Container</span></span>
<span data-ttu-id="606c0-157">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-157">Specifies the name of a container.</span></span>
<span data-ttu-id="606c0-158">Ez a parancsmag a paraméter által megadott tárolóban lévő blobra tölti fel a fájlt.</span><span class="sxs-lookup"><span data-stu-id="606c0-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-159">-Környezet</span><span class="sxs-lookup"><span data-stu-id="606c0-159">-Context</span></span>
<span data-ttu-id="606c0-160">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="606c0-161">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="606c0-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-162">-Fájl</span><span class="sxs-lookup"><span data-stu-id="606c0-162">-File</span></span>
<span data-ttu-id="606c0-163">Annak a fájlnak a helyi elérési útját adja meg, amely blob-fájlként tölthető fel.</span><span class="sxs-lookup"><span data-stu-id="606c0-163">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-164">-Force</span><span class="sxs-lookup"><span data-stu-id="606c0-164">-Force</span></span>
<span data-ttu-id="606c0-165">Jelzi, hogy ez a parancsmag felülír egy meglévő blobot, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="606c0-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="606c0-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="606c0-166">-Metadata</span></span>
<span data-ttu-id="606c0-167">A feltöltött blob metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-167">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-168">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="606c0-168">-PremiumPageBlobTier</span></span>
<span data-ttu-id="606c0-169">Lap blob-rétege</span><span class="sxs-lookup"><span data-stu-id="606c0-169">Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-170">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="606c0-170">-Properties</span></span>
<span data-ttu-id="606c0-171">A feltöltött blob tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="606c0-171">Specifies properties for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606c0-172">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="606c0-172">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="606c0-173">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="606c0-173">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="606c0-174">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="606c0-174">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="606c0-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="606c0-175">-Confirm</span></span>
<span data-ttu-id="606c0-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="606c0-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="606c0-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="606c0-177">-WhatIf</span></span>
<span data-ttu-id="606c0-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="606c0-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="606c0-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="606c0-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="606c0-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606c0-180">CommonParameters</span></span>
<span data-ttu-id="606c0-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="606c0-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606c0-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="606c0-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606c0-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="606c0-183">INPUTS</span></span>

### <span data-ttu-id="606c0-184">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="606c0-184">IStorageContext</span></span>

<span data-ttu-id="606c0-185">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="606c0-185">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="606c0-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="606c0-186">OUTPUTS</span></span>

### <span data-ttu-id="606c0-187">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="606c0-187">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="606c0-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="606c0-188">NOTES</span></span>

## <span data-ttu-id="606c0-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="606c0-189">RELATED LINKS</span></span>

[<span data-ttu-id="606c0-190">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="606c0-190">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="606c0-191">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="606c0-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="606c0-192">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="606c0-192">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
