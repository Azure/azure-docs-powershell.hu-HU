---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 979cfd1241910cb98bebee3b80bc0a1ab6b8da71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195029"
---
# <span data-ttu-id="937f9-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="937f9-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="937f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="937f9-102">SYNOPSIS</span></span>
<span data-ttu-id="937f9-103">Leállít egy másolási műveletet.</span><span class="sxs-lookup"><span data-stu-id="937f9-103">Stops a copy operation.</span></span>

## <span data-ttu-id="937f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="937f9-104">SYNTAX</span></span>

### <span data-ttu-id="937f9-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="937f9-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="937f9-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="937f9-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="937f9-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="937f9-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="937f9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="937f9-108">DESCRIPTION</span></span>
<span data-ttu-id="937f9-109">A **stop-AzStorageBlobCopy** parancsmag leállítja a másolási műveletet a megadott cél blobra.</span><span class="sxs-lookup"><span data-stu-id="937f9-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="937f9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="937f9-110">EXAMPLES</span></span>

### <span data-ttu-id="937f9-111">Példa 1: a másolási művelet leállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="937f9-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="937f9-112">Ez a parancs a másolási műveletet leállítja név szerint.</span><span class="sxs-lookup"><span data-stu-id="937f9-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="937f9-113">2. példa: a másolási művelet leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="937f9-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="937f9-114">Ez a parancs leállítja a másolási műveletet, ha a tárolót a futószalagról a **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="937f9-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="937f9-115">3. példa: a másolási művelet leállítása a csővezeték és a Get-AzStorageBlob segítségével</span><span class="sxs-lookup"><span data-stu-id="937f9-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="937f9-116">Ez a példa leállítja a másolási műveletet, ha a tárolót a Get-AzStorageBlob parancsmagból átadja.</span><span class="sxs-lookup"><span data-stu-id="937f9-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="937f9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="937f9-117">PARAMETERS</span></span>

### <span data-ttu-id="937f9-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="937f9-118">-Blob</span></span>
<span data-ttu-id="937f9-119">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="937f9-119">Specifies the name of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="937f9-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="937f9-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="937f9-121">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="937f9-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="937f9-122">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="937f9-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="937f9-123">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="937f9-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="937f9-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="937f9-124">-CloudBlob</span></span>
<span data-ttu-id="937f9-125">Egy **CloudBlob** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="937f9-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="937f9-126">**CloudBlob** objektum beolvasásához használja az Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="937f9-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="937f9-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="937f9-127">-CloudBlobContainer</span></span>
<span data-ttu-id="937f9-128">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="937f9-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="937f9-129">Létrehozhatja az objektumot, vagy használhatja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="937f9-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="937f9-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="937f9-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="937f9-131">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="937f9-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="937f9-132">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="937f9-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="937f9-133">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="937f9-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="937f9-134">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="937f9-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="937f9-135">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="937f9-135">The default value is 10.</span></span>

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

### <span data-ttu-id="937f9-136">-Container</span><span class="sxs-lookup"><span data-stu-id="937f9-136">-Container</span></span>
<span data-ttu-id="937f9-137">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="937f9-137">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="937f9-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="937f9-138">-Context</span></span>
<span data-ttu-id="937f9-139">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="937f9-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="937f9-140">A környezetet az New-AzStorageContext parancsmag használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="937f9-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="937f9-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="937f9-141">-CopyId</span></span>
<span data-ttu-id="937f9-142">A másolat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="937f9-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="937f9-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937f9-143">-DefaultProfile</span></span>
<span data-ttu-id="937f9-144">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="937f9-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="937f9-145">-Force</span><span class="sxs-lookup"><span data-stu-id="937f9-145">-Force</span></span>
<span data-ttu-id="937f9-146">Az aktuális másolási feladat leállítása a megadott blobra a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="937f9-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="937f9-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="937f9-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="937f9-148">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="937f9-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="937f9-149">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="937f9-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="937f9-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="937f9-150">-Confirm</span></span>
<span data-ttu-id="937f9-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="937f9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937f9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937f9-152">-WhatIf</span></span>
<span data-ttu-id="937f9-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="937f9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="937f9-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="937f9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="937f9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937f9-155">CommonParameters</span></span>
<span data-ttu-id="937f9-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="937f9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937f9-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937f9-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937f9-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="937f9-158">INPUTS</span></span>

### <span data-ttu-id="937f9-159">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="937f9-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="937f9-160">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="937f9-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="937f9-161">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="937f9-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="937f9-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="937f9-162">OUTPUTS</span></span>

### <span data-ttu-id="937f9-163">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="937f9-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="937f9-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="937f9-164">NOTES</span></span>

## <span data-ttu-id="937f9-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="937f9-165">RELATED LINKS</span></span>

[<span data-ttu-id="937f9-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="937f9-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="937f9-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="937f9-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="937f9-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="937f9-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="937f9-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="937f9-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)