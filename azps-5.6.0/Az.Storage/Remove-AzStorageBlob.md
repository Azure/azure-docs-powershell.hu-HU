---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 12bfa9ab7e35bab3421bee71cf5ea0787c95a86d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918033"
---
# <span data-ttu-id="82972-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82972-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="82972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82972-102">SYNOPSIS</span></span>
<span data-ttu-id="82972-103">Eltávolítja a megadott tárterület-blobot.</span><span class="sxs-lookup"><span data-stu-id="82972-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="82972-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82972-104">SYNTAX</span></span>

### <span data-ttu-id="82972-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82972-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82972-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="82972-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82972-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="82972-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82972-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82972-108">DESCRIPTION</span></span>
<span data-ttu-id="82972-109">A **Remove-AzStorageBlob** parancsmag eltávolítja a megadott blobot az Azure-beli tárfiókból.</span><span class="sxs-lookup"><span data-stu-id="82972-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="82972-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82972-110">EXAMPLES</span></span>

### <span data-ttu-id="82972-111">1. példa: Tár blob eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="82972-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="82972-112">Ez a parancs eltávolítja a neve által azonosított blobot.</span><span class="sxs-lookup"><span data-stu-id="82972-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="82972-113">2. példa: Tár blob eltávolítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="82972-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="82972-114">Ez a parancs a folyamatot használja.</span><span class="sxs-lookup"><span data-stu-id="82972-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="82972-115">3. példa: Tárterület-blobok eltávolítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="82972-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="82972-116">Ez a parancs a csillag (\*) helyettesítő karaktert és a prognózist használva beolvassa a blobot vagy a blobokat, majd eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="82972-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="82972-117">4. példa: Egyetlen blobverzió eltávolítása</span><span class="sxs-lookup"><span data-stu-id="82972-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="82972-118">Ez a parancs eltávolít egy blob veriont a VersionId paranccsal.</span><span class="sxs-lookup"><span data-stu-id="82972-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="82972-119">5. példa: Egyetlen blob-pillanatfelvétel eltávolítása</span><span class="sxs-lookup"><span data-stu-id="82972-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="82972-120">Ez a parancs eltávolít egyetlen blob-pillanatfelvételt a SnapshotTime-val.</span><span class="sxs-lookup"><span data-stu-id="82972-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="82972-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82972-121">PARAMETERS</span></span>

### <span data-ttu-id="82972-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="82972-122">-Blob</span></span>
<span data-ttu-id="82972-123">Az eltávolítani kívánt blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82972-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="82972-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="82972-124">-BlobBaseClient</span></span>
<span data-ttu-id="82972-125">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="82972-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="82972-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="82972-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="82972-127">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="82972-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="82972-128">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="82972-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="82972-129">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="82972-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="82972-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="82972-130">-CloudBlob</span></span>
<span data-ttu-id="82972-131">Felhő blobot ad meg.</span><span class="sxs-lookup"><span data-stu-id="82972-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="82972-132">**CloudBlob-objektum** beszerzéséhez használja a Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="82972-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="82972-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="82972-133">-CloudBlobContainer</span></span>
<span data-ttu-id="82972-134">Egy **CloudBlobContainer-objektumot** ad meg az Azure Storage Client tárból.</span><span class="sxs-lookup"><span data-stu-id="82972-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="82972-135">A Get-AzStorageContainer parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="82972-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="82972-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="82972-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="82972-137">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="82972-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="82972-138">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="82972-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="82972-139">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="82972-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="82972-140">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="82972-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="82972-141">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="82972-141">The default value is 10.</span></span>

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

### <span data-ttu-id="82972-142">-Container</span><span class="sxs-lookup"><span data-stu-id="82972-142">-Container</span></span>
<span data-ttu-id="82972-143">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82972-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="82972-144">-Környezet</span><span class="sxs-lookup"><span data-stu-id="82972-144">-Context</span></span>
<span data-ttu-id="82972-145">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="82972-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="82972-146">A New-AzStorageContext létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="82972-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="82972-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82972-147">-DefaultProfile</span></span>
<span data-ttu-id="82972-148">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82972-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82972-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="82972-149">-DeleteSnapshot</span></span>
<span data-ttu-id="82972-150">Azt adja meg, hogy az összes pillanatkép törlődik, de az alap blob nem.</span><span class="sxs-lookup"><span data-stu-id="82972-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="82972-151">Ha nincs megadva ez a paraméter, az alap blob és pillanatképei együtt törlődnek.</span><span class="sxs-lookup"><span data-stu-id="82972-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="82972-152">A rendszer kéri a felhasználót a törlési művelet megerősítésére.</span><span class="sxs-lookup"><span data-stu-id="82972-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="82972-153">-Force</span><span class="sxs-lookup"><span data-stu-id="82972-153">-Force</span></span>
<span data-ttu-id="82972-154">Azt jelzi, hogy ez a parancsmag jóváhagyás nélkül eltávolítja a blobot és a pillanatképét.</span><span class="sxs-lookup"><span data-stu-id="82972-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="82972-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82972-155">-PassThru</span></span>
<span data-ttu-id="82972-156">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="82972-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="82972-157">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="82972-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="82972-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="82972-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="82972-159">Azt az Azure-profilt adja meg, amely felolvassa a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="82972-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="82972-160">Ha nincs megadva, a parancsmag az alapértelmezett profilból olvassa be az olvasott értékeket.</span><span class="sxs-lookup"><span data-stu-id="82972-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="82972-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="82972-161">-SnapshotTime</span></span>
<span data-ttu-id="82972-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="82972-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82972-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="82972-163">-VersionId</span></span>
<span data-ttu-id="82972-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="82972-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82972-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82972-165">-Confirm</span></span>
<span data-ttu-id="82972-166">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82972-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82972-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82972-167">-WhatIf</span></span>
<span data-ttu-id="82972-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82972-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82972-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82972-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82972-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82972-170">CommonParameters</span></span>
<span data-ttu-id="82972-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82972-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82972-172">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82972-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82972-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82972-173">INPUTS</span></span>

### <span data-ttu-id="82972-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="82972-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="82972-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="82972-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="82972-176">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="82972-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="82972-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82972-177">OUTPUTS</span></span>

### <span data-ttu-id="82972-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82972-178">System.Boolean</span></span>

## <span data-ttu-id="82972-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82972-179">NOTES</span></span>

## <span data-ttu-id="82972-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82972-180">RELATED LINKS</span></span>

[<span data-ttu-id="82972-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82972-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="82972-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82972-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="82972-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82972-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
