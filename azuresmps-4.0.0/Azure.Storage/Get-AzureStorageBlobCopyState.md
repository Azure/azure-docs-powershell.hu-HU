---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3191d7369597fbfb0781b550a57f0032f9aaad4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491741"
---
# <span data-ttu-id="a4e0a-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="a4e0a-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="a4e0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e0a-103">Az Azure Storage blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="a4e0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4e0a-104">SYNTAX</span></span>

### <span data-ttu-id="a4e0a-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4e0a-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a4e0a-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a4e0a-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4e0a-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a4e0a-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a4e0a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4e0a-108">DESCRIPTION</span></span>
<span data-ttu-id="a4e0a-109">A **Get-AzureStorageBlobCopyState** parancsmag az Azure Storage blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="a4e0a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a4e0a-110">EXAMPLES</span></span>

### <span data-ttu-id="a4e0a-111">Példa 1: blob másolati állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a4e0a-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="a4e0a-112">Ez a parancs a ContosoPlanning2015 nevű blob másolati állapotát kapja meg a tároló ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="a4e0a-113">2. példa: a blob-objektum másolati állapotának beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="a4e0a-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="a4e0a-114">Ez a parancs a ContosoUploads nevű ContosoPlanning2015 a **Get-AzureStorageBlob** parancsmag használatával kapja meg az eredményét, majd átadja az eredményt az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a4e0a-115">A **Get-AzureStorageBlobCopyState** parancsmag az adott blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="a4e0a-116">3. példa: a másolati állapot beolvasása a tárolóban lévő blob-tárolóban a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="a4e0a-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="a4e0a-117">Ez a parancs a **Get-AzureStorageBlob** parancsmag használatával kapja meg a tárolót, és az eredményt átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="a4e0a-118">A **Get-AzureStorageContainer** parancsmag a tárolóban lévő ContosoPlanning2015 nevű blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="a4e0a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4e0a-119">PARAMETERS</span></span>

### <span data-ttu-id="a4e0a-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a4e0a-120">-Blob</span></span>
<span data-ttu-id="a4e0a-121">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="a4e0a-122">Ez a parancsmag beilleszti az Azure-tárterület blob-másolási műveletének állapotát, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="a4e0a-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a4e0a-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a4e0a-124">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a4e0a-125">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a4e0a-126">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a4e0a-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-127">-CloudBlob</span></span>
<span data-ttu-id="a4e0a-128">Egy **CloudBlob** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="a4e0a-129">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a4e0a-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a4e0a-130">-CloudBlobContainer</span></span>
<span data-ttu-id="a4e0a-131">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a4e0a-132">Ez a parancsmag a paraméter által megadott tárolóban lévő blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="a4e0a-133">**CloudBlobContainer** objektum beolvasásához használja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="a4e0a-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a4e0a-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a4e0a-135">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a4e0a-136">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a4e0a-137">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a4e0a-138">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="a4e0a-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a4e0a-139">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-139">The default value is 10.</span></span>

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

### <span data-ttu-id="a4e0a-140">-Container</span><span class="sxs-lookup"><span data-stu-id="a4e0a-140">-Container</span></span>
<span data-ttu-id="a4e0a-141">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-141">Specifies the name of a container.</span></span>
<span data-ttu-id="a4e0a-142">Ez a parancsmag a paraméter által megadott tárolóban lévő blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="a4e0a-143">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a4e0a-143">-Context</span></span>
<span data-ttu-id="a4e0a-144">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a4e0a-145">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a4e0a-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a4e0a-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a4e0a-147">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a4e0a-148">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a4e0a-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="a4e0a-149">-WaitForComplete</span></span>
<span data-ttu-id="a4e0a-150">Jelzi, hogy ez a parancsmag várja a másolat befejezését.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="a4e0a-151">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadott eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="a4e0a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e0a-152">CommonParameters</span></span>
<span data-ttu-id="a4e0a-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4e0a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e0a-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e0a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e0a-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4e0a-155">INPUTS</span></span>

## <span data-ttu-id="a4e0a-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4e0a-156">OUTPUTS</span></span>

### <span data-ttu-id="a4e0a-157">CopyState</span><span class="sxs-lookup"><span data-stu-id="a4e0a-157">CopyState</span></span>

## <span data-ttu-id="a4e0a-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4e0a-158">NOTES</span></span>

## <span data-ttu-id="a4e0a-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4e0a-159">RELATED LINKS</span></span>

[<span data-ttu-id="a4e0a-160">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a4e0a-160">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="a4e0a-161">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a4e0a-161">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


