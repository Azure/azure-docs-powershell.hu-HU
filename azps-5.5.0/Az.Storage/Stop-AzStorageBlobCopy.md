---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 979cfd1241910cb98bebee3b80bc0a1ab6b8da71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150370"
---
# <span data-ttu-id="0322f-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0322f-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="0322f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0322f-102">SYNOPSIS</span></span>
<span data-ttu-id="0322f-103">A másolási művelet leállítja.</span><span class="sxs-lookup"><span data-stu-id="0322f-103">Stops a copy operation.</span></span>

## <span data-ttu-id="0322f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0322f-104">SYNTAX</span></span>

### <span data-ttu-id="0322f-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0322f-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0322f-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="0322f-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0322f-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="0322f-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0322f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0322f-108">DESCRIPTION</span></span>
<span data-ttu-id="0322f-109">A **Stop-AzStorageBlobCopy** parancsmag leállít egy másolási műveletet a megadott cél blobba.</span><span class="sxs-lookup"><span data-stu-id="0322f-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="0322f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0322f-110">EXAMPLES</span></span>

### <span data-ttu-id="0322f-111">1. példa: Másolási művelet leállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="0322f-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="0322f-112">Ez a parancs név szerint leállítja a másolási műveletet.</span><span class="sxs-lookup"><span data-stu-id="0322f-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="0322f-113">2. példa: Másolási művelet leállítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="0322f-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="0322f-114">Ez a parancs leállítja a másolási műveletet úgy, hogy átállítja a tárolót a folyamaton a **Get-AzStorageContainerből.**</span><span class="sxs-lookup"><span data-stu-id="0322f-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="0322f-115">3. példa: Másolási művelet leállítása a folyamat és a Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0322f-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="0322f-116">Ez a példa leállítja a másolási műveletet úgy, hogy a folyamat tárolóját a Get-AzStorageBlob parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="0322f-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="0322f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0322f-117">PARAMETERS</span></span>

### <span data-ttu-id="0322f-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="0322f-118">-Blob</span></span>
<span data-ttu-id="0322f-119">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0322f-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="0322f-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0322f-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0322f-121">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="0322f-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0322f-122">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="0322f-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0322f-123">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="0322f-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0322f-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0322f-124">-CloudBlob</span></span>
<span data-ttu-id="0322f-125">Egy **CloudBlob-objektumot** ad meg az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="0322f-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="0322f-126">**CloudBlob-objektum** beszerzéséhez használja a Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0322f-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="0322f-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0322f-127">-CloudBlobContainer</span></span>
<span data-ttu-id="0322f-128">Egy **CloudBlobContainer-objektumot** ad meg az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="0322f-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="0322f-129">Létrehozhatja az objektumot, vagy használhatja a Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0322f-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="0322f-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0322f-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0322f-131">Megadja a maximális párhuzamos hálózati hívást.</span><span class="sxs-lookup"><span data-stu-id="0322f-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0322f-132">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="0322f-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0322f-133">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="0322f-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0322f-134">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="0322f-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0322f-135">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0322f-135">The default value is 10.</span></span>

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

### <span data-ttu-id="0322f-136">-Container</span><span class="sxs-lookup"><span data-stu-id="0322f-136">-Container</span></span>
<span data-ttu-id="0322f-137">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0322f-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="0322f-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0322f-138">-Context</span></span>
<span data-ttu-id="0322f-139">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0322f-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0322f-140">A környezet létrehozásához használja a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0322f-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0322f-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="0322f-141">-CopyId</span></span>
<span data-ttu-id="0322f-142">A másolásazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="0322f-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="0322f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0322f-143">-DefaultProfile</span></span>
<span data-ttu-id="0322f-144">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0322f-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0322f-145">-Force</span><span class="sxs-lookup"><span data-stu-id="0322f-145">-Force</span></span>
<span data-ttu-id="0322f-146">Leállítja az aktuális másolási feladatot a megadott blobon megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0322f-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0322f-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0322f-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0322f-148">A szolgáltatás oldalának időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="0322f-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0322f-149">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="0322f-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0322f-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0322f-150">-Confirm</span></span>
<span data-ttu-id="0322f-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0322f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0322f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0322f-152">-WhatIf</span></span>
<span data-ttu-id="0322f-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0322f-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0322f-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0322f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0322f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0322f-155">CommonParameters</span></span>
<span data-ttu-id="0322f-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0322f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0322f-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0322f-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0322f-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0322f-158">INPUTS</span></span>

### <span data-ttu-id="0322f-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0322f-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="0322f-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0322f-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="0322f-161">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0322f-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0322f-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0322f-162">OUTPUTS</span></span>

### <span data-ttu-id="0322f-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0322f-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="0322f-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0322f-164">NOTES</span></span>

## <span data-ttu-id="0322f-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0322f-165">RELATED LINKS</span></span>

[<span data-ttu-id="0322f-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0322f-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="0322f-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0322f-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="0322f-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0322f-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="0322f-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="0322f-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
