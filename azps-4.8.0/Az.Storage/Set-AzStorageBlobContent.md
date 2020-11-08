---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: a71995015a8345b3ba181d92ba17e4dd258b169b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024293"
---
# <span data-ttu-id="72381-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="72381-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="72381-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72381-102">SYNOPSIS</span></span>
<span data-ttu-id="72381-103">Egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="72381-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="72381-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72381-104">SYNTAX</span></span>

### <span data-ttu-id="72381-105">SendManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72381-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72381-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="72381-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72381-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="72381-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72381-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="72381-108">DESCRIPTION</span></span>
<span data-ttu-id="72381-109">A **set-AzStorageBlobContent** parancsmag egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="72381-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="72381-110">Példák</span><span class="sxs-lookup"><span data-stu-id="72381-110">EXAMPLES</span></span>

### <span data-ttu-id="72381-111">1. példa: névvel ellátott fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="72381-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="72381-112">Ez a parancs feltölti a PlanningData nevű fájlt egy Planning2015 nevű blobtal.</span><span class="sxs-lookup"><span data-stu-id="72381-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="72381-113">2. példa: az aktuális mappa alatti fájlok feltöltése</span><span class="sxs-lookup"><span data-stu-id="72381-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="72381-114">Ez a parancs az alapszintű Windows PowerShell-parancsmagot használja Get-ChildItem az aktuális mappában és az almappákban lévő összes fájl letöltéséhez, majd a csővezeték-kezelő használatával átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="72381-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="72381-115">A **set-AzStorageBlobContent** parancsmag a fájlokat a ContosoUploads nevű tárolóba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="72381-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="72381-116">3. példa: meglévő blob felülírása</span><span class="sxs-lookup"><span data-stu-id="72381-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="72381-117">Ez a parancs a Planning2015 nevű blobot az ContosoUploads-tárolóban kapja meg az Get-AzStorageBlob parancsmag használatával, majd ezt a blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="72381-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="72381-118">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="72381-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="72381-119">Ez a parancs nem adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="72381-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="72381-120">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="72381-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="72381-121">Ha jóváhagyja a parancsot, a parancsmag felülírja a meglévő blobot.</span><span class="sxs-lookup"><span data-stu-id="72381-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="72381-122">4. példa: fájlok feltöltése tárolóba a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="72381-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="72381-123">Ez a parancs a **Get-AzStorageContainer** parancsmaggal kezdődően a karakterlánc ContosoUpload kezdődő tárolót kapja, majd az adott blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="72381-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="72381-124">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="72381-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="72381-125">5. példa: fájl feltöltése a lap blob-ba metaadatokkal és PremiumPageBlobTier mint P10</span><span class="sxs-lookup"><span data-stu-id="72381-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="72381-126">Az első parancs létrehoz egy hash-táblázatot, amely egy blob metaadatait tartalmazza, és a hash-táblázatot a $Metadata változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72381-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="72381-127">A második parancs feltölti a ContosoPlanning nevű fájlt a ContosoUploads nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="72381-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="72381-128">A blob tartalmazza a $Metadataban tárolt metaadatokat, és a PremiumPageBlobTier a P10.</span><span class="sxs-lookup"><span data-stu-id="72381-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="72381-129">Példa 6: fájl feltöltése a blob-ra megadott blob-tulajdonságokkal, és a StandardBlobTier beállítása cool</span><span class="sxs-lookup"><span data-stu-id="72381-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="72381-130">A parancs feltölti a fájlt c:\temp\index.html-re a contosouploads nevű tárolóhoz megadott blob-tulajdonságokkal, és beállíthatja a StandardBlobTier.</span><span class="sxs-lookup"><span data-stu-id="72381-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="72381-131">Ez a parancs a [System. Web. MimeMapping]:: GetMimeMapping () API-val megadhatja a blob-tulajdonságok ContentType értékét.</span><span class="sxs-lookup"><span data-stu-id="72381-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

## <span data-ttu-id="72381-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72381-132">PARAMETERS</span></span>

