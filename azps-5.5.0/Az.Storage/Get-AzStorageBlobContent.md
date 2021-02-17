---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164802"
---
# <span data-ttu-id="1a9bd-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1a9bd-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="1a9bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9bd-103">Letölt egy tár blobját.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="1a9bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a9bd-104">SYNTAX</span></span>

### <span data-ttu-id="1a9bd-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1a9bd-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a9bd-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="1a9bd-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a9bd-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="1a9bd-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a9bd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a9bd-108">DESCRIPTION</span></span>
<span data-ttu-id="1a9bd-109">A **Get-AzStorageBlobContent** parancsmag letölti a megadott tárterület-blobot.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="1a9bd-110">Ha a blobnév érvénytelen a helyi számítógéphez, ez a parancsmag automatikusan feloldja azt, ha lehetséges.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="1a9bd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a9bd-111">EXAMPLES</span></span>

### <span data-ttu-id="1a9bd-112">1. példa: Blob-tartalom letöltése név szerint</span><span class="sxs-lookup"><span data-stu-id="1a9bd-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="1a9bd-113">Ez a parancs név szerint letölt egy blobot.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="1a9bd-114">2. példa: Blob-tartalom letöltése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="1a9bd-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="1a9bd-115">Ez a parancs a folyamat segítségével megkeresi és letölti a blobtartalmat.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="1a9bd-116">3. példa: Blobtartalom letöltése a folyamat és egy helyettesítő karakter használatával</span><span class="sxs-lookup"><span data-stu-id="1a9bd-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="1a9bd-117">Ebben a példában a csillag helyettesítő karakter és a folyamat segítségével megkeresi és letölti a blobtartalmat.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="1a9bd-118">4. példa: Blob-objektum lehozása és mentése egy változóba, majd blobtartalom letöltése a blobobjektummal</span><span class="sxs-lookup"><span data-stu-id="1a9bd-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="1a9bd-119">Ez a példa először egy blobobjektumot kap, és egy változóba menti, majd letölti a blobobjektumot tároló blobtartalmat.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="1a9bd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a9bd-120">PARAMETERS</span></span>

### <span data-ttu-id="1a9bd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a9bd-121">-AsJob</span></span>
<span data-ttu-id="1a9bd-122">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1a9bd-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="1a9bd-123">-Blob</span></span>
<span data-ttu-id="1a9bd-124">A letöltendő blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-124">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="1a9bd-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="1a9bd-125">-BlobBaseClient</span></span>
<span data-ttu-id="1a9bd-126">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="1a9bd-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bd-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="1a9bd-127">-CheckMd5</span></span>
<span data-ttu-id="1a9bd-128">Azt adja meg, hogy ellenőrizze-e a letöltött fájl Md5-ös összegét.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="1a9bd-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a9bd-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a9bd-130">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1a9bd-131">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1a9bd-132">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1a9bd-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1a9bd-133">-CloudBlob</span></span>
<span data-ttu-id="1a9bd-134">Felhő blobot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="1a9bd-135">**CloudBlob-objektum** beszerzéséhez használja a Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="1a9bd-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1a9bd-136">-CloudBlobContainer</span></span>
<span data-ttu-id="1a9bd-137">Egy **CloudBlobContainer-objektumot** ad meg az Azure-tárból.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="1a9bd-138">Létrehozhatja, vagy használhatja a Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="1a9bd-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a9bd-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a9bd-140">Megadja a maximális párhuzamos hálózati hívást.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1a9bd-141">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1a9bd-142">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1a9bd-143">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1a9bd-144">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-144">The default value is 10.</span></span>

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

### <span data-ttu-id="1a9bd-145">-Container</span><span class="sxs-lookup"><span data-stu-id="1a9bd-145">-Container</span></span>
<span data-ttu-id="1a9bd-146">Annak a tárolónak a nevét adja meg, amely a letölteni kívánt blobot tárolja.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-146">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="1a9bd-147">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1a9bd-147">-Context</span></span>
<span data-ttu-id="1a9bd-148">Azt az Azure-tárfiókot adja meg, amelyből blobtartalmat szeretne letölteni.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="1a9bd-149">A New-AzStorageContext környezet létrehozásához használhatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="1a9bd-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9bd-150">-DefaultProfile</span></span>
<span data-ttu-id="1a9bd-151">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a9bd-152">-Destination</span><span class="sxs-lookup"><span data-stu-id="1a9bd-152">-Destination</span></span>
<span data-ttu-id="1a9bd-153">A letöltött fájl tárolására megadott hely.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-153">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="1a9bd-154">-Force</span><span class="sxs-lookup"><span data-stu-id="1a9bd-154">-Force</span></span>
<span data-ttu-id="1a9bd-155">Jóváhagyás nélkül felülír egy meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="1a9bd-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a9bd-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a9bd-157">A szolgáltatás oldalának időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1a9bd-158">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1a9bd-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a9bd-159">-Confirm</span></span>
<span data-ttu-id="1a9bd-160">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a9bd-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a9bd-161">-WhatIf</span></span>
<span data-ttu-id="1a9bd-162">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a9bd-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a9bd-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9bd-164">CommonParameters</span></span>
<span data-ttu-id="1a9bd-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9bd-166">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a9bd-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9bd-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a9bd-167">INPUTS</span></span>

### <span data-ttu-id="1a9bd-168">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1a9bd-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="1a9bd-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1a9bd-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="1a9bd-170">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a9bd-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a9bd-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a9bd-171">OUTPUTS</span></span>

### <span data-ttu-id="1a9bd-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1a9bd-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="1a9bd-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a9bd-173">NOTES</span></span>
* <span data-ttu-id="1a9bd-174">Ha a blob neve érvénytelen a helyi számítógépen, ez a parancsmag automatikusan feloldja azt, ha lehetséges.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="1a9bd-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a9bd-175">RELATED LINKS</span></span>

[<span data-ttu-id="1a9bd-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1a9bd-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="1a9bd-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1a9bd-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="1a9bd-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1a9bd-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
