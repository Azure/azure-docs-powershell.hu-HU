---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025890"
---
# <span data-ttu-id="51b8f-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="51b8f-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="51b8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="51b8f-103">Letölti a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="51b8f-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="51b8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51b8f-104">SYNTAX</span></span>

### <span data-ttu-id="51b8f-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51b8f-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="51b8f-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="51b8f-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="51b8f-107">Directory</span><span class="sxs-lookup"><span data-stu-id="51b8f-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="51b8f-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="51b8f-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="51b8f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="51b8f-109">DESCRIPTION</span></span>
<span data-ttu-id="51b8f-110">A **Get-AzStorageFileContent** parancsmag letölti a fájl tartalmát, majd a megadott célhelyre menti.</span><span class="sxs-lookup"><span data-stu-id="51b8f-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="51b8f-111">Ez a parancsmag nem adja vissza a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="51b8f-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="51b8f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="51b8f-112">EXAMPLES</span></span>

### <span data-ttu-id="51b8f-113">Példa 1: fájl letöltése mappából</span><span class="sxs-lookup"><span data-stu-id="51b8f-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="51b8f-114">Ez a parancs letölti a CurrentDataFile nevű fájlt a ContosoWorkingFolder mappából a fájl megosztása ContosoShare06 az aktuális mappába.</span><span class="sxs-lookup"><span data-stu-id="51b8f-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="51b8f-115">2. példa: a fájlok letöltése a minta fájlmegosztás csoportban</span><span class="sxs-lookup"><span data-stu-id="51b8f-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="51b8f-116">Ez a példa a minta fájlmegosztás alatti fájlokat tölti le</span><span class="sxs-lookup"><span data-stu-id="51b8f-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="51b8f-117">3. példa: töltse le az Azure-fájlt egy helyi fájlra, és perserve az Azure-fájl SMB-tulajdonságait (fájl Attributtes, a fájlok létrehozásának ideje, a fájl utolsó írási ideje) a helyi fájlban.</span><span class="sxs-lookup"><span data-stu-id="51b8f-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="51b8f-118">Ebben a példában az Azure-fájl egy helyi fájlra tölthető le, és az Azure-perserves (fájl-és Attributtes, fájl-létrehozási idő, fájl utolsó írási ideje) a helyi fájlban.</span><span class="sxs-lookup"><span data-stu-id="51b8f-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="51b8f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51b8f-119">PARAMETERS</span></span>

### <span data-ttu-id="51b8f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51b8f-120">-AsJob</span></span>
<span data-ttu-id="51b8f-121">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="51b8f-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="51b8f-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="51b8f-122">-CheckMd5</span></span>
<span data-ttu-id="51b8f-123">Itt adhatja meg, hogy a letöltött fájlhoz tartozó Md5-összeget szeretné-e ellenőrizni.</span><span class="sxs-lookup"><span data-stu-id="51b8f-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="51b8f-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51b8f-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="51b8f-125">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="51b8f-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="51b8f-126">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="51b8f-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="51b8f-127">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="51b8f-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="51b8f-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="51b8f-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="51b8f-129">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="51b8f-130">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="51b8f-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="51b8f-131">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="51b8f-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="51b8f-132">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="51b8f-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="51b8f-133">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="51b8f-133">The default value is 10.</span></span>

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

