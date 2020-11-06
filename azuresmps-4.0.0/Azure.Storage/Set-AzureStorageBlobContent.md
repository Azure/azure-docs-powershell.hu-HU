---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491673"
---
# <span data-ttu-id="70cc1-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="70cc1-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="70cc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="70cc1-103">Egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="70cc1-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="70cc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70cc1-104">SYNTAX</span></span>

### <span data-ttu-id="70cc1-105">SendManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70cc1-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70cc1-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="70cc1-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70cc1-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="70cc1-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70cc1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="70cc1-108">DESCRIPTION</span></span>
<span data-ttu-id="70cc1-109">A **set-AzureStorageBlobContent** parancsmag egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="70cc1-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="70cc1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="70cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="70cc1-111">1. példa: névvel ellátott fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="70cc1-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="70cc1-112">Ez a parancs feltölti a PlanningData nevű fájlt egy Planning2015 nevű blobtal.</span><span class="sxs-lookup"><span data-stu-id="70cc1-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="70cc1-113">2. példa: az aktuális mappa alatti fájlok feltöltése</span><span class="sxs-lookup"><span data-stu-id="70cc1-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="70cc1-114">Ez a parancs az alapszintű Windows PowerShell-parancsmagot használja Get-ChildItem az aktuális mappában és az almappákban lévő összes fájl letöltéséhez, majd a csővezeték-kezelő használatával átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="70cc1-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="70cc1-115">A **set-AzureStorageBlobContent** parancsmag a fájlokat a ContosoUploads nevű tárolóba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="70cc1-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="70cc1-116">3. példa: meglévő blob felülírása</span><span class="sxs-lookup"><span data-stu-id="70cc1-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="70cc1-117">Ez a parancs a Planning2015 nevű blobot az ContosoUploads-tárolóban kapja meg az Get-AzureStorageBlob parancsmag használatával, majd ezt a blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="70cc1-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="70cc1-118">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="70cc1-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="70cc1-119">Ez a parancs nem adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="70cc1-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="70cc1-120">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="70cc1-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="70cc1-121">Ha jóváhagyja a parancsot, a parancsmag felülírja a meglévő blobot.</span><span class="sxs-lookup"><span data-stu-id="70cc1-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="70cc1-122">4. példa: fájlok feltöltése tárolóba a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="70cc1-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="70cc1-123">Ez a parancs a **Get-AzureStorageContainer** parancsmaggal kezdődően a karakterlánc ContosoUpload kezdődő tárolót kapja, majd az adott blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="70cc1-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="70cc1-124">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="70cc1-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="70cc1-125">Példa 5: fájl és metaadatok feltöltése</span><span class="sxs-lookup"><span data-stu-id="70cc1-125">Example 5: Upload a file and metadata</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

<span data-ttu-id="70cc1-126">Az első parancs létrehoz egy hash-táblázatot, amely egy blob metaadatait tartalmazza, és a hash-táblázatot a $Metadata változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="70cc1-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="70cc1-127">A második parancs feltölti a ContosoPlanning nevű fájlt a ContosoUploads nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="70cc1-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="70cc1-128">A blob a $Metadataban tárolt metaadatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="70cc1-128">The blob includes the metadata stored in $Metadata.</span></span>

## <span data-ttu-id="70cc1-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70cc1-129">PARAMETERS</span></span>

### <span data-ttu-id="70cc1-130">-BLOB</span><span class="sxs-lookup"><span data-stu-id="70cc1-130">-Blob</span></span>
<span data-ttu-id="70cc1-131">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="70cc1-132">Ez a parancsmag olyan fájlt tölt fel az Azure Storage blob szolgáltatásba, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="70cc1-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="70cc1-133">-BlobType</span></span>
<span data-ttu-id="70cc1-134">A parancsmag által feltöltött blob típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="70cc1-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="70cc1-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="70cc1-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70cc1-136">Letiltása</span><span class="sxs-lookup"><span data-stu-id="70cc1-136">Block</span></span>
- <span data-ttu-id="70cc1-137">Lap</span><span class="sxs-lookup"><span data-stu-id="70cc1-137">Page</span></span>

