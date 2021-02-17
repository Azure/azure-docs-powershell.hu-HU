---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164723"
---
# <span data-ttu-id="fe52b-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fe52b-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="fe52b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe52b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe52b-103">Blob másolását kezdi.</span><span class="sxs-lookup"><span data-stu-id="fe52b-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="fe52b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe52b-104">SYNTAX</span></span>

### <span data-ttu-id="fe52b-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe52b-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe52b-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="fe52b-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe52b-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="fe52b-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe52b-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fe52b-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe52b-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="fe52b-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe52b-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="fe52b-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe52b-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="fe52b-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe52b-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="fe52b-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe52b-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="fe52b-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe52b-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="fe52b-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe52b-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe52b-115">DESCRIPTION</span></span>
<span data-ttu-id="fe52b-116">A **Start-AzStorageBlobCopy** parancsmag megkezdi a blob másolását.</span><span class="sxs-lookup"><span data-stu-id="fe52b-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="fe52b-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe52b-117">EXAMPLES</span></span>

### <span data-ttu-id="fe52b-118">1. példa: Elnevezett blob másolása</span><span class="sxs-lookup"><span data-stu-id="fe52b-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="fe52b-119">Ez a parancs elindítja a ContosoPlanning2015 nevű blob másolási műveletét a ContosoUploads nevű tárolóból a ContosoArchives nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="fe52b-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="fe52b-120">2. példa: A másolni kívánt blobok megadására szolgáló tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="fe52b-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="fe52b-121">Ez a parancs a **Get-AzStorageContainer** parancsmag használatával megkapja a ContosoUploads nevű tárolót, majd a folyamat műveleti operátorával átadja a tárolót az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fe52b-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe52b-122">Ez a parancsmag elindítja a ContosoPlanning2015 nevű blob másolási műveletét.</span><span class="sxs-lookup"><span data-stu-id="fe52b-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="fe52b-123">Az előző parancsmag biztosítja a forrástárolót.</span><span class="sxs-lookup"><span data-stu-id="fe52b-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="fe52b-124">A *DestContainer paraméter* a ContosoArchives paramétert adja meg céltárolóként.</span><span class="sxs-lookup"><span data-stu-id="fe52b-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="fe52b-125">3. példa: Egy tároló összes blobja be- és másolása</span><span class="sxs-lookup"><span data-stu-id="fe52b-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="fe52b-126">Ez a parancs a ContosoUploads nevű tárolóban lévő blobokat a **Get-AzStorageBlob** parancsmag használatával kapja meg, majd a folyamat műveleti operátorával átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fe52b-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe52b-127">Ez a parancsmag elindítja a blobok másolási műveletét a ContosoArchives nevű tárolóra.</span><span class="sxs-lookup"><span data-stu-id="fe52b-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="fe52b-128">4. példa: Objektumként megadott blob másolása</span><span class="sxs-lookup"><span data-stu-id="fe52b-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="fe52b-129">Az első parancs a ContosoPlanning2015 nevű blobot kapja meg a ContosoUploads nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="fe52b-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="fe52b-130">A parancs az objektumot a $SrcBlob tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe52b-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="fe52b-131">A második parancs a ContosoPlanning2015Archived nevű blobot kapja meg a ContosoArchives nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="fe52b-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="fe52b-132">A parancs az objektumot a $DestBlob tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe52b-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="fe52b-133">Az utolsó parancs elindítja a másolási műveletet a forrástárolóból a céltárolóba.</span><span class="sxs-lookup"><span data-stu-id="fe52b-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="fe52b-134">A parancs szabványos pontként használja az **ICloudBlob-objektumokat** a $SrcBlob és $DestBlob meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="fe52b-135">5. példa: Blob másolása URI-ból</span><span class="sxs-lookup"><span data-stu-id="fe52b-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="fe52b-136">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a kulcsot a $Context tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe52b-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="fe52b-137">A második parancs átmásolja a fájlt a megadott URI-ból a ContosoPlanning nevű blobba a ContosoArchive nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="fe52b-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="fe52b-138">A parancs a másolási műveletet a helyi menüben tárolt célkörnyezetbe $Context.</span><span class="sxs-lookup"><span data-stu-id="fe52b-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="fe52b-139">Nincs forrástárolási környezet, ezért a forrás uri-nak hozzáféréssel kell lennie a forrásobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="fe52b-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="fe52b-140">Például: ha a forrás nincs nyilvános Azure blob, az Uri-nak TARTALMAZNIA kell SAS-jogkivonatot, amely olvasási hozzáféréssel rendelkezik a blobhoz.</span><span class="sxs-lookup"><span data-stu-id="fe52b-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="fe52b-141">6. példa: Blokk blob másolása céltárolóba új blobnévvel, és a cél blob StandardBlobTier beállítása Hot, RehidrasztálásPriority magasként</span><span class="sxs-lookup"><span data-stu-id="fe52b-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="fe52b-142">Ez a parancs elindítja egy blokk blob másolási műveletét céltárolóba egy új blobnévvel, és a cél blob StandardBlobTier-ját Hot, RehidrasztálásPriority magasra állítva</span><span class="sxs-lookup"><span data-stu-id="fe52b-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="fe52b-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe52b-143">PARAMETERS</span></span>

