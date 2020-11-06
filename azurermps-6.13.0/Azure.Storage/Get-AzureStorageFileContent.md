---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 0641fdf635bce2bbb545e50ecc99a39329fabc9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495209"
---
# <span data-ttu-id="c39dc-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c39dc-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="c39dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c39dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c39dc-103">Letölti a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="c39dc-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c39dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c39dc-104">SYNTAX</span></span>

### <span data-ttu-id="c39dc-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c39dc-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39dc-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="c39dc-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c39dc-107">Directory</span><span class="sxs-lookup"><span data-stu-id="c39dc-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c39dc-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="c39dc-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c39dc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c39dc-109">DESCRIPTION</span></span>
<span data-ttu-id="c39dc-110">A **Get-AzureStorageFileContent** parancsmag letölti a fájl tartalmát, majd a megadott célhelyre menti.</span><span class="sxs-lookup"><span data-stu-id="c39dc-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="c39dc-111">Ez a parancsmag nem adja vissza a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="c39dc-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="c39dc-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c39dc-112">EXAMPLES</span></span>

### <span data-ttu-id="c39dc-113">Példa 1: fájl letöltése mappából</span><span class="sxs-lookup"><span data-stu-id="c39dc-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="c39dc-114">Ez a parancs letölti a CurrentDataFile nevű fájlt a ContosoWorkingFolder mappából a fájl megosztása ContosoShare06 az aktuális mappába.</span><span class="sxs-lookup"><span data-stu-id="c39dc-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="c39dc-115">2. példa: a fájlok letöltése a minta fájlmegosztás csoportban</span><span class="sxs-lookup"><span data-stu-id="c39dc-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="c39dc-116">Ez a példa a minta fájlmegosztás alatti fájlokat tölti le</span><span class="sxs-lookup"><span data-stu-id="c39dc-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="c39dc-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c39dc-117">PARAMETERS</span></span>

### <span data-ttu-id="c39dc-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="c39dc-118">-CheckMd5</span></span>
<span data-ttu-id="c39dc-119">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-120">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-121">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-122">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c39dc-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c39dc-124">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-125">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-126">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-127">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c39dc-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c39dc-129">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-130">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-131">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-132">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-133">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c39dc-133">-Context</span></span>
<span data-ttu-id="c39dc-134">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-135">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-136">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-137">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39dc-138">-DefaultProfile</span></span>
<span data-ttu-id="c39dc-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c39dc-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c39dc-140">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="c39dc-140">-Destination</span></span>
<span data-ttu-id="c39dc-141">A cél elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-141">Specifies the destination path.</span></span>
<span data-ttu-id="c39dc-142">Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="c39dc-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="c39dc-143">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-144">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-145">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-146">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-147">-Címtár</span><span class="sxs-lookup"><span data-stu-id="c39dc-147">-Directory</span></span>
<span data-ttu-id="c39dc-148">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="c39dc-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c39dc-149">Ez a parancsmag egy fájl tartalmát a paraméter által megadott mappában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="c39dc-150">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c39dc-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c39dc-151">A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="c39dc-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c39dc-152">-Fájl</span><span class="sxs-lookup"><span data-stu-id="c39dc-152">-File</span></span>
<span data-ttu-id="c39dc-153">A fájlt **CloudFile** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="c39dc-154">Ez a parancsmag a paraméter által megadott fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="c39dc-155">**CloudFile** objektum beolvasásához használja az Get-AzureStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c39dc-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c39dc-156">-Force</span><span class="sxs-lookup"><span data-stu-id="c39dc-156">-Force</span></span>
<span data-ttu-id="c39dc-157">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-158">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-159">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-160">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c39dc-161">-PassThru</span></span>
<span data-ttu-id="c39dc-162">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-163">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-164">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-165">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-166">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c39dc-166">-Path</span></span>
<span data-ttu-id="c39dc-167">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-167">Specifies the path of a file.</span></span>
<span data-ttu-id="c39dc-168">Ez a parancsmag a paraméter által megadott fájl tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="c39dc-169">Ha a fájl nem létezik, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="c39dc-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c39dc-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c39dc-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c39dc-171">Ha egy olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat az új fájlban.</span><span class="sxs-lookup"><span data-stu-id="c39dc-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c39dc-172">Ha olyan fájl elérési útját adja meg, amely már létezik, és az *erő* paramétert adja meg, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c39dc-173">Ha egy meglévő fájl elérési útját adja meg, és nem adja meg az *erő* beállítást, a parancsmag a folytatás előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="c39dc-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c39dc-174">Ha a mappa elérési útját adja meg, a parancsmag megkísérli létrehozni az Azure-tárterület nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c39dc-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c39dc-175">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="c39dc-175">-Share</span></span>
<span data-ttu-id="c39dc-176">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c39dc-177">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="c39dc-178">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c39dc-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="c39dc-179">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c39dc-179">This object contains the storage context.</span></span>
<span data-ttu-id="c39dc-180">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c39dc-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c39dc-181">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="c39dc-181">-ShareName</span></span>
<span data-ttu-id="c39dc-182">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="c39dc-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="c39dc-183">Ez a parancsmag a fájl tartalmának letöltését a megosztás ebben a paraméterben című részen adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39dc-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="c39dc-184">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c39dc-184">-Confirm</span></span>
<span data-ttu-id="c39dc-185">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c39dc-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c39dc-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39dc-186">-WhatIf</span></span>
<span data-ttu-id="c39dc-187">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c39dc-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39dc-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c39dc-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c39dc-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39dc-189">CommonParameters</span></span>
<span data-ttu-id="c39dc-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c39dc-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39dc-191">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c39dc-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39dc-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c39dc-192">INPUTS</span></span>

### <span data-ttu-id="c39dc-193">Microsoft. WindowsAzure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c39dc-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="c39dc-194">Paraméterek: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c39dc-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="c39dc-195">Microsoft. WindowsAzure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c39dc-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="c39dc-196">Paraméterek: címtár (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c39dc-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="c39dc-197">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="c39dc-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="c39dc-198">Paraméterek: fájl (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c39dc-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="c39dc-199">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c39dc-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c39dc-200">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c39dc-200">OUTPUTS</span></span>

### <span data-ttu-id="c39dc-201">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="c39dc-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="c39dc-202">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c39dc-202">NOTES</span></span>

## <span data-ttu-id="c39dc-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c39dc-203">RELATED LINKS</span></span>

[<span data-ttu-id="c39dc-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c39dc-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c39dc-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c39dc-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


