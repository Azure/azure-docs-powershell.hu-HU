---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 388adccb9578c695055815ab6e6de5478958621f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150387"
---
# <span data-ttu-id="d07bc-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d07bc-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="d07bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d07bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d07bc-103">Feltölt egy helyi fájlt egy Azure Storage blobba.</span><span class="sxs-lookup"><span data-stu-id="d07bc-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="d07bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d07bc-104">SYNTAX</span></span>

### <span data-ttu-id="d07bc-105">SendManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d07bc-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d07bc-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="d07bc-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d07bc-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="d07bc-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d07bc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d07bc-108">DESCRIPTION</span></span>
<span data-ttu-id="d07bc-109">A **Set-AzStorageBlobContent** parancsmag feltölt egy helyi fájlt egy Azure Storage-blobba.</span><span class="sxs-lookup"><span data-stu-id="d07bc-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="d07bc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d07bc-110">EXAMPLES</span></span>

### <span data-ttu-id="d07bc-111">1. példa: Elnevezett fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="d07bc-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="d07bc-112">Ez a parancs feltölti a PlanningData nevű fájlt egy Planning2015 nevű blobba.</span><span class="sxs-lookup"><span data-stu-id="d07bc-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="d07bc-113">2. példa: Az aktuális mappa alatti összes fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="d07bc-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="d07bc-114">Ez a parancs a Windows PowerShell alapparancsmagját Get-ChildItem az aktuális mappában és almappákban lévő összes fájl beszerzéhez, majd a folyamat műveleti operátorával átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d07bc-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d07bc-115">A **Set-AzStorageBlobContent** parancsmag feltölti a fájlokat a ContosoUploads nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="d07bc-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="d07bc-116">3. példa: Meglévő blob felülírása</span><span class="sxs-lookup"><span data-stu-id="d07bc-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="d07bc-117">Ez a parancs a Get-AzStorageBlob parancsmag használatával megkapja a Planning2015 nevű blobot a ContosoUploads tárolóban, majd átadja a blobot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d07bc-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="d07bc-118">A parancs feltölti a ContosoPlanning nevű fájlt Tervezés2015-ként.</span><span class="sxs-lookup"><span data-stu-id="d07bc-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="d07bc-119">Ez a parancs nem adja meg a *Force paramétert.*</span><span class="sxs-lookup"><span data-stu-id="d07bc-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="d07bc-120">A parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d07bc-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="d07bc-121">Ha megerősíti a parancsot, a parancsmag felülírja a meglévő blobot.</span><span class="sxs-lookup"><span data-stu-id="d07bc-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="d07bc-122">4. példa: Fájl feltöltése egy tárolóba a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="d07bc-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="d07bc-123">Ez a parancs a ContosoUpload karakterláncot tartalmazó tárolót a **Get-AzStorageContainer** parancsmaggal kezdi el használni, majd átadja a blobot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d07bc-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="d07bc-124">A parancs feltölti a ContosoPlanning nevű fájlt Tervezés2015-ként.</span><span class="sxs-lookup"><span data-stu-id="d07bc-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="d07bc-125">5. példa: Fájl feltöltése lap blobba metaadatokkal és PremiumPageBlobTier mint P10</span><span class="sxs-lookup"><span data-stu-id="d07bc-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="d07bc-126">Az első parancs létrehoz egy kivonattáblát, amely egy blob metaadatait tartalmazza, és amely a kivonattáblát tárolja a $Metadata változóban.</span><span class="sxs-lookup"><span data-stu-id="d07bc-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="d07bc-127">A második parancs feltölti a ContosoPlanning nevű fájlt a ContosoUploads nevű tárolóba.</span><span class="sxs-lookup"><span data-stu-id="d07bc-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="d07bc-128">A blob tartalmazza a $Metadata, és P10-ként tartalmazza a PremiumPageBlobTier metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="d07bc-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="d07bc-129">6. példa: Fájl feltöltése blobba megadott blobtulajdonságokkal, és a StandardBlobTier beállítása nagyszerűként</span><span class="sxs-lookup"><span data-stu-id="d07bc-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="d07bc-130">Ez a parancs feltölti az l fájlt c:\temp\index.htma contosouploads nevű tárolóba megadott blobtulajdonságokkal, és a StandardBlobTier értéket Cool értékként adja meg.</span><span class="sxs-lookup"><span data-stu-id="d07bc-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="d07bc-131">Ez a parancs a [System.Web.MimeMapping]::GetMimeMapping() API által a ContentType-érték blobtulajdonságokra van beállítva.</span><span class="sxs-lookup"><span data-stu-id="d07bc-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="d07bc-132">7. példa: Fájl feltöltése titkosítási hatókörű blobba</span><span class="sxs-lookup"><span data-stu-id="d07bc-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="d07bc-133">Ez a parancs egy titkosítási hatókörű blobba tölti fel a fájlt.</span><span class="sxs-lookup"><span data-stu-id="d07bc-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="d07bc-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d07bc-134">PARAMETERS</span></span>