### <span data-ttu-id="fe52b-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="fe52b-144">-AbsoluteUri</span></span>
<span data-ttu-id="fe52b-145">Egy Azure-tár blobba másolt fájl abszolút URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="fe52b-146">-BlobBaseClient</span></span>
<span data-ttu-id="fe52b-147">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="fe52b-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fe52b-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fe52b-149">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="fe52b-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fe52b-150">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="fe52b-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fe52b-151">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="fe52b-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fe52b-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="fe52b-152">-CloudBlob</span></span>
<span data-ttu-id="fe52b-153">Egy **CloudBlob-objektumot** ad meg az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="fe52b-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="fe52b-154">**CloudBlob-objektum** beszerzéséhez használja a Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe52b-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="fe52b-155">-CloudBlobContainer</span></span>
<span data-ttu-id="fe52b-156">Egy **CloudBlobContainer-objektumot** ad meg az Azure Storage Client tárból.</span><span class="sxs-lookup"><span data-stu-id="fe52b-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="fe52b-157">Ez a parancsmag egy blobot másol a paraméter által megadott tárolóból.</span><span class="sxs-lookup"><span data-stu-id="fe52b-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="fe52b-158">**CloudBlobContainer-objektum** beszerzéséhez használja a Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe52b-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fe52b-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fe52b-160">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="fe52b-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fe52b-161">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="fe52b-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fe52b-162">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="fe52b-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fe52b-163">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="fe52b-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fe52b-164">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="fe52b-164">The default value is 10.</span></span>

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

### <span data-ttu-id="fe52b-165">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fe52b-165">-Context</span></span>
<span data-ttu-id="fe52b-166">Egy Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fe52b-167">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe52b-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe52b-168">-DefaultProfile</span></span>
<span data-ttu-id="fe52b-169">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe52b-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe52b-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="fe52b-170">-DestBlob</span></span>
<span data-ttu-id="fe52b-171">A cél blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="fe52b-172">-DestCloudBlob</span></span>
<span data-ttu-id="fe52b-173">A **CloudBlob-objektum célhelyét** adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="fe52b-174">-DestContainer</span></span>
<span data-ttu-id="fe52b-175">A céltároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="fe52b-176">-DestContext</span></span>
<span data-ttu-id="fe52b-177">Egy Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fe52b-178">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe52b-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-179">-Force</span><span class="sxs-lookup"><span data-stu-id="fe52b-179">-Force</span></span>
<span data-ttu-id="fe52b-180">Azt jelzi, hogy ez a parancsmag felülírja a cél blobot anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fe52b-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fe52b-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="fe52b-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="fe52b-182">Prémium lap blobrétege</span><span class="sxs-lookup"><span data-stu-id="fe52b-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-183">-RehidradvePriority</span><span class="sxs-lookup"><span data-stu-id="fe52b-183">-RehydratePriority</span></span>
<span data-ttu-id="fe52b-184">Blob RehidrasztálásPrioritás blokkolása</span><span class="sxs-lookup"><span data-stu-id="fe52b-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="fe52b-185">Az archivált blob rehidrálásának prioritása.</span><span class="sxs-lookup"><span data-stu-id="fe52b-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="fe52b-186">Érvényes értékek: High/Standard.</span><span class="sxs-lookup"><span data-stu-id="fe52b-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fe52b-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fe52b-188">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="fe52b-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fe52b-189">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="fe52b-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fe52b-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="fe52b-190">-SrcBlob</span></span>
<span data-ttu-id="fe52b-191">A forrás blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="fe52b-192">-SrcContainer</span></span>
<span data-ttu-id="fe52b-193">A forrástároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-193">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="fe52b-194">-SrcDir</span></span>
<span data-ttu-id="fe52b-195">Egy **CloudFileDirectory objektumot** ad meg az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="fe52b-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="fe52b-196">-SrcFile</span></span>
<span data-ttu-id="fe52b-197">Egy **CloudFile-objektumot ad** meg az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="fe52b-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="fe52b-198">Létrehozhatja, vagy használhatja Get-AzStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe52b-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="fe52b-199">-SrcFilePath</span></span>
<span data-ttu-id="fe52b-200">A forráscímtár vagy forrásmegosztás relatív elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="fe52b-201">-SrcShare</span></span>
<span data-ttu-id="fe52b-202">Egy **CloudFileShare-objektumot** ad meg az Azure Storage Client-tárból.</span><span class="sxs-lookup"><span data-stu-id="fe52b-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="fe52b-203">Létrehozhatja, vagy használhatja Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe52b-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="fe52b-204">-SrcShareName</span></span>
<span data-ttu-id="fe52b-205">A forrás megosztási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe52b-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="fe52b-206">-StandardBlobTier</span></span>
<span data-ttu-id="fe52b-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="fe52b-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="fe52b-208">Részleteket itt láthat: https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="fe52b-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe52b-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe52b-209">-Confirm</span></span>
<span data-ttu-id="fe52b-210">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fe52b-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe52b-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe52b-211">-WhatIf</span></span>
<span data-ttu-id="fe52b-212">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fe52b-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe52b-213">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe52b-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe52b-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe52b-214">CommonParameters</span></span>
<span data-ttu-id="fe52b-215">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe52b-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe52b-216">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe52b-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe52b-217">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe52b-217">INPUTS</span></span>

### <span data-ttu-id="fe52b-218">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="fe52b-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="fe52b-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="fe52b-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="fe52b-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="fe52b-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="fe52b-221">System.String</span><span class="sxs-lookup"><span data-stu-id="fe52b-221">System.String</span></span>

### <span data-ttu-id="fe52b-222">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe52b-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fe52b-223">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe52b-223">OUTPUTS</span></span>

### <span data-ttu-id="fe52b-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="fe52b-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="fe52b-225">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe52b-225">NOTES</span></span>

## <span data-ttu-id="fe52b-226">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe52b-226">RELATED LINKS</span></span>

[<span data-ttu-id="fe52b-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="fe52b-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="fe52b-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fe52b-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
