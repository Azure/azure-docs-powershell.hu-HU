---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158131"
---
# <span data-ttu-id="74cb7-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="74cb7-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="74cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="74cb7-103">Egy tárolóban lévő blobokat sorol fel.</span><span class="sxs-lookup"><span data-stu-id="74cb7-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="74cb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74cb7-104">SYNTAX</span></span>

### <span data-ttu-id="74cb7-105">BlobName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74cb7-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="74cb7-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="74cb7-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="74cb7-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="74cb7-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="74cb7-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="74cb7-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="74cb7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74cb7-109">DESCRIPTION</span></span>
<span data-ttu-id="74cb7-110">A **Get-AzStorageBlob** parancsmag egy Azure-tárfiók adott tárolóján lévő blobokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="74cb7-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="74cb7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74cb7-111">EXAMPLES</span></span>

### <span data-ttu-id="74cb7-112">1. példa: Blob lekérte a blob nevét</span><span class="sxs-lookup"><span data-stu-id="74cb7-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="74cb7-113">Ez a parancs blobnevet és helyettesítő karaktereket használ a blob lekérthez.</span><span class="sxs-lookup"><span data-stu-id="74cb7-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="74cb7-114">2. példa: Blobok lekérte egy tárolóban a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="74cb7-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="74cb7-115">Ez a parancs a folyamat segítségével behoz minden blobot (a Törölt állapotban lévő blobokat is) egy tárolóba.</span><span class="sxs-lookup"><span data-stu-id="74cb7-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="74cb7-116">3. példa: Blobok lekért névelőtagja</span><span class="sxs-lookup"><span data-stu-id="74cb7-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="74cb7-117">Ez a parancs egy névelőtagot használ a blobok leküldésekor.</span><span class="sxs-lookup"><span data-stu-id="74cb7-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="74cb7-118">4. példa: Több köteg blobos listájának létrehozása</span><span class="sxs-lookup"><span data-stu-id="74cb7-118">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="74cb7-119">Ebben a példában *a MaxCount* és *a ContinuationToken paramétert* használva több kötegben listába soroljuk az Azure Storage blobokat.</span><span class="sxs-lookup"><span data-stu-id="74cb7-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="74cb7-120">Az első négy parancs értékeket rendel a példában használt változókhoz.</span><span class="sxs-lookup"><span data-stu-id="74cb7-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="74cb7-121">Az ötödik parancs egy **Olyan Do-While utasítást** ad meg, amely a **Get-AzStorageBlob** parancsmagot használja a blobok be szereznie.</span><span class="sxs-lookup"><span data-stu-id="74cb7-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="74cb7-122">Az utasítás tartalmazza a $Token változóban tárolt $Token tokent.</span><span class="sxs-lookup"><span data-stu-id="74cb7-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="74cb7-123">$Token a hurok futásakor megváltozik az érték.</span><span class="sxs-lookup"><span data-stu-id="74cb7-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="74cb7-124">További információért írja be a `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="74cb7-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="74cb7-125">Az utolsó parancs a **Visszhang paranccsal** jeleníti meg az összeget.</span><span class="sxs-lookup"><span data-stu-id="74cb7-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="74cb7-126">5. példa: Egy tároló összes blobját le kell szereznie, amely tartalmazza a blobverziót</span><span class="sxs-lookup"><span data-stu-id="74cb7-126">Example 5: Get all blobs in a container include blob version</span></span>
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

<span data-ttu-id="74cb7-127">Ez a parancs a tárolók összes blobját beveszi, például a blobverziót.</span><span class="sxs-lookup"><span data-stu-id="74cb7-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="74cb7-128">6. példa: Egyetlen blobverzió lekérte</span><span class="sxs-lookup"><span data-stu-id="74cb7-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="74cb7-129">Ez a parancs egyetlen blob veriont kap a VersionId segítségével.</span><span class="sxs-lookup"><span data-stu-id="74cb7-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="74cb7-130">7. példa: Egyetlen blob-pillanatfelvétel készítése</span><span class="sxs-lookup"><span data-stu-id="74cb7-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="74cb7-131">Ez a parancs egyetlen blob-pillanatképet kap a SnapshotTime-val.</span><span class="sxs-lookup"><span data-stu-id="74cb7-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="74cb7-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74cb7-132">PARAMETERS</span></span>

### <span data-ttu-id="74cb7-133">-Blob</span><span class="sxs-lookup"><span data-stu-id="74cb7-133">-Blob</span></span>
<span data-ttu-id="74cb7-134">Egy nevet vagy egy névmintát ad meg, amely helyettesítő karakterekkel való keresésre használható.</span><span class="sxs-lookup"><span data-stu-id="74cb7-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="74cb7-135">Ha nincs megadva blobnév, a parancsmag felsorolja a megadott tároló összes blobját.</span><span class="sxs-lookup"><span data-stu-id="74cb7-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="74cb7-136">Ha a paraméterhez meg van adva egy érték, a parancsmag felsorolja az összes olyan blobot, amely megfelel ennek a paraméternek.</span><span class="sxs-lookup"><span data-stu-id="74cb7-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="74cb7-137">Ez a paraméter a karakterlánc bármely helyében támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="74cb7-137">This parameter supports wildcards anywhere in the string.</span></span>

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

