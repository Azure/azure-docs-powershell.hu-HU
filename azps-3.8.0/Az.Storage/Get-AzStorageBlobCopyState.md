---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 6f9b08b59ff4b89243a26442b793bf2cf70f73d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011236"
---
# <span data-ttu-id="d45fb-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="d45fb-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="d45fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d45fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d45fb-103">Az Azure Storage blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="d45fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d45fb-104">SYNTAX</span></span>

### <span data-ttu-id="d45fb-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d45fb-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d45fb-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="d45fb-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d45fb-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="d45fb-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d45fb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d45fb-108">DESCRIPTION</span></span>
<span data-ttu-id="d45fb-109">A **Get-AzStorageBlobCopyState** parancsmag az Azure Storage blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="d45fb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d45fb-110">EXAMPLES</span></span>

### <span data-ttu-id="d45fb-111">Példa 1: blob másolati állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d45fb-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="d45fb-112">Ez a parancs a ContosoPlanning2015 nevű blob másolati állapotát kapja meg a tároló ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="d45fb-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="d45fb-113">2. példa: a blob-objektum másolati állapotának beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="d45fb-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="d45fb-114">Ez a parancs a ContosoUploads nevű ContosoPlanning2015 a **Get-AzStorageBlob** parancsmag használatával kapja meg az eredményét, majd átadja az eredményt az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="d45fb-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d45fb-115">A **Get-AzStorageBlobCopyState** parancsmag az adott blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="d45fb-116">3. példa: a másolati állapot beolvasása a tárolóban lévő blob-tárolóban a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="d45fb-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="d45fb-117">Ez a parancs a **Get-AzStorageBlob** parancsmag használatával kapja meg a tárolót, és az eredményt átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d45fb-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="d45fb-118">A **Get-AzStorageContainer** parancsmag a tárolóban lévő ContosoPlanning2015 nevű blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="d45fb-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d45fb-119">PARAMETERS</span></span>

### <span data-ttu-id="d45fb-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="d45fb-120">-Blob</span></span>
<span data-ttu-id="d45fb-121">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="d45fb-122">Ez a parancsmag beilleszti az Azure-tárterület blob-másolási műveletének állapotát, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="d45fb-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d45fb-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d45fb-124">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="d45fb-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d45fb-125">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="d45fb-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d45fb-126">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d45fb-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d45fb-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d45fb-127">-CloudBlob</span></span>
<span data-ttu-id="d45fb-128">Egy **CloudBlob** -objektumot ad meg az Azure Storage Client Library webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d45fb-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="d45fb-129">**CloudBlob** objektum beolvasásához használja az Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d45fb-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="d45fb-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d45fb-130">-CloudBlobContainer</span></span>
<span data-ttu-id="d45fb-131">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="d45fb-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="d45fb-132">Ez a parancsmag a paraméter által megadott tárolóban lévő blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="d45fb-133">**CloudBlobContainer** objektum beolvasásához használja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d45fb-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="d45fb-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d45fb-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d45fb-135">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d45fb-136">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d45fb-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d45fb-137">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="d45fb-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d45fb-138">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="d45fb-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d45fb-139">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="d45fb-139">The default value is 10.</span></span>

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

### <span data-ttu-id="d45fb-140">-Container</span><span class="sxs-lookup"><span data-stu-id="d45fb-140">-Container</span></span>
<span data-ttu-id="d45fb-141">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-141">Specifies the name of a container.</span></span>
<span data-ttu-id="d45fb-142">Ez a parancsmag a paraméter által megadott tárolóban lévő blob másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="d45fb-143">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d45fb-143">-Context</span></span>
<span data-ttu-id="d45fb-144">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d45fb-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d45fb-145">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d45fb-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d45fb-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45fb-146">-DefaultProfile</span></span>
<span data-ttu-id="d45fb-147">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d45fb-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d45fb-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d45fb-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d45fb-149">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="d45fb-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d45fb-150">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d45fb-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d45fb-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d45fb-151">-WaitForComplete</span></span>
<span data-ttu-id="d45fb-152">Jelzi, hogy ez a parancsmag várja a másolat befejezését.</span><span class="sxs-lookup"><span data-stu-id="d45fb-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="d45fb-153">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadott eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="d45fb-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="d45fb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45fb-154">CommonParameters</span></span>
<span data-ttu-id="d45fb-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d45fb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45fb-156">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45fb-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45fb-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d45fb-157">INPUTS</span></span>

### <span data-ttu-id="d45fb-158">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d45fb-158">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="d45fb-159">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d45fb-159">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="d45fb-160">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d45fb-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d45fb-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d45fb-161">OUTPUTS</span></span>

### <span data-ttu-id="d45fb-162">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d45fb-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="d45fb-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d45fb-163">NOTES</span></span>

## <span data-ttu-id="d45fb-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d45fb-164">RELATED LINKS</span></span>

[<span data-ttu-id="d45fb-165">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d45fb-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="d45fb-166">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d45fb-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


