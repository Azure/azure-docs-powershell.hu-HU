---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 76af94e4ab2518a47fad03f31a2f0f24bb0d0422
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668673"
---
# <span data-ttu-id="c1b98-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c1b98-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="c1b98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1b98-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b98-103">Tárhely blobjának letöltése.</span><span class="sxs-lookup"><span data-stu-id="c1b98-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="c1b98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1b98-104">SYNTAX</span></span>

### <span data-ttu-id="c1b98-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1b98-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1b98-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="c1b98-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1b98-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="c1b98-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b98-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1b98-108">DESCRIPTION</span></span>
<span data-ttu-id="c1b98-109">A **Get-AzStorageBlobContent** parancsmag letölti a megadott tárterület-blobot.</span><span class="sxs-lookup"><span data-stu-id="c1b98-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="c1b98-110">Ha a blob-név nem érvényes a helyi számítógépen, ez a parancsmag automatikusan megoldja azt, ha lehetséges.</span><span class="sxs-lookup"><span data-stu-id="c1b98-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="c1b98-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c1b98-111">EXAMPLES</span></span>

### <span data-ttu-id="c1b98-112">1. példa: blob-tartalom letöltése név szerint</span><span class="sxs-lookup"><span data-stu-id="c1b98-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="c1b98-113">Ez a parancs a blobot név szerint tölti le.</span><span class="sxs-lookup"><span data-stu-id="c1b98-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="c1b98-114">2. példa: blob-tartalom letöltése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c1b98-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="c1b98-115">Ez a parancs a futószalag tartalmát a blob-tartalom megtalálásához és letöltéséhez használja.</span><span class="sxs-lookup"><span data-stu-id="c1b98-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="c1b98-116">3. példa: blob-tartalom letöltése a csővezeték és egy helyettesítő karakter használatával</span><span class="sxs-lookup"><span data-stu-id="c1b98-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="c1b98-117">Ez a példa a csillagokkal behelyettesített helyettesítő karaktert és a csővezetéket használja a blob-tartalom megkereséséhez és letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="c1b98-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="c1b98-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1b98-118">PARAMETERS</span></span>

### <span data-ttu-id="c1b98-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1b98-119">-AsJob</span></span>
<span data-ttu-id="c1b98-120">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="c1b98-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c1b98-121">-BLOB</span><span class="sxs-lookup"><span data-stu-id="c1b98-121">-Blob</span></span>
<span data-ttu-id="c1b98-122">A letöltendő blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1b98-122">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="c1b98-123">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="c1b98-123">-CheckMd5</span></span>
<span data-ttu-id="c1b98-124">Itt adhatja meg, hogy a letöltött fájlhoz tartozó Md5-összeget szeretné-e ellenőrizni.</span><span class="sxs-lookup"><span data-stu-id="c1b98-124">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="c1b98-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1b98-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c1b98-126">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="c1b98-126">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c1b98-127">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="c1b98-127">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c1b98-128">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="c1b98-128">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c1b98-129">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c1b98-129">-CloudBlob</span></span>
<span data-ttu-id="c1b98-130">Felhőbeli blobot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c1b98-130">Specifies a cloud blob.</span></span>
<span data-ttu-id="c1b98-131">**CloudBlob** objektum beolvasásához használja az Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c1b98-131">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="c1b98-132">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c1b98-132">-CloudBlobContainer</span></span>
<span data-ttu-id="c1b98-133">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="c1b98-133">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="c1b98-134">Létrehozhatja vagy használhatja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c1b98-134">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="c1b98-135">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c1b98-135">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c1b98-136">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1b98-136">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c1b98-137">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="c1b98-137">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c1b98-138">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="c1b98-138">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c1b98-139">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="c1b98-139">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c1b98-140">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c1b98-140">The default value is 10.</span></span>
<span data-ttu-id="c1b98-141">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c1b98-141">The default value is 10.</span></span>

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

### <span data-ttu-id="c1b98-142">-Container</span><span class="sxs-lookup"><span data-stu-id="c1b98-142">-Container</span></span>
<span data-ttu-id="c1b98-143">Annak a tárolónak a nevét adja meg, amelynek a blobját le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="c1b98-143">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="c1b98-144">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c1b98-144">-Context</span></span>
<span data-ttu-id="c1b98-145">Azt az Azure-tárterületet adja meg, amelyből a blob-tartalmat le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="c1b98-145">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="c1b98-146">A New-AzStorageContext parancsmagot használhatja a tárolási környezet létrehozására.</span><span class="sxs-lookup"><span data-stu-id="c1b98-146">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="c1b98-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b98-147">-DefaultProfile</span></span>
<span data-ttu-id="c1b98-148">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1b98-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1b98-149">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="c1b98-149">-Destination</span></span>
<span data-ttu-id="c1b98-150">A letöltött fájl tárolási helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1b98-150">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="c1b98-151">-Force</span><span class="sxs-lookup"><span data-stu-id="c1b98-151">-Force</span></span>
<span data-ttu-id="c1b98-152">Felülír egy meglévő fájlt megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="c1b98-152">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="c1b98-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1b98-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c1b98-154">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="c1b98-154">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c1b98-155">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="c1b98-155">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c1b98-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1b98-156">-Confirm</span></span>
<span data-ttu-id="c1b98-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1b98-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1b98-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b98-158">-WhatIf</span></span>
<span data-ttu-id="c1b98-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1b98-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1b98-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1b98-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1b98-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b98-161">CommonParameters</span></span>
<span data-ttu-id="c1b98-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1b98-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b98-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b98-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b98-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1b98-164">INPUTS</span></span>

### <span data-ttu-id="c1b98-165">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c1b98-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c1b98-166">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c1b98-166">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="c1b98-167">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1b98-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1b98-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1b98-168">OUTPUTS</span></span>

### <span data-ttu-id="c1b98-169">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c1b98-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c1b98-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1b98-170">NOTES</span></span>
* <span data-ttu-id="c1b98-171">Ha a blob-név nem érvényes a helyi számítógépen, akkor ez a parancsmag azt észleli, hogy lehetséges-e.</span><span class="sxs-lookup"><span data-stu-id="c1b98-171">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="c1b98-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1b98-172">RELATED LINKS</span></span>

[<span data-ttu-id="c1b98-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c1b98-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="c1b98-174">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c1b98-174">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c1b98-175">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c1b98-175">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
