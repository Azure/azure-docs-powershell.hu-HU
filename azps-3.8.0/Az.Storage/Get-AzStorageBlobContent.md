---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 3f8c85ac8f6a93438176fb20acd98fdb84733927
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011241"
---
# <span data-ttu-id="3e3f1-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3e3f1-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="3e3f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3f1-103">Tárhely blobjának letöltése.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="3e3f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e3f1-104">SYNTAX</span></span>

### <span data-ttu-id="3e3f1-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e3f1-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e3f1-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="3e3f1-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e3f1-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="3e3f1-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e3f1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e3f1-108">DESCRIPTION</span></span>
<span data-ttu-id="3e3f1-109">A **Get-AzStorageBlobContent** parancsmag letölti a megadott tárterület-blobot.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="3e3f1-110">Ha a blob-név nem érvényes a helyi számítógépen, ez a parancsmag automatikusan megoldja azt, ha lehetséges.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="3e3f1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3e3f1-111">EXAMPLES</span></span>

### <span data-ttu-id="3e3f1-112">1. példa: blob-tartalom letöltése név szerint</span><span class="sxs-lookup"><span data-stu-id="3e3f1-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="3e3f1-113">Ez a parancs a blobot név szerint tölti le.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="3e3f1-114">2. példa: blob-tartalom letöltése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="3e3f1-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="3e3f1-115">Ez a parancs a futószalag tartalmát a blob-tartalom megtalálásához és letöltéséhez használja.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="3e3f1-116">3. példa: blob-tartalom letöltése a csővezeték és egy helyettesítő karakter használatával</span><span class="sxs-lookup"><span data-stu-id="3e3f1-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="3e3f1-117">Ez a példa a csillagokkal behelyettesített helyettesítő karaktert és a csővezetéket használja a blob-tartalom megkereséséhez és letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="3e3f1-118">Példa 4: blob-objektum beszerzése és mentése egy változóba, majd a blob-tartalom letöltése a blob-objektummal</span><span class="sxs-lookup"><span data-stu-id="3e3f1-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="3e3f1-119">Ez a példa először egy blob-objektumot kap, és egy változóban menti, majd letölti a blob-tartalmat a blob-objektummal.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="3e3f1-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e3f1-120">PARAMETERS</span></span>

### <span data-ttu-id="3e3f1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e3f1-121">-AsJob</span></span>
<span data-ttu-id="3e3f1-122">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3e3f1-123">-BLOB</span><span class="sxs-lookup"><span data-stu-id="3e3f1-123">-Blob</span></span>
<span data-ttu-id="3e3f1-124">A letöltendő blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3f1-125">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="3e3f1-125">-CheckMd5</span></span>
<span data-ttu-id="3e3f1-126">Itt adhatja meg, hogy a letöltött fájlhoz tartozó Md5-összeget szeretné-e ellenőrizni.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-126">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="3e3f1-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3e3f1-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3e3f1-128">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3e3f1-129">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3e3f1-130">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3e3f1-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3e3f1-131">-CloudBlob</span></span>
<span data-ttu-id="3e3f1-132">Felhőbeli blobot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-132">Specifies a cloud blob.</span></span>
<span data-ttu-id="3e3f1-133">**CloudBlob** objektum beolvasásához használja az Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3f1-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3e3f1-134">-CloudBlobContainer</span></span>
<span data-ttu-id="3e3f1-135">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-135">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="3e3f1-136">Létrehozhatja vagy használhatja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-136">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3f1-137">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3e3f1-137">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3e3f1-138">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-138">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3e3f1-139">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-139">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3e3f1-140">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-140">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3e3f1-141">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="3e3f1-141">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3e3f1-142">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-142">The default value is 10.</span></span>

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

### <span data-ttu-id="3e3f1-143">-Container</span><span class="sxs-lookup"><span data-stu-id="3e3f1-143">-Container</span></span>
<span data-ttu-id="3e3f1-144">Annak a tárolónak a nevét adja meg, amelynek a blobját le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-144">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3f1-145">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3e3f1-145">-Context</span></span>
<span data-ttu-id="3e3f1-146">Azt az Azure-tárterületet adja meg, amelyből a blob-tartalmat le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-146">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="3e3f1-147">A New-AzStorageContext parancsmagot használhatja a tárolási környezet létrehozására.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-147">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3f1-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e3f1-148">-DefaultProfile</span></span>
<span data-ttu-id="3e3f1-149">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e3f1-150">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="3e3f1-150">-Destination</span></span>
<span data-ttu-id="3e3f1-151">A letöltött fájl tárolási helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-151">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3f1-152">-Force</span><span class="sxs-lookup"><span data-stu-id="3e3f1-152">-Force</span></span>
<span data-ttu-id="3e3f1-153">Felülír egy meglévő fájlt megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-153">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="3e3f1-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3e3f1-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3e3f1-155">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3e3f1-156">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3e3f1-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e3f1-157">-Confirm</span></span>
<span data-ttu-id="3e3f1-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e3f1-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e3f1-159">-WhatIf</span></span>
<span data-ttu-id="3e3f1-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e3f1-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e3f1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3f1-162">CommonParameters</span></span>
<span data-ttu-id="3e3f1-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e3f1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3f1-164">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e3f1-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3f1-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e3f1-165">INPUTS</span></span>

### <span data-ttu-id="3e3f1-166">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3e3f1-166">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="3e3f1-167">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3e3f1-167">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="3e3f1-168">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3e3f1-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3e3f1-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e3f1-169">OUTPUTS</span></span>

### <span data-ttu-id="3e3f1-170">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3e3f1-170">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="3e3f1-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e3f1-171">NOTES</span></span>
* <span data-ttu-id="3e3f1-172">Ha a blob-név nem érvényes a helyi számítógépen, akkor ez a parancsmag azt észleli, hogy lehetséges-e.</span><span class="sxs-lookup"><span data-stu-id="3e3f1-172">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="3e3f1-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e3f1-173">RELATED LINKS</span></span>

[<span data-ttu-id="3e3f1-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3e3f1-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="3e3f1-175">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3e3f1-175">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="3e3f1-176">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3e3f1-176">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
