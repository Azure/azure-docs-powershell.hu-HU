---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: edc2a178ac8fa1c3a009830decb62d60ece2a367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494239"
---
# <span data-ttu-id="9e513-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9e513-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="9e513-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e513-102">SYNOPSIS</span></span>
<span data-ttu-id="9e513-103">Egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="9e513-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e513-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e513-104">SYNTAX</span></span>

### <span data-ttu-id="9e513-105">SendManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e513-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e513-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="9e513-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e513-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="9e513-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e513-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e513-108">DESCRIPTION</span></span>
<span data-ttu-id="9e513-109">A **set-AzureStorageBlobContent** parancsmag egy helyi fájlt tölt fel egy Azure Storage blob-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="9e513-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="9e513-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9e513-110">EXAMPLES</span></span>

### <span data-ttu-id="9e513-111">1. példa: névvel ellátott fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="9e513-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="9e513-112">Ez a parancs feltölti a PlanningData nevű fájlt egy Planning2015 nevű blobtal.</span><span class="sxs-lookup"><span data-stu-id="9e513-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="9e513-113">2. példa: az aktuális mappa alatti fájlok feltöltése</span><span class="sxs-lookup"><span data-stu-id="9e513-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="9e513-114">Ez a parancs az alapszintű Windows PowerShell-parancsmagot használja Get-ChildItem az aktuális mappában és az almappákban lévő összes fájl letöltéséhez, majd a csővezeték-kezelő használatával átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="9e513-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e513-115">A **set-AzureStorageBlobContent** parancsmag a fájlokat a ContosoUploads nevű tárolóba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="9e513-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="9e513-116">3. példa: meglévő blob felülírása</span><span class="sxs-lookup"><span data-stu-id="9e513-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="9e513-117">Ez a parancs a Planning2015 nevű blobot az ContosoUploads-tárolóban kapja meg az Get-AzureStorageBlob parancsmag használatával, majd ezt a blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="9e513-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="9e513-118">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="9e513-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="9e513-119">Ez a parancs nem adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="9e513-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="9e513-120">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="9e513-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="9e513-121">Ha jóváhagyja a parancsot, a parancsmag felülírja a meglévő blobot.</span><span class="sxs-lookup"><span data-stu-id="9e513-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="9e513-122">4. példa: fájlok feltöltése tárolóba a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="9e513-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="9e513-123">Ez a parancs a **Get-AzureStorageContainer** parancsmaggal kezdődően a karakterlánc ContosoUpload kezdődő tárolót kapja, majd az adott blobot átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="9e513-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="9e513-124">A parancs feltölti a ContosoPlanning nevű fájlt Planning2015-ként.</span><span class="sxs-lookup"><span data-stu-id="9e513-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="9e513-125">5. példa: fájl feltöltése a lap blob-ba metaadatokkal és PremiumPageBlobTier mint P10</span><span class="sxs-lookup"><span data-stu-id="9e513-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="9e513-126">Az első parancs létrehoz egy hash-táblázatot, amely egy blob metaadatait tartalmazza, és a hash-táblázatot a $Metadata változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9e513-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="9e513-127">A második parancs feltölti a ContosoPlanning nevű fájlt a ContosoUploads nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="9e513-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="9e513-128">A blob tartalmazza a $Metadataban tárolt metaadatokat, és a PremiumPageBlobTier a P10.</span><span class="sxs-lookup"><span data-stu-id="9e513-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="9e513-129">Példa 6: fájl feltöltése a blob-ra megadott blob-tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="9e513-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="9e513-130">Ez a parancs feltölti a ContosoPlanning nevű fájlt a ContosoUploads nevű tárolóhoz megadott blob-tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="9e513-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="9e513-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e513-131">PARAMETERS</span></span>

### <span data-ttu-id="9e513-132">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9e513-132">-Blob</span></span>
<span data-ttu-id="9e513-133">A blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="9e513-134">Ez a parancsmag olyan fájlt tölt fel az Azure Storage blob szolgáltatásba, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e513-135">-BlobType</span><span class="sxs-lookup"><span data-stu-id="9e513-135">-BlobType</span></span>
<span data-ttu-id="9e513-136">A parancsmag által feltöltött blob típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="9e513-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="9e513-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9e513-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e513-138">Letiltása</span><span class="sxs-lookup"><span data-stu-id="9e513-138">Block</span></span>
- <span data-ttu-id="9e513-139">Lap: az alapértelmezett érték a blokk.</span><span class="sxs-lookup"><span data-stu-id="9e513-139">Page The default value is Block.</span></span>

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