### <span data-ttu-id="72381-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72381-133">-AsJob</span></span>
<span data-ttu-id="72381-134">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="72381-134">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="72381-135">-BLOB</span><span class="sxs-lookup"><span data-stu-id="72381-135">-Blob</span></span>
<span data-ttu-id="72381-136">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72381-136">Specifies the name of a blob.</span></span>
<span data-ttu-id="72381-137">Ez a parancsmag olyan fájlt tölt fel az Azure Storage blob szolgáltatásba, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="72381-137">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72381-138">-BlobType</span><span class="sxs-lookup"><span data-stu-id="72381-138">-BlobType</span></span>
<span data-ttu-id="72381-139">A parancsmag által feltöltött blob típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="72381-139">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="72381-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="72381-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72381-141">Letiltása</span><span class="sxs-lookup"><span data-stu-id="72381-141">Block</span></span>
- <span data-ttu-id="72381-142">Lap: az alapértelmezett érték a blokk.</span><span class="sxs-lookup"><span data-stu-id="72381-142">Page The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72381-143">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72381-143">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="72381-144">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="72381-144">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="72381-145">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="72381-145">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="72381-146">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="72381-146">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="72381-147">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="72381-147">-CloudBlob</span></span>
<span data-ttu-id="72381-148">Egy **CloudBlob** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="72381-148">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="72381-149">**CloudBlob** objektum beolvasásához használja az Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="72381-149">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="72381-150">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="72381-150">-CloudBlobContainer</span></span>
<span data-ttu-id="72381-151">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="72381-151">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="72381-152">Ez a parancsmag feltölti a tartalmat a tárolóban lévő blobra, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="72381-152">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="72381-153">**CloudBlobContainer** objektum beolvasásához használja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="72381-153">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="72381-154">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="72381-154">-ConcurrentTaskCount</span></span>
<span data-ttu-id="72381-155">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="72381-155">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="72381-156">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="72381-156">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="72381-157">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="72381-157">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="72381-158">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="72381-158">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="72381-159">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="72381-159">The default value is 10.</span></span>

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

### <span data-ttu-id="72381-160">-Container</span><span class="sxs-lookup"><span data-stu-id="72381-160">-Container</span></span>
<span data-ttu-id="72381-161">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72381-161">Specifies the name of a container.</span></span>
<span data-ttu-id="72381-162">Ez a parancsmag a paraméter által megadott tárolóban lévő blobra tölti fel a fájlt.</span><span class="sxs-lookup"><span data-stu-id="72381-162">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72381-163">-Környezet</span><span class="sxs-lookup"><span data-stu-id="72381-163">-Context</span></span>
<span data-ttu-id="72381-164">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72381-164">Specifies an Azure storage context.</span></span>
<span data-ttu-id="72381-165">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="72381-165">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="72381-166">Ha egy, a SAS-jogkivonatból létrehozott tárterületet olvasási engedély nélkül szeretne használni, az Add-Force paraméterrel kell kihagynia a blob-jelenléti érték kihagyását.</span><span class="sxs-lookup"><span data-stu-id="72381-166">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="72381-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72381-167">-DefaultProfile</span></span>
<span data-ttu-id="72381-168">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72381-168">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72381-169">-Fájl</span><span class="sxs-lookup"><span data-stu-id="72381-169">-File</span></span>
<span data-ttu-id="72381-170">Annak a fájlnak a helyi elérési útját adja meg, amely blob-fájlként tölthető fel.</span><span class="sxs-lookup"><span data-stu-id="72381-170">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72381-171">-Force</span><span class="sxs-lookup"><span data-stu-id="72381-171">-Force</span></span>
<span data-ttu-id="72381-172">Jelzi, hogy ez a parancsmag felülír egy meglévő blobot, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72381-172">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="72381-173">-Metadata</span><span class="sxs-lookup"><span data-stu-id="72381-173">-Metadata</span></span>
<span data-ttu-id="72381-174">A feltöltött blob metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="72381-174">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72381-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="72381-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="72381-176">Lap blob-rétege</span><span class="sxs-lookup"><span data-stu-id="72381-176">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72381-177">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="72381-177">-Properties</span></span>
<span data-ttu-id="72381-178">A feltöltött blob tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="72381-178">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="72381-179">A támogatott tulajdonságok a következők: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="72381-179">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72381-180">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72381-180">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="72381-181">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="72381-181">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="72381-182">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="72381-182">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="72381-183">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="72381-183">-StandardBlobTier</span></span>
<span data-ttu-id="72381-184">BLOB-szint letiltása: az érvényes értékek a meleg/hűvös/Archívek.</span><span class="sxs-lookup"><span data-stu-id="72381-184">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="72381-185">Részletes tudnivalók https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="72381-185">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="72381-186">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72381-186">-Confirm</span></span>
<span data-ttu-id="72381-187">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72381-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72381-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72381-188">-WhatIf</span></span>
<span data-ttu-id="72381-189">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72381-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72381-190">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72381-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72381-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72381-191">CommonParameters</span></span>
<span data-ttu-id="72381-192">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72381-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72381-193">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72381-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72381-194">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72381-194">INPUTS</span></span>

### <span data-ttu-id="72381-195">System. String</span><span class="sxs-lookup"><span data-stu-id="72381-195">System.String</span></span>

### <span data-ttu-id="72381-196">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="72381-196">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="72381-197">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="72381-197">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="72381-198">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="72381-198">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72381-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72381-199">OUTPUTS</span></span>

### <span data-ttu-id="72381-200">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="72381-200">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="72381-201">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72381-201">NOTES</span></span>

## <span data-ttu-id="72381-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72381-202">RELATED LINKS</span></span>

[<span data-ttu-id="72381-203">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="72381-203">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="72381-204">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="72381-204">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="72381-205">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="72381-205">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
