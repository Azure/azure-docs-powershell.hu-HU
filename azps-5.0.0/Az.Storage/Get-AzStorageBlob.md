---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195078"
---
# <span data-ttu-id="5da5a-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5da5a-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="5da5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5da5a-102">SYNOPSIS</span></span>
<span data-ttu-id="5da5a-103">A tárolóban lévő Blobs listák.</span><span class="sxs-lookup"><span data-stu-id="5da5a-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="5da5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5da5a-104">SYNTAX</span></span>

### <span data-ttu-id="5da5a-105">BlobName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5da5a-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5da5a-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="5da5a-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5da5a-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="5da5a-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5da5a-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="5da5a-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5da5a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5da5a-109">DESCRIPTION</span></span>
<span data-ttu-id="5da5a-110">A **Get-AzStorageBlob** parancsmag a megadott tárolóban lévő blobokat az Azure Storage-fiókban sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="5da5a-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="5da5a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5da5a-111">EXAMPLES</span></span>

### <span data-ttu-id="5da5a-112">Példa 1: blobos név beszerzése</span><span class="sxs-lookup"><span data-stu-id="5da5a-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="5da5a-113">Ez a parancs egy blob-nevet és egy helyettesítő karaktert használ a blob beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="5da5a-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="5da5a-114">2. példa: a festékfoltok beolvasása a tárolóban a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="5da5a-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="5da5a-115">Ez a parancs a csővezetéken a tárolóban lévő összes blobot (a törölt állapotban lévő Blobs-objektumokat is tartalmazza) fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5da5a-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="5da5a-116">3. példa: a festékfoltok beolvasása név előtaggal</span><span class="sxs-lookup"><span data-stu-id="5da5a-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="5da5a-117">Ez a parancs egy név előtagot használ a festékfoltok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="5da5a-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="5da5a-118">Példa 4: a lista festékfoltok több kötegben</span><span class="sxs-lookup"><span data-stu-id="5da5a-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="5da5a-119">Ebben a példában a *MaxCount* és a *ContinuationToken* paraméterrel több kötegben listázhatja az Azure Storage blob-ket.</span><span class="sxs-lookup"><span data-stu-id="5da5a-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="5da5a-120">Az első négy parancs az értékeket a példában használt változókhoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="5da5a-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="5da5a-121">Az ötödik parancs a **Get-AzStorageBlob** parancsmagot használó **do-while** utasítást ad meg a Blobs-adatok beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="5da5a-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="5da5a-122">Az utasítás tartalmazza a $Token változóban tárolt folytatólagos tokent.</span><span class="sxs-lookup"><span data-stu-id="5da5a-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="5da5a-123">$Token az érték ismétléssel változik.</span><span class="sxs-lookup"><span data-stu-id="5da5a-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="5da5a-124">További információért írja be a következőt: `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="5da5a-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="5da5a-125">A végleges parancs a **echo** parancs segítségével jeleníti meg a végösszeget.</span><span class="sxs-lookup"><span data-stu-id="5da5a-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="5da5a-126">Példa 5: a tároló összes blobjának beolvasása blob-verzióval</span><span class="sxs-lookup"><span data-stu-id="5da5a-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="5da5a-127">Ez a parancs a tárolóban található összes blobot beilleszti a blob-verzióba.</span><span class="sxs-lookup"><span data-stu-id="5da5a-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="5da5a-128">Példa 6: egyetlen blob-verzió beszerzése</span><span class="sxs-lookup"><span data-stu-id="5da5a-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="5da5a-129">Ez a parancs a VersionId-nal egyetlen bináris verzióját kap.</span><span class="sxs-lookup"><span data-stu-id="5da5a-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="5da5a-130">7. példa: egyetlen blob-pillanatfelvétel beszerzése</span><span class="sxs-lookup"><span data-stu-id="5da5a-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="5da5a-131">Ez a parancs egyetlen blob-pillanatfelvételt kap a SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="5da5a-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="5da5a-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5da5a-132">PARAMETERS</span></span>

### <span data-ttu-id="5da5a-133">-BLOB</span><span class="sxs-lookup"><span data-stu-id="5da5a-133">-Blob</span></span>
<span data-ttu-id="5da5a-134">A helyettesítő karakteres kereséshez használható név vagy név mintázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5da5a-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="5da5a-135">Ha nincs megadva blob-név, a parancsmag a megadott tároló összes blobját megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="5da5a-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="5da5a-136">Ha meg van adva egy érték a paraméterhez, a parancsmag az összes olyan blobot felsorolja, amely megfelel a paraméternek.</span><span class="sxs-lookup"><span data-stu-id="5da5a-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="5da5a-137">Ez a paraméter a karakterláncban bárhol a helyettesítő karaktereket támogatja.</span><span class="sxs-lookup"><span data-stu-id="5da5a-137">This parameter supports wildcards anywhere in the string.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da5a-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5da5a-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5da5a-139">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="5da5a-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5da5a-140">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="5da5a-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5da5a-141">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="5da5a-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5da5a-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5da5a-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5da5a-143">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="5da5a-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5da5a-144">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="5da5a-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5da5a-145">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="5da5a-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5da5a-146">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="5da5a-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5da5a-147">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="5da5a-147">The default value is 10.</span></span>

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

