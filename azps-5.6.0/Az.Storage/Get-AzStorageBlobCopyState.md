---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 4bc06ca07c95986f75062a64a0f86475f7720ff1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002742"
---
# <span data-ttu-id="b4a69-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="b4a69-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="b4a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a69-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a69-103">Egy Azure Storage blob másolási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b4a69-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="b4a69-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b4a69-104">SYNTAX</span></span>

### <span data-ttu-id="b4a69-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4a69-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b4a69-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b4a69-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b4a69-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b4a69-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b4a69-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b4a69-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a69-109">A **Get-AzStorageBlobCopyState** parancsmag egy Azure Storage-blob másolási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b4a69-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="b4a69-110">A fájlnak a másolási cél blobon kell futnia.</span><span class="sxs-lookup"><span data-stu-id="b4a69-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="b4a69-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b4a69-111">EXAMPLES</span></span>

### <span data-ttu-id="b4a69-112">1. példa: Blob másolási állapotának lekérte</span><span class="sxs-lookup"><span data-stu-id="b4a69-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="b4a69-113">Ez a parancs a ContosoPlanning2015 nevű blob másolási állapotát kapja meg a ContosoUploads tárolóban.</span><span class="sxs-lookup"><span data-stu-id="b4a69-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="b4a69-114">2. példa: Blob másolási állapotának lekérte a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="b4a69-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="b4a69-115">Ez a parancs a ContosoPlanning2015 nevű blobot a ContosoUploads nevű tárolóba a **Get-AzStorageBlob** parancsmag használatával kapja meg, majd a folyamat műveleti operátorával átadja az eredményt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b4a69-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4a69-116">A **Get-AzStorageBlobCopyState** parancsmag megkapja a blob másolási állapotát.</span><span class="sxs-lookup"><span data-stu-id="b4a69-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="b4a69-117">3. példa: A blob másolási állapotának lekérte egy tárolóban a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="b4a69-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="b4a69-118">Ez a parancs a **Get-AzStorageBlob** parancsmag használatával elnevezett tárolót kapja, majd átadja az eredményt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b4a69-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="b4a69-119">A **Get-AzStorageContainer** parancsmag megkapja a ContosoPlanning2015 nevű blob másolási állapotát a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="b4a69-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="b4a69-120">4. példa: Másolás és folyamat létrehozása a másolás állapotának lekért érdekében</span><span class="sxs-lookup"><span data-stu-id="b4a69-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="b4a69-121">Az első parancs elindítja a "ContosoPlanning2015" másolási blobot a "ContosoPlanning2015_copy" szóra, és kimenetként kimenetet ad a destiantion blob objektumnak.</span><span class="sxs-lookup"><span data-stu-id="b4a69-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="b4a69-122">A második parancs produkálhatja a destiantion blob objektumot a Get-AzStorageBlobCopyState fájlba a blob másolási állapotának be szereznie.</span><span class="sxs-lookup"><span data-stu-id="b4a69-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="b4a69-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4a69-123">PARAMETERS</span></span>

### <span data-ttu-id="b4a69-124">-Blob</span><span class="sxs-lookup"><span data-stu-id="b4a69-124">-Blob</span></span>
<span data-ttu-id="b4a69-125">Egy blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4a69-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="b4a69-126">Ez a parancsmag a paraméter által megadott Azure Storage-blob blob blobmásolat-műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b4a69-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4a69-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b4a69-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b4a69-128">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b4a69-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b4a69-129">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="b4a69-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b4a69-130">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b4a69-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b4a69-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b4a69-131">-CloudBlob</span></span>
<span data-ttu-id="b4a69-132">Egy **CloudBlob-objektumot** ad meg az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="b4a69-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="b4a69-133">**CloudBlob-objektum** beszerzéséhez használja a Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4a69-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b4a69-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b4a69-134">-CloudBlobContainer</span></span>
<span data-ttu-id="b4a69-135">Egy **CloudBlobContainer-objektumot** ad meg az Azure Storage Client tárból.</span><span class="sxs-lookup"><span data-stu-id="b4a69-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b4a69-136">Ez a parancsmag egy blob másolási állapotát kapja meg a paraméter által megadott tárolóban.</span><span class="sxs-lookup"><span data-stu-id="b4a69-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="b4a69-137">**CloudBlobContainer-objektum** beszerzéséhez használja a Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4a69-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b4a69-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b4a69-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b4a69-139">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="b4a69-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b4a69-140">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="b4a69-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b4a69-141">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="b4a69-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b4a69-142">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b4a69-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b4a69-143">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b4a69-143">The default value is 10.</span></span>

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

### <span data-ttu-id="b4a69-144">-Container</span><span class="sxs-lookup"><span data-stu-id="b4a69-144">-Container</span></span>
<span data-ttu-id="b4a69-145">Egy tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4a69-145">Specifies the name of a container.</span></span>
<span data-ttu-id="b4a69-146">Ez a parancsmag a paraméter által megadott tárolóban lévő blob másolási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b4a69-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4a69-147">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b4a69-147">-Context</span></span>
<span data-ttu-id="b4a69-148">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4a69-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b4a69-149">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4a69-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b4a69-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a69-150">-DefaultProfile</span></span>
<span data-ttu-id="b4a69-151">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4a69-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a69-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b4a69-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b4a69-153">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="b4a69-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b4a69-154">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b4a69-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b4a69-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b4a69-155">-WaitForComplete</span></span>
<span data-ttu-id="b4a69-156">Azt jelzi, hogy a parancsmag a másolat befejeződik.</span><span class="sxs-lookup"><span data-stu-id="b4a69-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="b4a69-157">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadja az eredményt.</span><span class="sxs-lookup"><span data-stu-id="b4a69-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="b4a69-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a69-158">CommonParameters</span></span>
<span data-ttu-id="b4a69-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a69-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a69-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a69-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a69-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4a69-161">INPUTS</span></span>

### <span data-ttu-id="b4a69-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b4a69-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b4a69-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b4a69-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b4a69-164">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4a69-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b4a69-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4a69-165">OUTPUTS</span></span>

### <span data-ttu-id="b4a69-166">Microsoft.Azure.Storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="b4a69-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="b4a69-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b4a69-167">NOTES</span></span>

## <span data-ttu-id="b4a69-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4a69-168">RELATED LINKS</span></span>

[<span data-ttu-id="b4a69-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b4a69-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="b4a69-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b4a69-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


