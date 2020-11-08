---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017510"
---
# <span data-ttu-id="d23bc-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d23bc-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="d23bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d23bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d23bc-103">Eltávolítja a megadott tárterület-blobot.</span><span class="sxs-lookup"><span data-stu-id="d23bc-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="d23bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d23bc-104">SYNTAX</span></span>

### <span data-ttu-id="d23bc-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d23bc-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d23bc-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="d23bc-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d23bc-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="d23bc-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d23bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d23bc-108">DESCRIPTION</span></span>
<span data-ttu-id="d23bc-109">A **Remove-AzStorageBlob** parancsmag eltávolítja a megadott blobot egy tárterület-fiókból az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d23bc-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="d23bc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d23bc-110">EXAMPLES</span></span>

### <span data-ttu-id="d23bc-111">1. példa: tárterület-blob eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="d23bc-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="d23bc-112">Ez a parancs eltávolítja a nevével azonosított blobot.</span><span class="sxs-lookup"><span data-stu-id="d23bc-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="d23bc-113">2. példa: tárterület-blob eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="d23bc-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="d23bc-114">Ez a parancs a csővezetéket használja.</span><span class="sxs-lookup"><span data-stu-id="d23bc-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="d23bc-115">3. példa: a tárterületet tároló Blobok eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="d23bc-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="d23bc-116">Ez a parancs a csillag (\*) helyettesítő karaktert és a csővezetéket használja a blob vagy a Blobs-elemek beolvasásához, majd eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="d23bc-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="d23bc-117">4. példa: egyetlen blob-verzió eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d23bc-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="d23bc-118">Ez a parancs eltávolítja a VersionId-nal egyetlen bináris verzióját.</span><span class="sxs-lookup"><span data-stu-id="d23bc-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="d23bc-119">Példa 5: egyetlen blob-pillanatkép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d23bc-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="d23bc-120">Ez a parancs egyetlen blob-pillanatképet távolít el a SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="d23bc-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="d23bc-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d23bc-121">PARAMETERS</span></span>

### <span data-ttu-id="d23bc-122">-BLOB</span><span class="sxs-lookup"><span data-stu-id="d23bc-122">-Blob</span></span>
<span data-ttu-id="d23bc-123">Az eltávolítani kívánt blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d23bc-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="d23bc-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="d23bc-124">-BlobBaseClient</span></span>
<span data-ttu-id="d23bc-125">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="d23bc-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="d23bc-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d23bc-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d23bc-127">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="d23bc-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d23bc-128">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="d23bc-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d23bc-129">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d23bc-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d23bc-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d23bc-130">-CloudBlob</span></span>
<span data-ttu-id="d23bc-131">Felhőbeli blobot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d23bc-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="d23bc-132">**CloudBlob** objektum beolvasásához használja az Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d23bc-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="d23bc-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d23bc-133">-CloudBlobContainer</span></span>
<span data-ttu-id="d23bc-134">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="d23bc-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="d23bc-135">A Get-AzStorageContainer parancsmag használatával is elérheti.</span><span class="sxs-lookup"><span data-stu-id="d23bc-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="d23bc-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d23bc-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d23bc-137">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d23bc-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d23bc-138">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d23bc-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d23bc-139">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="d23bc-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d23bc-140">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="d23bc-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d23bc-141">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="d23bc-141">The default value is 10.</span></span>

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

### <span data-ttu-id="d23bc-142">-Container</span><span class="sxs-lookup"><span data-stu-id="d23bc-142">-Container</span></span>
<span data-ttu-id="d23bc-143">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d23bc-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="d23bc-144">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d23bc-144">-Context</span></span>
<span data-ttu-id="d23bc-145">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d23bc-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d23bc-146">A New-AzStorageContext parancsmag segítségével létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="d23bc-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="d23bc-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23bc-147">-DefaultProfile</span></span>
<span data-ttu-id="d23bc-148">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d23bc-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d23bc-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="d23bc-149">-DeleteSnapshot</span></span>
<span data-ttu-id="d23bc-150">Azt adja meg, hogy az összes pillanatkép törlődik, az alap blob nélkül.</span><span class="sxs-lookup"><span data-stu-id="d23bc-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="d23bc-151">Ha ez a paraméter nincs megadva, az alap blob és a pillanatképek együtt törlődnek.</span><span class="sxs-lookup"><span data-stu-id="d23bc-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="d23bc-152">A felhasználó a törlési művelet megerősítésére kéri.</span><span class="sxs-lookup"><span data-stu-id="d23bc-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="d23bc-153">-Force</span><span class="sxs-lookup"><span data-stu-id="d23bc-153">-Force</span></span>
<span data-ttu-id="d23bc-154">Azt jelzi, hogy a parancsmag megerősítés nélkül eltávolítja a blobot és annak pillanatképét.</span><span class="sxs-lookup"><span data-stu-id="d23bc-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="d23bc-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d23bc-155">-PassThru</span></span>
<span data-ttu-id="d23bc-156">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="d23bc-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d23bc-157">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="d23bc-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d23bc-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d23bc-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d23bc-159">Az elolvasni kívánt parancsmag Azure-profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d23bc-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="d23bc-160">Ha nincs megadva, a parancsmag az alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d23bc-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="d23bc-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="d23bc-161">-SnapshotTime</span></span>
<span data-ttu-id="d23bc-162">BLOB SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="d23bc-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="d23bc-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="d23bc-163">-VersionId</span></span>
<span data-ttu-id="d23bc-164">BLOB VersionId</span><span class="sxs-lookup"><span data-stu-id="d23bc-164">Blob VersionId</span></span>

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

### <span data-ttu-id="d23bc-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d23bc-165">-Confirm</span></span>
<span data-ttu-id="d23bc-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d23bc-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d23bc-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d23bc-167">-WhatIf</span></span>
<span data-ttu-id="d23bc-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d23bc-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d23bc-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d23bc-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d23bc-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23bc-170">CommonParameters</span></span>
<span data-ttu-id="d23bc-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d23bc-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23bc-172">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23bc-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23bc-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d23bc-173">INPUTS</span></span>

### <span data-ttu-id="d23bc-174">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d23bc-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="d23bc-175">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d23bc-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="d23bc-176">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d23bc-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d23bc-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d23bc-177">OUTPUTS</span></span>

### <span data-ttu-id="d23bc-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d23bc-178">System.Boolean</span></span>

## <span data-ttu-id="d23bc-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d23bc-179">NOTES</span></span>

## <span data-ttu-id="d23bc-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d23bc-180">RELATED LINKS</span></span>

[<span data-ttu-id="d23bc-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d23bc-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="d23bc-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d23bc-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="d23bc-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d23bc-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
