---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
ms.openlocfilehash: fba71dbac836fb6cc6551982945135e8e9410744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493300"
---
# <span data-ttu-id="fac92-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="fac92-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="fac92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fac92-102">SYNOPSIS</span></span>
<span data-ttu-id="fac92-103">Az Azure Storage blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fac92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fac92-104">SYNTAX</span></span>

### <span data-ttu-id="fac92-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fac92-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fac92-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="fac92-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="fac92-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="fac92-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fac92-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fac92-108">DESCRIPTION</span></span>
<span data-ttu-id="fac92-109">A **Get-AzureStorageBlobCopyState** parancsmag az Azure Storage blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="fac92-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fac92-110">EXAMPLES</span></span>

### <span data-ttu-id="fac92-111">Példa 1: blob másolati állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fac92-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="fac92-112">Ez a parancs a ContosoPlanning2015 nevű blob másolati állapotát kapja meg a tároló ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="fac92-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="fac92-113">2. példa: a blob-objektum másolati állapotának beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="fac92-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="fac92-114">Ez a parancs a ContosoUploads nevű ContosoPlanning2015 a **Get-AzureStorageBlob** parancsmag használatával kapja meg az eredményét, majd átadja az eredményt az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="fac92-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fac92-115">A **Get-AzureStorageBlobCopyState** parancsmag az adott blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="fac92-116">3. példa: a másolati állapot beolvasása a tárolóban lévő blob-tárolóban a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="fac92-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="fac92-117">Ez a parancs a **Get-AzureStorageBlob** parancsmag használatával kapja meg a tárolót, és az eredményt átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fac92-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="fac92-118">A **Get-AzureStorageContainer** parancsmag a tárolóban lévő ContosoPlanning2015 nevű blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="fac92-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fac92-119">PARAMETERS</span></span>

### <span data-ttu-id="fac92-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="fac92-120">-Blob</span></span>
<span data-ttu-id="fac92-121">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="fac92-122">Ez a parancsmag beilleszti az Azure-tárterület blob-másolási műveletének állapotát, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac92-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fac92-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fac92-124">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="fac92-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fac92-125">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="fac92-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fac92-126">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="fac92-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fac92-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="fac92-127">-CloudBlob</span></span>
<span data-ttu-id="fac92-128">Egy **CloudBlob** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="fac92-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="fac92-129">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fac92-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="fac92-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="fac92-130">-CloudBlobContainer</span></span>
<span data-ttu-id="fac92-131">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="fac92-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="fac92-132">Ez a parancsmag a paraméter által megadott tárolóban lévő blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="fac92-133">**CloudBlobContainer** objektum beolvasásához használja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fac92-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="fac92-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fac92-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fac92-135">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fac92-136">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="fac92-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fac92-137">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="fac92-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fac92-138">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="fac92-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fac92-139">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="fac92-139">The default value is 10.</span></span>

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

### <span data-ttu-id="fac92-140">-Container</span><span class="sxs-lookup"><span data-stu-id="fac92-140">-Container</span></span>
<span data-ttu-id="fac92-141">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-141">Specifies the name of a container.</span></span>
<span data-ttu-id="fac92-142">Ez a parancsmag a paraméter által megadott tárolóban lévő blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac92-143">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fac92-143">-Context</span></span>
<span data-ttu-id="fac92-144">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac92-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fac92-145">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fac92-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fac92-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fac92-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fac92-147">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="fac92-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fac92-148">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="fac92-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fac92-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="fac92-149">-WaitForComplete</span></span>
<span data-ttu-id="fac92-150">Jelzi, hogy ez a parancsmag várja a másolat befejezését.</span><span class="sxs-lookup"><span data-stu-id="fac92-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="fac92-151">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadott eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="fac92-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="fac92-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac92-152">CommonParameters</span></span>
<span data-ttu-id="fac92-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fac92-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac92-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fac92-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac92-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac92-155">INPUTS</span></span>

### <span data-ttu-id="fac92-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fac92-156">IStorageContext</span></span>

<span data-ttu-id="fac92-157">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fac92-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="fac92-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac92-158">OUTPUTS</span></span>

### <span data-ttu-id="fac92-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="fac92-159">CopyState</span></span>

## <span data-ttu-id="fac92-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fac92-160">NOTES</span></span>

## <span data-ttu-id="fac92-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fac92-161">RELATED LINKS</span></span>

[<span data-ttu-id="fac92-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fac92-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="fac92-163">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fac92-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


