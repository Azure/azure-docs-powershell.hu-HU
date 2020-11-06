---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 1dc1e95e2ecf085faad664f624e7595acd9ab607
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496776"
---
# <span data-ttu-id="b13df-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b13df-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="b13df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b13df-102">SYNOPSIS</span></span>
<span data-ttu-id="b13df-103">Letölti a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="b13df-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b13df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b13df-104">SYNTAX</span></span>

### <span data-ttu-id="b13df-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b13df-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13df-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="b13df-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13df-107">Directory</span><span class="sxs-lookup"><span data-stu-id="b13df-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13df-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="b13df-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13df-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b13df-109">DESCRIPTION</span></span>
<span data-ttu-id="b13df-110">A **Get-AzureStorageFileContent** parancsmag letölti a fájl tartalmát, majd a megadott célhelyre menti.</span><span class="sxs-lookup"><span data-stu-id="b13df-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="b13df-111">Ez a parancsmag nem adja vissza a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="b13df-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="b13df-112">Példák</span><span class="sxs-lookup"><span data-stu-id="b13df-112">EXAMPLES</span></span>

### <span data-ttu-id="b13df-113">Példa 1: fájl letöltése mappából</span><span class="sxs-lookup"><span data-stu-id="b13df-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="b13df-114">Ez a parancs letölti a CurrentDataFile nevű fájlt a ContosoWorkingFolder mappából a fájl megosztása ContosoShare06 az aktuális mappába.</span><span class="sxs-lookup"><span data-stu-id="b13df-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="b13df-115">2. példa: a fájlok letöltése a minta fájlmegosztás csoportban</span><span class="sxs-lookup"><span data-stu-id="b13df-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="b13df-116">Ez a példa a minta fájlmegosztás alatti fájlokat tölti le</span><span class="sxs-lookup"><span data-stu-id="b13df-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="b13df-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b13df-117">PARAMETERS</span></span>

### <span data-ttu-id="b13df-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="b13df-118">-CheckMd5</span></span>
<span data-ttu-id="b13df-119">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-120">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-121">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-122">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b13df-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b13df-124">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-125">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-126">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-127">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b13df-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b13df-129">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-130">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-131">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-132">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-133">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b13df-133">-Context</span></span>
<span data-ttu-id="b13df-134">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-135">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-136">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-137">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-138">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="b13df-138">-Destination</span></span>
<span data-ttu-id="b13df-139">A cél elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-139">Specifies the destination path.</span></span>
<span data-ttu-id="b13df-140">Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="b13df-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="b13df-141">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-142">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-143">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-144">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-145">-Címtár</span><span class="sxs-lookup"><span data-stu-id="b13df-145">-Directory</span></span>
<span data-ttu-id="b13df-146">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="b13df-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b13df-147">Ez a parancsmag egy fájl tartalmát a paraméter által megadott mappában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="b13df-148">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b13df-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b13df-149">A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="b13df-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-150">-Fájl</span><span class="sxs-lookup"><span data-stu-id="b13df-150">-File</span></span>
<span data-ttu-id="b13df-151">A fájlt **CloudFile** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="b13df-152">Ez a parancsmag a paraméter által megadott fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="b13df-153">**CloudFile** objektum beolvasásához használja az Get-AzureStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b13df-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-154">-Force</span><span class="sxs-lookup"><span data-stu-id="b13df-154">-Force</span></span>
<span data-ttu-id="b13df-155">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-156">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-157">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-158">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b13df-159">-PassThru</span></span>
<span data-ttu-id="b13df-160">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-161">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-162">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-163">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-164">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b13df-164">-Path</span></span>
<span data-ttu-id="b13df-165">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-165">Specifies the path of a file.</span></span>
<span data-ttu-id="b13df-166">Ez a parancsmag a paraméter által megadott fájl tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="b13df-167">Ha a fájl nem létezik, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b13df-167">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b13df-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b13df-169">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="b13df-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="b13df-170">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="b13df-171">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="b13df-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="b13df-172">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="b13df-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-173">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="b13df-173">-Share</span></span>
<span data-ttu-id="b13df-174">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b13df-175">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="b13df-176">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b13df-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="b13df-177">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b13df-177">This object contains the storage context.</span></span>
<span data-ttu-id="b13df-178">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b13df-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-179">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="b13df-179">-ShareName</span></span>
<span data-ttu-id="b13df-180">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="b13df-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="b13df-181">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="b13df-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-182">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b13df-182">-Confirm</span></span>
<span data-ttu-id="b13df-183">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b13df-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13df-184">-WhatIf</span></span>
<span data-ttu-id="b13df-185">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b13df-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13df-186">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b13df-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13df-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13df-187">CommonParameters</span></span>
<span data-ttu-id="b13df-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b13df-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13df-189">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13df-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13df-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b13df-190">INPUTS</span></span>

### <span data-ttu-id="b13df-191">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b13df-191">IStorageContext</span></span>

<span data-ttu-id="b13df-192">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b13df-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b13df-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b13df-193">CloudFileDirectory</span></span>

<span data-ttu-id="b13df-194">A "címtár" paraméter elfogadja a "CloudFileDirectory" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b13df-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="b13df-195">CloudFile</span><span class="sxs-lookup"><span data-stu-id="b13df-195">CloudFile</span></span>

<span data-ttu-id="b13df-196">A "fájl" paraméter elfogadja a "CloudFile" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b13df-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="b13df-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b13df-197">CloudFileShare</span></span>

<span data-ttu-id="b13df-198">A "share" paraméter értéke "CloudFileShare" típusú értéket ad a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b13df-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="b13df-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b13df-199">OUTPUTS</span></span>

## <span data-ttu-id="b13df-200">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b13df-200">NOTES</span></span>

## <span data-ttu-id="b13df-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b13df-201">RELATED LINKS</span></span>

[<span data-ttu-id="b13df-202">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b13df-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="b13df-203">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b13df-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


