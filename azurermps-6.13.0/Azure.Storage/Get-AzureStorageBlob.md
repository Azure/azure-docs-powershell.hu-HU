---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
ms.openlocfilehash: 20a96434c39483598d4bc6cb4d5d1d19b5454f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672334"
---
# <span data-ttu-id="0f616-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0f616-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="0f616-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f616-102">SYNOPSIS</span></span>
<span data-ttu-id="0f616-103">A tárolóban lévő Blobs listák.</span><span class="sxs-lookup"><span data-stu-id="0f616-103">Lists blobs in a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f616-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f616-104">SYNTAX</span></span>

### <span data-ttu-id="0f616-105">BlobName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f616-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f616-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="0f616-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f616-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f616-107">DESCRIPTION</span></span>
<span data-ttu-id="0f616-108">A **Get-AzureStorageBlob** parancsmag a megadott tárolóban lévő blobokat az Azure Storage-fiókban sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="0f616-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="0f616-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0f616-109">EXAMPLES</span></span>

### <span data-ttu-id="0f616-110">Példa 1: blobos név beszerzése</span><span class="sxs-lookup"><span data-stu-id="0f616-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="0f616-111">Ez a parancs egy blob-nevet és egy helyettesítő karaktert használ a blob beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="0f616-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="0f616-112">2. példa: a festékfoltok beolvasása a tárolóban a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="0f616-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="0f616-113">Ez a parancs a csővezetéken a tárolóban lévő összes blobot (a törölt állapotban lévő Blobs-objektumokat is tartalmazza) fogja használni.</span><span class="sxs-lookup"><span data-stu-id="0f616-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="0f616-114">3. példa: a festékfoltok beolvasása név előtaggal</span><span class="sxs-lookup"><span data-stu-id="0f616-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="0f616-115">Ez a parancs egy név előtagot használ a festékfoltok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="0f616-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="0f616-116">Példa 4: a lista festékfoltok több kötegben</span><span class="sxs-lookup"><span data-stu-id="0f616-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="0f616-117">Ebben a példában a *MaxCount* és a *ContinuationToken* paraméterrel több kötegben listázhatja az Azure Storage blob-ket.</span><span class="sxs-lookup"><span data-stu-id="0f616-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="0f616-118">Az első négy parancs az értékeket a példában használt változókhoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="0f616-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="0f616-119">Az ötödik parancs a **Get-AzureStorageBlob** parancsmagot használó **do-while** utasítást ad meg a Blobs-adatok beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="0f616-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="0f616-120">Az utasítás tartalmazza a $Token változóban tárolt folytatólagos tokent.</span><span class="sxs-lookup"><span data-stu-id="0f616-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="0f616-121">$Token az érték ismétléssel változik.</span><span class="sxs-lookup"><span data-stu-id="0f616-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="0f616-122">További információért írja be a következőt: `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="0f616-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="0f616-123">A végleges parancs a **echo** parancs segítségével jeleníti meg a végösszeget.</span><span class="sxs-lookup"><span data-stu-id="0f616-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="0f616-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f616-124">PARAMETERS</span></span>

### <span data-ttu-id="0f616-125">-BLOB</span><span class="sxs-lookup"><span data-stu-id="0f616-125">-Blob</span></span>
<span data-ttu-id="0f616-126">A helyettesítő karakteres kereséshez használható név vagy név mintázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f616-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="0f616-127">Ha nincs megadva blob-név, a parancsmag a megadott tároló összes blobját megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="0f616-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="0f616-128">Ha meg van adva egy érték a paraméterhez, a parancsmag az összes olyan blobot felsorolja, amely megfelel a paraméternek.</span><span class="sxs-lookup"><span data-stu-id="0f616-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f616-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0f616-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0f616-130">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="0f616-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0f616-131">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="0f616-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0f616-132">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="0f616-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0f616-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0f616-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0f616-134">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f616-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0f616-135">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="0f616-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0f616-136">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="0f616-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0f616-137">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="0f616-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0f616-138">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0f616-138">The default value is 10.</span></span>

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

### <span data-ttu-id="0f616-139">-Container</span><span class="sxs-lookup"><span data-stu-id="0f616-139">-Container</span></span>
<span data-ttu-id="0f616-140">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f616-140">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f616-141">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0f616-141">-Context</span></span>
<span data-ttu-id="0f616-142">Azt az Azure Storage-fiókot adja meg, amelyből meg szeretné kapni a Blobok listáját.</span><span class="sxs-lookup"><span data-stu-id="0f616-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="0f616-143">A New-AzureStorageContext parancsmagot használhatja a tárolási környezet létrehozására.</span><span class="sxs-lookup"><span data-stu-id="0f616-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="0f616-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="0f616-144">-ContinuationToken</span></span>
<span data-ttu-id="0f616-145">A blob-lista folytatólagos jogkivonatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f616-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="0f616-146">Ezzel a paraméterrel és a *MaxCount* paraméterrel több kötegben is listázhatja a Blobs-ket.</span><span class="sxs-lookup"><span data-stu-id="0f616-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f616-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f616-147">-DefaultProfile</span></span>
<span data-ttu-id="0f616-148">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f616-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f616-149">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="0f616-149">-IncludeDeleted</span></span>
<span data-ttu-id="0f616-150">A törölt blob hozzáadásával a blob alapértelmezés szerint nem fogja tartalmazni a törölt blobot.</span><span class="sxs-lookup"><span data-stu-id="0f616-150">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="0f616-151">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0f616-151">-MaxCount</span></span>
<span data-ttu-id="0f616-152">A parancsmag által visszaadott objektumok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f616-152">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="0f616-153">-Prefix</span><span class="sxs-lookup"><span data-stu-id="0f616-153">-Prefix</span></span>
<span data-ttu-id="0f616-154">Itt adhatja meg, hogy milyen blob-neveket szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="0f616-154">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="0f616-155">Ez a paraméter nem támogatja reguláris kifejezések és helyettesítő karakterek használatát a kereséshez.</span><span class="sxs-lookup"><span data-stu-id="0f616-155">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="0f616-156">Ez azt jelenti, hogy ha a tárolóban csak az "én", "MyBlob1", "MyBlob2" és "" nevű blobot adja meg, és a "-prefix My \*" értéket adja meg, akkor a parancsmag nem tartalmaz blobot.</span><span class="sxs-lookup"><span data-stu-id="0f616-156">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="0f616-157">Ha azonban a "-prefix My" értéket adja meg, a parancsmag a "saját", "MyBlob1" és a "MyBlob2" karakterláncot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0f616-157">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f616-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0f616-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0f616-159">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="0f616-159">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0f616-160">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="0f616-160">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0f616-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f616-161">CommonParameters</span></span>
<span data-ttu-id="0f616-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f616-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f616-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f616-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f616-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f616-164">INPUTS</span></span>

### <span data-ttu-id="0f616-165">System. String</span><span class="sxs-lookup"><span data-stu-id="0f616-165">System.String</span></span>

### <span data-ttu-id="0f616-166">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0f616-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0f616-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f616-167">OUTPUTS</span></span>

### <span data-ttu-id="0f616-168">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0f616-168">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="0f616-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f616-169">NOTES</span></span>

## <span data-ttu-id="0f616-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f616-170">RELATED LINKS</span></span>

[<span data-ttu-id="0f616-171">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0f616-171">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="0f616-172">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0f616-172">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="0f616-173">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0f616-173">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