### <span data-ttu-id="d07bc-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d07bc-135">-AsJob</span></span>
<span data-ttu-id="d07bc-136">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="d07bc-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d07bc-137">-Blob</span><span class="sxs-lookup"><span data-stu-id="d07bc-137">-Blob</span></span>
<span data-ttu-id="d07bc-138">Egy blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d07bc-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="d07bc-139">Ez a parancsmag feltölt egy fájlt az Azure Storage blobba, amit ez a paraméter megad.</span><span class="sxs-lookup"><span data-stu-id="d07bc-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="d07bc-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="d07bc-140">-BlobType</span></span>
<span data-ttu-id="d07bc-141">A parancsmag által feltöltött blob típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d07bc-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="d07bc-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="d07bc-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d07bc-143">Blokkolás</span><span class="sxs-lookup"><span data-stu-id="d07bc-143">Block</span></span>
- <span data-ttu-id="d07bc-144">Page</span><span class="sxs-lookup"><span data-stu-id="d07bc-144">Page</span></span>
- <span data-ttu-id="d07bc-145">Hozzáfűzés: Az alapértelmezett érték a Blokk.</span><span class="sxs-lookup"><span data-stu-id="d07bc-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="d07bc-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d07bc-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d07bc-147">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="d07bc-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d07bc-148">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="d07bc-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d07bc-149">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d07bc-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d07bc-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d07bc-150">-CloudBlob</span></span>
<span data-ttu-id="d07bc-151">Egy **CloudBlob-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="d07bc-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="d07bc-152">**CloudBlob-objektum** beszerzéséhez használja a Get-AzStorageBlob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d07bc-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="d07bc-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d07bc-153">-CloudBlobContainer</span></span>
<span data-ttu-id="d07bc-154">Egy **CloudBlobContainer-objektumot** ad meg az Azure Storage Client tárból.</span><span class="sxs-lookup"><span data-stu-id="d07bc-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="d07bc-155">Ez a parancsmag feltölti a tartalmat egy blobba a paraméter által megadott tárolóban.</span><span class="sxs-lookup"><span data-stu-id="d07bc-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="d07bc-156">**CloudBlobContainer-objektum** beszerzéséhez használja a Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d07bc-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="d07bc-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d07bc-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d07bc-158">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="d07bc-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d07bc-159">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d07bc-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d07bc-160">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="d07bc-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d07bc-161">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="d07bc-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d07bc-162">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="d07bc-162">The default value is 10.</span></span>

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

### <span data-ttu-id="d07bc-163">-Container</span><span class="sxs-lookup"><span data-stu-id="d07bc-163">-Container</span></span>
<span data-ttu-id="d07bc-164">Egy tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d07bc-164">Specifies the name of a container.</span></span>
<span data-ttu-id="d07bc-165">Ez a parancsmag feltölt egy fájlt egy blobba a paraméter által megadott tárolóban.</span><span class="sxs-lookup"><span data-stu-id="d07bc-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="d07bc-166">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d07bc-166">-Context</span></span>
<span data-ttu-id="d07bc-167">Egy Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d07bc-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d07bc-168">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d07bc-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="d07bc-169">Ha olvasási engedély nélkül szeretne használni egy SAS-jogkivonatból létrehozott tárterületkörnyezetet, hozzá kell adni a -Force paramétert a blob meglétének ellenőrzésének kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d07bc-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="d07bc-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07bc-170">-DefaultProfile</span></span>
<span data-ttu-id="d07bc-171">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d07bc-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d07bc-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="d07bc-172">-EncryptionScope</span></span>
<span data-ttu-id="d07bc-173">A blobra vonatkozó kérések során használt titkosítási hatókör.</span><span class="sxs-lookup"><span data-stu-id="d07bc-173">Encryption scope to be used when making requests to the blob.</span></span>

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

### <span data-ttu-id="d07bc-174">-File</span><span class="sxs-lookup"><span data-stu-id="d07bc-174">-File</span></span>
<span data-ttu-id="d07bc-175">Megadja a blobtartalomként feltölthet fájlok helyi elérési útját.</span><span class="sxs-lookup"><span data-stu-id="d07bc-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="d07bc-176">-Force</span><span class="sxs-lookup"><span data-stu-id="d07bc-176">-Force</span></span>
<span data-ttu-id="d07bc-177">Azt jelzi, hogy ez a parancsmag felülír egy meglévő blobot anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d07bc-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d07bc-178">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d07bc-178">-Metadata</span></span>
<span data-ttu-id="d07bc-179">A feltöltött blob metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d07bc-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="d07bc-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="d07bc-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="d07bc-181">Lap blobrétege</span><span class="sxs-lookup"><span data-stu-id="d07bc-181">Page Blob Tier</span></span>

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

### <span data-ttu-id="d07bc-182">-Properties</span><span class="sxs-lookup"><span data-stu-id="d07bc-182">-Properties</span></span>
<span data-ttu-id="d07bc-183">Megadja a feltöltött blob tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d07bc-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="d07bc-184">A támogatott tulajdonságok: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="d07bc-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="d07bc-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d07bc-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d07bc-186">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="d07bc-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d07bc-187">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d07bc-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d07bc-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="d07bc-188">-StandardBlobTier</span></span>
<span data-ttu-id="d07bc-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="d07bc-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="d07bc-190">Részleteket itt láthat: https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="d07bc-190">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="d07bc-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d07bc-191">-Confirm</span></span>
<span data-ttu-id="d07bc-192">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d07bc-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d07bc-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07bc-193">-WhatIf</span></span>
<span data-ttu-id="d07bc-194">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d07bc-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07bc-195">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d07bc-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d07bc-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07bc-196">CommonParameters</span></span>
<span data-ttu-id="d07bc-197">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d07bc-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07bc-198">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07bc-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07bc-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d07bc-199">INPUTS</span></span>

### <span data-ttu-id="d07bc-200">System.String</span><span class="sxs-lookup"><span data-stu-id="d07bc-200">System.String</span></span>

### <span data-ttu-id="d07bc-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d07bc-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="d07bc-202">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d07bc-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="d07bc-203">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d07bc-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d07bc-204">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07bc-204">OUTPUTS</span></span>

### <span data-ttu-id="d07bc-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d07bc-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="d07bc-206">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d07bc-206">NOTES</span></span>

## <span data-ttu-id="d07bc-207">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d07bc-207">RELATED LINKS</span></span>

[<span data-ttu-id="d07bc-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d07bc-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="d07bc-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d07bc-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="d07bc-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d07bc-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