<span data-ttu-id="70cc1-138">Az alapértelmezett érték a blokk.</span><span class="sxs-lookup"><span data-stu-id="70cc1-138">The default value is Block.</span></span>

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

### <span data-ttu-id="70cc1-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="70cc1-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="70cc1-140">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="70cc1-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="70cc1-141">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="70cc1-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="70cc1-142">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="70cc1-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="70cc1-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="70cc1-143">-CloudBlob</span></span>
<span data-ttu-id="70cc1-144">Egy **CloudBlob** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="70cc1-145">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70cc1-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="70cc1-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="70cc1-146">-CloudBlobContainer</span></span>
<span data-ttu-id="70cc1-147">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="70cc1-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="70cc1-148">Ez a parancsmag feltölti a tartalmat a tárolóban lévő blobra, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="70cc1-149">**CloudBlobContainer** objektum beolvasásához használja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70cc1-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="70cc1-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="70cc1-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="70cc1-151">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="70cc1-152">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="70cc1-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="70cc1-153">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="70cc1-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="70cc1-154">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="70cc1-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="70cc1-155">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="70cc1-155">The default value is 10.</span></span>

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

### <span data-ttu-id="70cc1-156">-Container</span><span class="sxs-lookup"><span data-stu-id="70cc1-156">-Container</span></span>
<span data-ttu-id="70cc1-157">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-157">Specifies the name of a container.</span></span>
<span data-ttu-id="70cc1-158">Ez a parancsmag a paraméter által megadott tárolóban lévő blobra tölti fel a fájlt.</span><span class="sxs-lookup"><span data-stu-id="70cc1-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="70cc1-159">-Környezet</span><span class="sxs-lookup"><span data-stu-id="70cc1-159">-Context</span></span>
<span data-ttu-id="70cc1-160">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="70cc1-161">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70cc1-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="70cc1-162">-Fájl</span><span class="sxs-lookup"><span data-stu-id="70cc1-162">-File</span></span>
<span data-ttu-id="70cc1-163">Annak a fájlnak a helyi elérési útját adja meg, amely blob-fájlként tölthető fel.</span><span class="sxs-lookup"><span data-stu-id="70cc1-163">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="70cc1-164">-Force</span><span class="sxs-lookup"><span data-stu-id="70cc1-164">-Force</span></span>
<span data-ttu-id="70cc1-165">Jelzi, hogy ez a parancsmag felülír egy meglévő blobot, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70cc1-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="70cc1-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="70cc1-166">-Metadata</span></span>
<span data-ttu-id="70cc1-167">A feltöltött blob metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-167">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="70cc1-168">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="70cc1-168">-Properties</span></span>
<span data-ttu-id="70cc1-169">A feltöltött blob tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="70cc1-169">Specifies properties for the uploaded blob.</span></span>

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

### <span data-ttu-id="70cc1-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="70cc1-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="70cc1-171">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="70cc1-171">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="70cc1-172">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="70cc1-172">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="70cc1-173">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70cc1-173">-Confirm</span></span>
<span data-ttu-id="70cc1-174">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70cc1-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70cc1-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70cc1-175">-WhatIf</span></span>
<span data-ttu-id="70cc1-176">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70cc1-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70cc1-177">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70cc1-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70cc1-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70cc1-178">CommonParameters</span></span>
<span data-ttu-id="70cc1-179">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70cc1-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70cc1-180">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70cc1-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70cc1-181">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70cc1-181">INPUTS</span></span>

## <span data-ttu-id="70cc1-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70cc1-182">OUTPUTS</span></span>

## <span data-ttu-id="70cc1-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70cc1-183">NOTES</span></span>

## <span data-ttu-id="70cc1-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70cc1-184">RELATED LINKS</span></span>

[<span data-ttu-id="70cc1-185">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="70cc1-185">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="70cc1-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="70cc1-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="70cc1-187">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="70cc1-187">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