### <span data-ttu-id="5da5a-148">-Container</span><span class="sxs-lookup"><span data-stu-id="5da5a-148">-Container</span></span>
<span data-ttu-id="5da5a-149">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5da5a-149">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="5da5a-150">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5da5a-150">-Context</span></span>
<span data-ttu-id="5da5a-151">Azt az Azure Storage-fiókot adja meg, amelyből meg szeretné kapni a Blobok listáját.</span><span class="sxs-lookup"><span data-stu-id="5da5a-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="5da5a-152">A New-AzStorageContext parancsmagot használhatja a tárolási környezet létrehozására.</span><span class="sxs-lookup"><span data-stu-id="5da5a-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="5da5a-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="5da5a-153">-ContinuationToken</span></span>
<span data-ttu-id="5da5a-154">A blob-lista folytatólagos jogkivonatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5da5a-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="5da5a-155">Ezzel a paraméterrel és a *MaxCount* paraméterrel több kötegben is listázhatja a Blobs-ket.</span><span class="sxs-lookup"><span data-stu-id="5da5a-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da5a-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da5a-156">-DefaultProfile</span></span>
<span data-ttu-id="5da5a-157">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5da5a-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da5a-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="5da5a-158">-IncludeDeleted</span></span>
<span data-ttu-id="5da5a-159">A törölt blob hozzáadásával a blob alapértelmezés szerint nem fogja tartalmazni a törölt blobot.</span><span class="sxs-lookup"><span data-stu-id="5da5a-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="5da5a-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="5da5a-160">-IncludeVersion</span></span>
<span data-ttu-id="5da5a-161">A blob-verziók csak akkor jelennek meg a listában, ha ez a paraméter létezik, alapértelmezés szerint a blob nem tartalmaz blob-verziókat.</span><span class="sxs-lookup"><span data-stu-id="5da5a-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da5a-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5da5a-162">-MaxCount</span></span>
<span data-ttu-id="5da5a-163">A parancsmag által visszaadott objektumok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5da5a-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="5da5a-164">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5da5a-164">-Prefix</span></span>
<span data-ttu-id="5da5a-165">Itt adhatja meg, hogy milyen blob-neveket szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="5da5a-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="5da5a-166">Ez a paraméter nem támogatja reguláris kifejezések és helyettesítő karakterek használatát a kereséshez.</span><span class="sxs-lookup"><span data-stu-id="5da5a-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="5da5a-167">Ez azt jelenti, hogy ha a tárolóban csak az "én", "MyBlob1", "MyBlob2" és "" nevű blobot adja meg, és a "-prefix My \*" értéket adja meg, akkor a parancsmag nem tartalmaz blobot.</span><span class="sxs-lookup"><span data-stu-id="5da5a-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="5da5a-168">Ha azonban a "-prefix My" értéket adja meg, a parancsmag a "saját", "MyBlob1" és a "MyBlob2" karakterláncot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5da5a-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="5da5a-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5da5a-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5da5a-170">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="5da5a-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="5da5a-171">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="5da5a-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="5da5a-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="5da5a-172">-SnapshotTime</span></span>
<span data-ttu-id="5da5a-173">BLOB SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="5da5a-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da5a-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="5da5a-174">-VersionId</span></span>
<span data-ttu-id="5da5a-175">BLOB VersionId</span><span class="sxs-lookup"><span data-stu-id="5da5a-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da5a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da5a-176">CommonParameters</span></span>
<span data-ttu-id="5da5a-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5da5a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da5a-178">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da5a-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da5a-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5da5a-179">INPUTS</span></span>

### <span data-ttu-id="5da5a-180">System. String</span><span class="sxs-lookup"><span data-stu-id="5da5a-180">System.String</span></span>

### <span data-ttu-id="5da5a-181">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5da5a-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5da5a-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5da5a-182">OUTPUTS</span></span>

### <span data-ttu-id="5da5a-183">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5da5a-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="5da5a-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5da5a-184">NOTES</span></span>

## <span data-ttu-id="5da5a-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5da5a-185">RELATED LINKS</span></span>

[<span data-ttu-id="5da5a-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5da5a-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="5da5a-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5da5a-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="5da5a-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5da5a-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


