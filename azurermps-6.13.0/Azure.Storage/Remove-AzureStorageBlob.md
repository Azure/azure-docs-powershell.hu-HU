---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
ms.openlocfilehash: 0472bb767ee1b5d6092e0ac2e6ca94396bf7e417
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502295"
---
# <span data-ttu-id="b0e58-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b0e58-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="b0e58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0e58-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e58-103">Eltávolítja a megadott tárterület-blobot.</span><span class="sxs-lookup"><span data-stu-id="b0e58-103">Removes the specified storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0e58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0e58-104">SYNTAX</span></span>

### <span data-ttu-id="b0e58-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0e58-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e58-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b0e58-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e58-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b0e58-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0e58-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0e58-108">DESCRIPTION</span></span>
<span data-ttu-id="b0e58-109">A **Remove-AzureStorageBlob** parancsmag eltávolítja a megadott blobot egy tárterület-fiókból az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b0e58-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="b0e58-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b0e58-110">EXAMPLES</span></span>

### <span data-ttu-id="b0e58-111">1. példa: tárterület-blob eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="b0e58-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="b0e58-112">Ez a parancs eltávolítja a nevével azonosított blobot.</span><span class="sxs-lookup"><span data-stu-id="b0e58-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="b0e58-113">2. példa: tárterület-blob eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="b0e58-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="b0e58-114">Ez a parancs a csővezetéket használja.</span><span class="sxs-lookup"><span data-stu-id="b0e58-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="b0e58-115">3. példa: a tárterületet tároló Blobok eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="b0e58-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="b0e58-116">Ez a parancs a csillag (\*) helyettesítő karaktert és a csővezetéket használja a blob vagy a Blobs-elemek beolvasásához, majd eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="b0e58-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="b0e58-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0e58-117">PARAMETERS</span></span>

### <span data-ttu-id="b0e58-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="b0e58-118">-Blob</span></span>
<span data-ttu-id="b0e58-119">Az eltávolítani kívánt blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0e58-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="b0e58-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0e58-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b0e58-121">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="b0e58-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b0e58-122">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="b0e58-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b0e58-123">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b0e58-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b0e58-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b0e58-124">-CloudBlob</span></span>
<span data-ttu-id="b0e58-125">Felhőbeli blobot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b0e58-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="b0e58-126">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b0e58-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e58-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b0e58-127">-CloudBlobContainer</span></span>
<span data-ttu-id="b0e58-128">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="b0e58-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b0e58-129">A Get-AzureStorageContainer parancsmag használatával is elérheti.</span><span class="sxs-lookup"><span data-stu-id="b0e58-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e58-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b0e58-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b0e58-131">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0e58-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b0e58-132">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="b0e58-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b0e58-133">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="b0e58-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b0e58-134">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="b0e58-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b0e58-135">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b0e58-135">The default value is 10.</span></span>

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

### <span data-ttu-id="b0e58-136">-Container</span><span class="sxs-lookup"><span data-stu-id="b0e58-136">-Container</span></span>
<span data-ttu-id="b0e58-137">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0e58-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="b0e58-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b0e58-138">-Context</span></span>
<span data-ttu-id="b0e58-139">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0e58-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b0e58-140">A New-AzureStorageContext parancsmag segítségével létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="b0e58-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="b0e58-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e58-141">-DefaultProfile</span></span>
<span data-ttu-id="b0e58-142">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0e58-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e58-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="b0e58-143">-DeleteSnapshot</span></span>
<span data-ttu-id="b0e58-144">Azt adja meg, hogy az összes pillanatkép törlődik, az alap blob nélkül.</span><span class="sxs-lookup"><span data-stu-id="b0e58-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="b0e58-145">Ha ez a paraméter nincs megadva, az alap blob és a pillanatképek együtt törlődnek.</span><span class="sxs-lookup"><span data-stu-id="b0e58-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="b0e58-146">A felhasználó a törlési művelet megerősítésére kéri.</span><span class="sxs-lookup"><span data-stu-id="b0e58-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="b0e58-147">-Force</span><span class="sxs-lookup"><span data-stu-id="b0e58-147">-Force</span></span>
<span data-ttu-id="b0e58-148">Azt jelzi, hogy a parancsmag megerősítés nélkül eltávolítja a blobot és annak pillanatképét.</span><span class="sxs-lookup"><span data-stu-id="b0e58-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="b0e58-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0e58-149">-PassThru</span></span>
<span data-ttu-id="b0e58-150">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="b0e58-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b0e58-151">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="b0e58-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b0e58-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0e58-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b0e58-153">Az elolvasni kívánt parancsmag Azure-profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0e58-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="b0e58-154">Ha nincs megadva, a parancsmag az alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b0e58-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="b0e58-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0e58-155">-Confirm</span></span>
<span data-ttu-id="b0e58-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0e58-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e58-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e58-157">-WhatIf</span></span>
<span data-ttu-id="b0e58-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0e58-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e58-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0e58-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e58-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e58-160">CommonParameters</span></span>
<span data-ttu-id="b0e58-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0e58-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e58-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e58-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e58-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0e58-163">INPUTS</span></span>

### <span data-ttu-id="b0e58-164">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b0e58-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b0e58-165">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b0e58-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b0e58-166">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0e58-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0e58-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0e58-167">OUTPUTS</span></span>

### <span data-ttu-id="b0e58-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0e58-168">System.Boolean</span></span>

## <span data-ttu-id="b0e58-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0e58-169">NOTES</span></span>

## <span data-ttu-id="b0e58-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0e58-170">RELATED LINKS</span></span>

[<span data-ttu-id="b0e58-171">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b0e58-171">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="b0e58-172">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b0e58-172">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="b0e58-173">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b0e58-173">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)