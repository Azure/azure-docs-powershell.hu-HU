---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bdb5a02f474f575f90406ad9026b4437194dffb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491774"
---
# <span data-ttu-id="2f54d-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2f54d-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="2f54d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f54d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f54d-103">Leállít egy másolási műveletet.</span><span class="sxs-lookup"><span data-stu-id="2f54d-103">Stops a copy operation.</span></span>

## <span data-ttu-id="2f54d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f54d-104">SYNTAX</span></span>

### <span data-ttu-id="2f54d-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f54d-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f54d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2f54d-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f54d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2f54d-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f54d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f54d-108">DESCRIPTION</span></span>
<span data-ttu-id="2f54d-109">A **stop-AzureStorageBlobCopy** parancsmag leállítja a másolási műveletet a megadott cél blobra.</span><span class="sxs-lookup"><span data-stu-id="2f54d-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="2f54d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f54d-110">EXAMPLES</span></span>

### <span data-ttu-id="2f54d-111">Példa 1: a másolási művelet leállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="2f54d-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="2f54d-112">Ez a parancs a másolási műveletet leállítja név szerint.</span><span class="sxs-lookup"><span data-stu-id="2f54d-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="2f54d-113">2. példa: a másolási művelet leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="2f54d-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="2f54d-114">Ez a parancs leállítja a másolási műveletet, ha a tárolót a futószalagról a **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="2f54d-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="2f54d-115">3. példa: a másolási művelet leállítása a csővezeték és a Get-AzureStorageBlob segítségével</span><span class="sxs-lookup"><span data-stu-id="2f54d-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="2f54d-116">Ez a példa leállítja a másolási műveletet, ha a tárolót a Get-AzureStorageBlob parancsmagból átadja.</span><span class="sxs-lookup"><span data-stu-id="2f54d-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="2f54d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f54d-117">PARAMETERS</span></span>

### <span data-ttu-id="2f54d-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2f54d-118">-Blob</span></span>
<span data-ttu-id="2f54d-119">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f54d-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="2f54d-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2f54d-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2f54d-121">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="2f54d-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2f54d-122">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="2f54d-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2f54d-123">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="2f54d-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2f54d-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2f54d-124">-CloudBlob</span></span>
<span data-ttu-id="2f54d-125">Egy **CloudBlob** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="2f54d-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="2f54d-126">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2f54d-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="2f54d-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2f54d-127">-CloudBlobContainer</span></span>
<span data-ttu-id="2f54d-128">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="2f54d-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2f54d-129">Létrehozhatja az objektumot, vagy használhatja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2f54d-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="2f54d-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2f54d-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2f54d-131">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f54d-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2f54d-132">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="2f54d-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2f54d-133">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="2f54d-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2f54d-134">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="2f54d-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2f54d-135">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="2f54d-135">The default value is 10.</span></span>

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

### <span data-ttu-id="2f54d-136">-Container</span><span class="sxs-lookup"><span data-stu-id="2f54d-136">-Container</span></span>
<span data-ttu-id="2f54d-137">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f54d-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="2f54d-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2f54d-138">-Context</span></span>
<span data-ttu-id="2f54d-139">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f54d-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2f54d-140">A környezetet az New-AzureStorageContext parancsmag használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="2f54d-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2f54d-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="2f54d-141">-CopyId</span></span>
<span data-ttu-id="2f54d-142">A másolat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f54d-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f54d-143">-Force</span><span class="sxs-lookup"><span data-stu-id="2f54d-143">-Force</span></span>
<span data-ttu-id="2f54d-144">Az aktuális másolási feladat leállítása a megadott blobra a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2f54d-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2f54d-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2f54d-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2f54d-146">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="2f54d-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2f54d-147">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="2f54d-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2f54d-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f54d-148">-Confirm</span></span>
<span data-ttu-id="2f54d-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f54d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f54d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f54d-150">-WhatIf</span></span>
<span data-ttu-id="2f54d-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f54d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f54d-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f54d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f54d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f54d-153">CommonParameters</span></span>
<span data-ttu-id="2f54d-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f54d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f54d-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f54d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f54d-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f54d-156">INPUTS</span></span>

## <span data-ttu-id="2f54d-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f54d-157">OUTPUTS</span></span>

## <span data-ttu-id="2f54d-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f54d-158">NOTES</span></span>

## <span data-ttu-id="2f54d-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f54d-159">RELATED LINKS</span></span>

[<span data-ttu-id="2f54d-160">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2f54d-160">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="2f54d-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2f54d-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="2f54d-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2f54d-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="2f54d-163">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="2f54d-163">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