### <span data-ttu-id="74cb7-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="74cb7-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="74cb7-139">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="74cb7-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="74cb7-140">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="74cb7-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="74cb7-141">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="74cb7-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="74cb7-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="74cb7-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="74cb7-143">Megadja a maximális párhuzamos hálózati hívást.</span><span class="sxs-lookup"><span data-stu-id="74cb7-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="74cb7-144">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="74cb7-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="74cb7-145">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="74cb7-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="74cb7-146">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="74cb7-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="74cb7-147">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="74cb7-147">The default value is 10.</span></span>

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

### <span data-ttu-id="74cb7-148">-Container</span><span class="sxs-lookup"><span data-stu-id="74cb7-148">-Container</span></span>
<span data-ttu-id="74cb7-149">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74cb7-149">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="74cb7-150">-Környezet</span><span class="sxs-lookup"><span data-stu-id="74cb7-150">-Context</span></span>
<span data-ttu-id="74cb7-151">Azt az Azure-tárfiókot adja meg, amelyből le szeretné kapni a blobok listáját.</span><span class="sxs-lookup"><span data-stu-id="74cb7-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="74cb7-152">A New-AzStorageContext környezet létrehozásához használhatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="74cb7-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="74cb7-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="74cb7-153">-ContinuationToken</span></span>
<span data-ttu-id="74cb7-154">A bloblista folytatására vonatkozó jogkivonatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="74cb7-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="74cb7-155">Ezt a paramétert és *a MaxCount paramétert* használva több kötegben is listába sorolhatja a blobokat.</span><span class="sxs-lookup"><span data-stu-id="74cb7-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

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

### <span data-ttu-id="74cb7-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74cb7-156">-DefaultProfile</span></span>
<span data-ttu-id="74cb7-157">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74cb7-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74cb7-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="74cb7-158">-IncludeDeleted</span></span>
<span data-ttu-id="74cb7-159">A Törölt blobok alapértelmezés szerint nem tartalmaznak törölt blobot.</span><span class="sxs-lookup"><span data-stu-id="74cb7-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="74cb7-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="74cb7-160">-IncludeVersion</span></span>
<span data-ttu-id="74cb7-161">A blobverziók csak akkor lesznek felsorolva, ha ez a paraméter jelen van, alapértelmezés szerint a blob lekért verziója nem tartalmaz blobverziókat.</span><span class="sxs-lookup"><span data-stu-id="74cb7-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

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

### <span data-ttu-id="74cb7-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="74cb7-162">-MaxCount</span></span>
<span data-ttu-id="74cb7-163">A parancsmag által visszaadott objektumok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="74cb7-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="74cb7-164">-Előtag</span><span class="sxs-lookup"><span data-stu-id="74cb7-164">-Prefix</span></span>
<span data-ttu-id="74cb7-165">Megadja a lekért blobnevek előtagját.</span><span class="sxs-lookup"><span data-stu-id="74cb7-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="74cb7-166">Ez a paraméter nem támogatja reguláris kifejezések vagy helyettesítő karakterek keresését.</span><span class="sxs-lookup"><span data-stu-id="74cb7-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="74cb7-167">Ez azt jelenti, hogy ha a tárolóban csak a "Saját", a "MyBlob1" és a "MyBlob2" nevű blobok vannak, és a "-Előtag my\*" értéket adja meg, a parancsmag nem ad vissza blobokat.</span><span class="sxs-lookup"><span data-stu-id="74cb7-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="74cb7-168">Ha azonban a "-Prefix My" értéket adja meg, a parancsmag a "Saját", a "MyBlob1" és a "MyBlob2" értéket adja vissza.</span><span class="sxs-lookup"><span data-stu-id="74cb7-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="74cb7-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="74cb7-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="74cb7-170">A szolgáltatás oldalának időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="74cb7-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="74cb7-171">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="74cb7-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="74cb7-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="74cb7-172">-SnapshotTime</span></span>
<span data-ttu-id="74cb7-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="74cb7-173">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="74cb7-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="74cb7-174">-VersionId</span></span>
<span data-ttu-id="74cb7-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="74cb7-175">Blob VersionId</span></span>

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

### <span data-ttu-id="74cb7-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cb7-176">CommonParameters</span></span>
<span data-ttu-id="74cb7-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74cb7-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cb7-178">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74cb7-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cb7-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74cb7-179">INPUTS</span></span>

### <span data-ttu-id="74cb7-180">System.String</span><span class="sxs-lookup"><span data-stu-id="74cb7-180">System.String</span></span>

### <span data-ttu-id="74cb7-181">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="74cb7-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="74cb7-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74cb7-182">OUTPUTS</span></span>

### <span data-ttu-id="74cb7-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="74cb7-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="74cb7-184">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74cb7-184">NOTES</span></span>

## <span data-ttu-id="74cb7-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74cb7-185">RELATED LINKS</span></span>

[<span data-ttu-id="74cb7-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="74cb7-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="74cb7-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="74cb7-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="74cb7-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="74cb7-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