### <span data-ttu-id="51b8f-134">-Környezet</span><span class="sxs-lookup"><span data-stu-id="51b8f-134">-Context</span></span>
<span data-ttu-id="51b8f-135">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="51b8f-136">Környezet beolvasásához használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="51b8f-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51b8f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b8f-137">-DefaultProfile</span></span>
<span data-ttu-id="51b8f-138">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51b8f-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b8f-139">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="51b8f-139">-Destination</span></span>
<span data-ttu-id="51b8f-140">A cél elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-140">Specifies the destination path.</span></span>
<span data-ttu-id="51b8f-141">Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="51b8f-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="51b8f-142">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="51b8f-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51b8f-143">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="51b8f-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51b8f-144">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="51b8f-144">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="51b8f-145">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="51b8f-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b8f-146">-Címtár</span><span class="sxs-lookup"><span data-stu-id="51b8f-146">-Directory</span></span>
<span data-ttu-id="51b8f-147">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="51b8f-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="51b8f-148">Ez a parancsmag egy fájl tartalmát a paraméter által megadott mappában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="51b8f-149">Címtár beolvasásához használja az New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="51b8f-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="51b8f-150">A címtár eléréséhez használhatja az Get-AzStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="51b8f-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51b8f-151">-Fájl</span><span class="sxs-lookup"><span data-stu-id="51b8f-151">-File</span></span>
<span data-ttu-id="51b8f-152">A fájlt **CloudFile** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="51b8f-153">Ez a parancsmag a paraméter által megadott fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="51b8f-154">**CloudFile** objektum beolvasásához használja az Get-AzStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="51b8f-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51b8f-155">-Force</span><span class="sxs-lookup"><span data-stu-id="51b8f-155">-Force</span></span>
<span data-ttu-id="51b8f-156">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="51b8f-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="51b8f-157">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="51b8f-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="51b8f-158">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="51b8f-158">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="51b8f-159">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="51b8f-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="51b8f-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51b8f-160">-PassThru</span></span>
<span data-ttu-id="51b8f-161">Azt jelzi, hogy ez a parancsmag a letöltött **AzureStorageFile** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="51b8f-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="51b8f-162">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="51b8f-162">-Path</span></span>
<span data-ttu-id="51b8f-163">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-163">Specifies the path of a file.</span></span>
<span data-ttu-id="51b8f-164">Ez a parancsmag a paraméter által megadott fájl tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="51b8f-165">Ha a fájl nem létezik, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="51b8f-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b8f-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="51b8f-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="51b8f-167">Tartsa meg a forrásfájl SMB-tulajdonságait (fájl-és Attributtes, fájl-létrehozási idő, fájl utolsó írási ideje) a célfájlba.</span><span class="sxs-lookup"><span data-stu-id="51b8f-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="51b8f-168">Ez a paraméter csak Windowson érhető el.</span><span class="sxs-lookup"><span data-stu-id="51b8f-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="51b8f-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51b8f-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="51b8f-170">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="51b8f-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="51b8f-171">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="51b8f-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="51b8f-172">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="51b8f-172">-Share</span></span>
<span data-ttu-id="51b8f-173">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="51b8f-174">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="51b8f-175">**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="51b8f-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="51b8f-176">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="51b8f-176">This object contains the storage context.</span></span>
<span data-ttu-id="51b8f-177">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="51b8f-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51b8f-178">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="51b8f-178">-ShareName</span></span>
<span data-ttu-id="51b8f-179">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="51b8f-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="51b8f-180">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="51b8f-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b8f-181">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51b8f-181">-Confirm</span></span>
<span data-ttu-id="51b8f-182">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51b8f-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b8f-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b8f-183">-WhatIf</span></span>
<span data-ttu-id="51b8f-184">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51b8f-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b8f-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51b8f-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b8f-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b8f-186">CommonParameters</span></span>
<span data-ttu-id="51b8f-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51b8f-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b8f-188">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b8f-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b8f-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51b8f-189">INPUTS</span></span>

### <span data-ttu-id="51b8f-190">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="51b8f-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="51b8f-191">Microsoft. Azure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="51b8f-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="51b8f-192">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="51b8f-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="51b8f-193">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="51b8f-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="51b8f-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51b8f-194">OUTPUTS</span></span>

### <span data-ttu-id="51b8f-195">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="51b8f-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="51b8f-196">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51b8f-196">NOTES</span></span>

## <span data-ttu-id="51b8f-197">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51b8f-197">RELATED LINKS</span></span>

[<span data-ttu-id="51b8f-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="51b8f-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="51b8f-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="51b8f-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


