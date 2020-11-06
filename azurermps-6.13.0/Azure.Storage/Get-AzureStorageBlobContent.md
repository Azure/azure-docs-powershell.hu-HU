---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
ms.openlocfilehash: c2b09edb37b142de6032b2479629e989ed5663b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500319"
---
# <span data-ttu-id="8b514-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8b514-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="8b514-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b514-102">SYNOPSIS</span></span>
<span data-ttu-id="8b514-103">Tárhely blobjának letöltése.</span><span class="sxs-lookup"><span data-stu-id="8b514-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b514-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b514-104">SYNTAX</span></span>

### <span data-ttu-id="8b514-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b514-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b514-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="8b514-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b514-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="8b514-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b514-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b514-108">DESCRIPTION</span></span>
<span data-ttu-id="8b514-109">A **Get-AzureStorageBlobContent** parancsmag letölti a megadott tárterület-blobot.</span><span class="sxs-lookup"><span data-stu-id="8b514-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="8b514-110">Ha a blob-név nem érvényes a helyi számítógépen, ez a parancsmag automatikusan megoldja azt, ha lehetséges.</span><span class="sxs-lookup"><span data-stu-id="8b514-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="8b514-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8b514-111">EXAMPLES</span></span>

### <span data-ttu-id="8b514-112">1. példa: blob-tartalom letöltése név szerint</span><span class="sxs-lookup"><span data-stu-id="8b514-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="8b514-113">Ez a parancs a blobot név szerint tölti le.</span><span class="sxs-lookup"><span data-stu-id="8b514-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="8b514-114">2. példa: blob-tartalom letöltése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="8b514-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="8b514-115">Ez a parancs a futószalag tartalmát a blob-tartalom megtalálásához és letöltéséhez használja.</span><span class="sxs-lookup"><span data-stu-id="8b514-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="8b514-116">3. példa: blob-tartalom letöltése a csővezeték és egy helyettesítő karakter használatával</span><span class="sxs-lookup"><span data-stu-id="8b514-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="8b514-117">Ez a példa a csillagokkal behelyettesített helyettesítő karaktert és a csővezetéket használja a blob-tartalom megkereséséhez és letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="8b514-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="8b514-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b514-118">PARAMETERS</span></span>

### <span data-ttu-id="8b514-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="8b514-119">-Blob</span></span>
<span data-ttu-id="8b514-120">A letöltendő blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b514-120">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="8b514-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="8b514-121">-CheckMd5</span></span>
<span data-ttu-id="8b514-122">Itt adhatja meg, hogy a letöltött fájlhoz tartozó Md5-összeget szeretné-e ellenőrizni.</span><span class="sxs-lookup"><span data-stu-id="8b514-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="8b514-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b514-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8b514-124">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="8b514-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8b514-125">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="8b514-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8b514-126">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="8b514-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b514-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8b514-127">-CloudBlob</span></span>
<span data-ttu-id="8b514-128">Felhőbeli blobot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8b514-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="8b514-129">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8b514-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b514-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8b514-130">-CloudBlobContainer</span></span>
<span data-ttu-id="8b514-131">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="8b514-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="8b514-132">Létrehozhatja vagy használhatja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8b514-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b514-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8b514-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8b514-134">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b514-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8b514-135">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="8b514-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8b514-136">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="8b514-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8b514-137">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="8b514-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8b514-138">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8b514-138">The default value is 10.</span></span>
<span data-ttu-id="8b514-139">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8b514-139">The default value is 10.</span></span>

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

### <span data-ttu-id="8b514-140">-Container</span><span class="sxs-lookup"><span data-stu-id="8b514-140">-Container</span></span>
<span data-ttu-id="8b514-141">Annak a tárolónak a nevét adja meg, amelynek a blobját le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="8b514-141">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="8b514-142">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8b514-142">-Context</span></span>
<span data-ttu-id="8b514-143">Azt az Azure-tárterületet adja meg, amelyből a blob-tartalmat le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="8b514-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="8b514-144">A New-AzureStorageContext parancsmagot használhatja a tárolási környezet létrehozására.</span><span class="sxs-lookup"><span data-stu-id="8b514-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="8b514-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b514-145">-DefaultProfile</span></span>
<span data-ttu-id="8b514-146">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b514-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b514-147">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="8b514-147">-Destination</span></span>
<span data-ttu-id="8b514-148">A letöltött fájl tárolási helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b514-148">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="8b514-149">-Force</span><span class="sxs-lookup"><span data-stu-id="8b514-149">-Force</span></span>
<span data-ttu-id="8b514-150">Felülír egy meglévő fájlt megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="8b514-150">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="8b514-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b514-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8b514-152">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="8b514-152">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8b514-153">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="8b514-153">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8b514-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b514-154">-Confirm</span></span>
<span data-ttu-id="8b514-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b514-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b514-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b514-156">-WhatIf</span></span>
<span data-ttu-id="8b514-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b514-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b514-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b514-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b514-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b514-159">CommonParameters</span></span>
<span data-ttu-id="8b514-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b514-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b514-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b514-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b514-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b514-162">INPUTS</span></span>

### <span data-ttu-id="8b514-163">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8b514-163">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="8b514-164">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8b514-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="8b514-165">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b514-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8b514-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b514-166">OUTPUTS</span></span>

### <span data-ttu-id="8b514-167">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8b514-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="8b514-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b514-168">NOTES</span></span>
* <span data-ttu-id="8b514-169">Ha a blob-név nem érvényes a helyi számítógépen, akkor ez a parancsmag azt észleli, hogy lehetséges-e.</span><span class="sxs-lookup"><span data-stu-id="8b514-169">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="8b514-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b514-170">RELATED LINKS</span></span>

[<span data-ttu-id="8b514-171">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8b514-171">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="8b514-172">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8b514-172">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="8b514-173">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8b514-173">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