### <span data-ttu-id="9e513-140">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e513-140">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9e513-141">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="9e513-141">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9e513-142">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="9e513-142">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9e513-143">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="9e513-143">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9e513-144">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9e513-144">-CloudBlob</span></span>
<span data-ttu-id="9e513-145">Egy **CloudBlob** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-145">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="9e513-146">**CloudBlob** objektum beolvasásához használja az Get-AzureStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9e513-146">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="9e513-147">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9e513-147">-CloudBlobContainer</span></span>
<span data-ttu-id="9e513-148">Egy **CloudBlobContainer** -objektumot ad meg az Azure Storage Client könyvtárból.</span><span class="sxs-lookup"><span data-stu-id="9e513-148">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="9e513-149">Ez a parancsmag feltölti a tartalmat a tárolóban lévő blobra, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-149">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="9e513-150">**CloudBlobContainer** objektum beolvasásához használja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9e513-150">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="9e513-151">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9e513-151">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9e513-152">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-152">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9e513-153">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="9e513-153">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9e513-154">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="9e513-154">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9e513-155">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="9e513-155">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9e513-156">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="9e513-156">The default value is 10.</span></span>

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

### <span data-ttu-id="9e513-157">-Container</span><span class="sxs-lookup"><span data-stu-id="9e513-157">-Container</span></span>
<span data-ttu-id="9e513-158">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-158">Specifies the name of a container.</span></span>
<span data-ttu-id="9e513-159">Ez a parancsmag a paraméter által megadott tárolóban lévő blobra tölti fel a fájlt.</span><span class="sxs-lookup"><span data-stu-id="9e513-159">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e513-160">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9e513-160">-Context</span></span>
<span data-ttu-id="9e513-161">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-161">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9e513-162">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9e513-162">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="9e513-163">Ha egy, a SAS-jogkivonatból létrehozott tárterületet olvasási engedély nélkül szeretne használni, az Add-Force paraméterrel kell kihagynia a blob-ellenőrzés létezésének kihagyását.</span><span class="sxs-lookup"><span data-stu-id="9e513-163">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existance.</span></span>

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

### <span data-ttu-id="9e513-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e513-164">-DefaultProfile</span></span>
<span data-ttu-id="9e513-165">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e513-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e513-166">-Fájl</span><span class="sxs-lookup"><span data-stu-id="9e513-166">-File</span></span>
<span data-ttu-id="9e513-167">Annak a fájlnak a helyi elérési útját adja meg, amely blob-fájlként tölthető fel.</span><span class="sxs-lookup"><span data-stu-id="9e513-167">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="9e513-168">-Force</span><span class="sxs-lookup"><span data-stu-id="9e513-168">-Force</span></span>
<span data-ttu-id="9e513-169">Jelzi, hogy ez a parancsmag felülír egy meglévő blobot, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e513-169">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9e513-170">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9e513-170">-Metadata</span></span>
<span data-ttu-id="9e513-171">A feltöltött blob metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-171">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="9e513-172">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="9e513-172">-PremiumPageBlobTier</span></span>
<span data-ttu-id="9e513-173">Lap blob-rétege</span><span class="sxs-lookup"><span data-stu-id="9e513-173">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e513-174">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="9e513-174">-Properties</span></span>
<span data-ttu-id="9e513-175">A feltöltött blob tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e513-175">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="9e513-176">A támogatott tulajdonságok a következők: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="9e513-176">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="9e513-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e513-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9e513-178">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="9e513-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9e513-179">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="9e513-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9e513-180">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e513-180">-Confirm</span></span>
<span data-ttu-id="9e513-181">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e513-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e513-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e513-182">-WhatIf</span></span>
<span data-ttu-id="9e513-183">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e513-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e513-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e513-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e513-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e513-185">CommonParameters</span></span>
<span data-ttu-id="9e513-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e513-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e513-187">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e513-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e513-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e513-188">INPUTS</span></span>

### <span data-ttu-id="9e513-189">System. String</span><span class="sxs-lookup"><span data-stu-id="9e513-189">System.String</span></span>

### <span data-ttu-id="9e513-190">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9e513-190">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="9e513-191">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9e513-191">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9e513-192">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e513-192">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e513-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e513-193">OUTPUTS</span></span>

### <span data-ttu-id="9e513-194">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9e513-194">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9e513-195">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e513-195">NOTES</span></span>

## <span data-ttu-id="9e513-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e513-196">RELATED LINKS</span></span>

[<span data-ttu-id="9e513-197">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9e513-197">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="9e513-198">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9e513-198">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="9e513-199">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9e513-199">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
