---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
ms.openlocfilehash: c945838d7d237fb37610d3763525b0ecac838fbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491732"
---
# <span data-ttu-id="84f7f-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="84f7f-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="84f7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="84f7f-103">Letölti a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="84f7f-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="84f7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84f7f-104">SYNTAX</span></span>

### <span data-ttu-id="84f7f-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84f7f-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7f-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="84f7f-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7f-107">Directory</span><span class="sxs-lookup"><span data-stu-id="84f7f-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7f-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="84f7f-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84f7f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="84f7f-109">DESCRIPTION</span></span>
<span data-ttu-id="84f7f-110">A **Get-AzureStorageFileContent** parancsmag letölti a fájl tartalmát, majd a megadott célhelyre menti.</span><span class="sxs-lookup"><span data-stu-id="84f7f-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="84f7f-111">Ez a parancsmag nem adja vissza a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="84f7f-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="84f7f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="84f7f-112">EXAMPLES</span></span>

### <span data-ttu-id="84f7f-113">Példa 1: fájl letöltése mappából</span><span class="sxs-lookup"><span data-stu-id="84f7f-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="84f7f-114">Ez a parancs letölti a CurrentDataFile nevű fájlt a ContosoWorkingFolder mappából a fájl megosztása ContosoShare06 az aktuális mappába.</span><span class="sxs-lookup"><span data-stu-id="84f7f-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

## <span data-ttu-id="84f7f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84f7f-115">PARAMETERS</span></span>

### <span data-ttu-id="84f7f-116">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="84f7f-116">-CheckMd5</span></span>
<span data-ttu-id="84f7f-117">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-117">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-118">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-118">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-119">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-119">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-120">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-120">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="84f7f-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="84f7f-122">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-122">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-123">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-123">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-124">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-124">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-125">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-125">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="84f7f-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="84f7f-127">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-127">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-128">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-128">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-129">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-129">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-130">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-130">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-131">-Környezet</span><span class="sxs-lookup"><span data-stu-id="84f7f-131">-Context</span></span>
<span data-ttu-id="84f7f-132">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-132">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-133">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-133">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-134">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-134">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-135">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-135">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-136">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="84f7f-136">-Destination</span></span>
<span data-ttu-id="84f7f-137">A cél elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-137">Specifies the destination path.</span></span>
<span data-ttu-id="84f7f-138">Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="84f7f-138">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="84f7f-139">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-139">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-140">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-140">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-141">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-141">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-142">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-142">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-143">-Címtár</span><span class="sxs-lookup"><span data-stu-id="84f7f-143">-Directory</span></span>
<span data-ttu-id="84f7f-144">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="84f7f-144">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="84f7f-145">Ez a parancsmag egy fájl tartalmát a paraméter által megadott mappában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-145">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="84f7f-146">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="84f7f-146">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="84f7f-147">A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="84f7f-147">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="84f7f-148">-Fájl</span><span class="sxs-lookup"><span data-stu-id="84f7f-148">-File</span></span>
<span data-ttu-id="84f7f-149">A fájlt **CloudFile** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-149">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="84f7f-150">Ez a parancsmag a paraméter által megadott fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-150">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="84f7f-151">**CloudFile** objektum beolvasásához használja az Get-AzureStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="84f7f-151">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="84f7f-152">-Force</span><span class="sxs-lookup"><span data-stu-id="84f7f-152">-Force</span></span>
<span data-ttu-id="84f7f-153">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-153">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-154">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-154">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-155">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-155">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-156">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-156">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-157">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84f7f-157">-PassThru</span></span>
<span data-ttu-id="84f7f-158">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-158">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-159">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-159">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-160">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-160">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-161">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-161">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-162">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="84f7f-162">-Path</span></span>
<span data-ttu-id="84f7f-163">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-163">Specifies the path of a file.</span></span>
<span data-ttu-id="84f7f-164">Ez a parancsmag a paraméter által megadott fájl tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="84f7f-165">Ha a fájl nem létezik, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="84f7f-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="84f7f-166">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="84f7f-166">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="84f7f-167">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="84f7f-167">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="84f7f-168">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-168">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="84f7f-169">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="84f7f-169">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="84f7f-170">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="84f7f-170">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="84f7f-171">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="84f7f-171">-Share</span></span>
<span data-ttu-id="84f7f-172">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-172">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="84f7f-173">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-173">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="84f7f-174">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="84f7f-174">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="84f7f-175">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="84f7f-175">This object contains the storage context.</span></span>
<span data-ttu-id="84f7f-176">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="84f7f-176">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="84f7f-177">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="84f7f-177">-ShareName</span></span>
<span data-ttu-id="84f7f-178">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="84f7f-178">Specifies the name of the file share.</span></span>
<span data-ttu-id="84f7f-179">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="84f7f-179">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="84f7f-180">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="84f7f-180">-Confirm</span></span>
<span data-ttu-id="84f7f-181">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84f7f-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84f7f-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84f7f-182">-WhatIf</span></span>
<span data-ttu-id="84f7f-183">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="84f7f-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84f7f-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84f7f-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84f7f-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f7f-185">CommonParameters</span></span>
<span data-ttu-id="84f7f-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84f7f-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f7f-187">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f7f-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f7f-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84f7f-188">INPUTS</span></span>

## <span data-ttu-id="84f7f-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84f7f-189">OUTPUTS</span></span>

## <span data-ttu-id="84f7f-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84f7f-190">NOTES</span></span>

## <span data-ttu-id="84f7f-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84f7f-191">RELATED LINKS</span></span>

[<span data-ttu-id="84f7f-192">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="84f7f-192">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="84f7f-193">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="84f7f-193">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


