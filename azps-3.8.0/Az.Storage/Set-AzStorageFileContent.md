---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: c495403c0705c256e6de7173c12f2e16e97c3303
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014454"
---
# <span data-ttu-id="b0b64-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b0b64-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="b0b64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0b64-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b64-103">Feltölti a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="b0b64-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="b0b64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0b64-104">SYNTAX</span></span>

### <span data-ttu-id="b0b64-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0b64-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="b0b64-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="b0b64-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="b0b64-107">Directory</span><span class="sxs-lookup"><span data-stu-id="b0b64-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="b0b64-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0b64-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b64-109">A **set-AzStorageFileContent** parancsmag a fájl tartalmát egy megadott megosztásban lévő fájlba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="b0b64-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="b0b64-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b0b64-110">EXAMPLES</span></span>

### <span data-ttu-id="b0b64-111">1. példa: fájl feltöltése az aktuális mappában</span><span class="sxs-lookup"><span data-stu-id="b0b64-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="b0b64-112">A parancs feltölti a DataFile37 nevű fájlt az aktuális mappában egy CurrentDataFile nevű fájlként a ContosoWorkingFolder nevű mappában.</span><span class="sxs-lookup"><span data-stu-id="b0b64-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="b0b64-113">2. példa: az aktuális mappa összes fájljának feltöltése</span><span class="sxs-lookup"><span data-stu-id="b0b64-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="b0b64-114">Ez a példa számos gyakori Windows PowerShell-parancsmagot és a jelenlegi parancsmagot használ, így az aktuális mappából az összes fájlt feltöltheti a tároló ContosoShare06 gyökérkönyvtárába.</span><span class="sxs-lookup"><span data-stu-id="b0b64-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="b0b64-115">Az első parancs megkapja az aktuális mappa nevét, és a $CurrentFolder változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b0b64-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="b0b64-116">A második parancs a **Get-AzStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beszerzéséhez, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b0b64-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b0b64-117">A végleges parancs beolvassa az aktuális mappa tartalmát, és átadja őket az Where-Object parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="b0b64-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0b64-118">Ez a parancsmag kiszűri a fájlokat nem tartalmazó objektumokat, majd átadja a fájlokat az ForEach-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b0b64-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="b0b64-119">A parancsmag minden olyan fájlhoz parancsfájl-zárolást futtat, amely a megfelelő elérési utat hozza létre, majd az aktuális parancsmagot használja a fájl feltöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="b0b64-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="b0b64-120">Az eredmény ugyanazt a nevet és relatív pozíciót veszi figyelembe az egyéb, a példa által feltöltött fájlokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="b0b64-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="b0b64-121">A parancsfájl-blokkokról a következő témakörben olvashat bővebben: `Get-Help about_Script_Blocks`</span><span class="sxs-lookup"><span data-stu-id="b0b64-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="b0b64-122">3. példa: helyi fájl feltöltése Azure-fájlba, és a helyi fájl SMB-perserve (fájl Attributtes, a fájlok létrehozásának ideje, a fájl utolsó írási ideje) az Azure-fájlban.</span><span class="sxs-lookup"><span data-stu-id="b0b64-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="b0b64-123">Ez a példa feltölt egy helyi fájlt egy Azure-fájlba, és perserves a helyi fájl SMB-tulajdonságait (fájl Attributtes, a fájlok létrehozásának időpontját, a fájl utolsó írási időpontját) az Azure-fájlban.</span><span class="sxs-lookup"><span data-stu-id="b0b64-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="b0b64-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0b64-124">PARAMETERS</span></span>

### <span data-ttu-id="b0b64-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b64-125">-AsJob</span></span>
<span data-ttu-id="b0b64-126">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="b0b64-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b0b64-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0b64-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b0b64-128">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="b0b64-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b0b64-129">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="b0b64-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b0b64-130">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b0b64-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b0b64-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b0b64-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b0b64-132">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b0b64-133">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="b0b64-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b0b64-134">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="b0b64-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b0b64-135">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="b0b64-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b0b64-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b0b64-136">The default value is 10.</span></span>

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

### <span data-ttu-id="b0b64-137">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b0b64-137">-Context</span></span>
<span data-ttu-id="b0b64-138">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b0b64-139">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b0b64-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b0b64-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b64-140">-DefaultProfile</span></span>
<span data-ttu-id="b0b64-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0b64-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b64-142">-Címtár</span><span class="sxs-lookup"><span data-stu-id="b0b64-142">-Directory</span></span>
<span data-ttu-id="b0b64-143">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="b0b64-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b0b64-144">Ez a parancsmag feltölti a fájlt a paraméter által megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="b0b64-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="b0b64-145">Címtár beolvasásához használja az New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b0b64-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b0b64-146">A címtár eléréséhez használhatja az Get-AzStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="b0b64-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b64-147">-Force</span><span class="sxs-lookup"><span data-stu-id="b0b64-147">-Force</span></span>
<span data-ttu-id="b0b64-148">Jelzi, hogy ez a parancsmag felülír egy meglévő Azure-tárterületet.</span><span class="sxs-lookup"><span data-stu-id="b0b64-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="b0b64-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0b64-149">-PassThru</span></span>
<span data-ttu-id="b0b64-150">Azt jelzi, hogy ez a parancsmag az általa létrehozott vagy feltöltött **AzureStorageFile** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b0b64-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="b0b64-151">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b0b64-151">-Path</span></span>
<span data-ttu-id="b0b64-152">A fájl vagy mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="b0b64-153">Ezzel a parancsmaggal a program feltölti a tartalmat a paraméter által megadott fájlba vagy a paraméter által megadott mappában lévő fájlba.</span><span class="sxs-lookup"><span data-stu-id="b0b64-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="b0b64-154">Ha megad egy mappát, a parancsmag a forrásfájl nevével megegyező nevű fájlt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b0b64-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="b0b64-155">Ha olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat.</span><span class="sxs-lookup"><span data-stu-id="b0b64-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="b0b64-156">Ha olyan fájlt ad meg, amely már létezik, és az _erő_ paramétert adja meg, ez a parancsmag felülírja a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="b0b64-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="b0b64-157">Ha olyan fájlt ad meg, amely már létezik, és nem adja meg az _erő_ lehetőséget, ez a parancsmag nem változtatja meg, és hibát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="b0b64-157">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="b0b64-158">Ha olyan mappa elérési útját adja meg, amely nem létezik, akkor ez a parancsmag nem változtatja meg a hibát, és hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b0b64-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="b0b64-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="b0b64-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="b0b64-160">Tartsa meg a forrásfájl SMB-tulajdonságait (fájl-és Attributtes, fájl-létrehozási idő, fájl utolsó írási ideje) a célfájlba.</span><span class="sxs-lookup"><span data-stu-id="b0b64-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="b0b64-161">Ez a paraméter csak Windowson érhető el.</span><span class="sxs-lookup"><span data-stu-id="b0b64-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="b0b64-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0b64-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b0b64-163">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b0b64-164">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="b0b64-164">-Share</span></span>
<span data-ttu-id="b0b64-165">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b0b64-166">Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="b0b64-167">**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b0b64-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="b0b64-168">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b0b64-168">This object contains the storage context.</span></span>
<span data-ttu-id="b0b64-169">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b0b64-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b64-170">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="b0b64-170">-ShareName</span></span>
<span data-ttu-id="b0b64-171">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="b0b64-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="b0b64-172">Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="b0b64-173">-Forrás</span><span class="sxs-lookup"><span data-stu-id="b0b64-173">-Source</span></span>
<span data-ttu-id="b0b64-174">A parancsmag által feltöltött forrásfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b64-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="b0b64-175">Ha olyan fájlt ad meg, amely nem létezik, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b0b64-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b64-176">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0b64-176">-Confirm</span></span>
<span data-ttu-id="b0b64-177">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0b64-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b64-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b64-178">-WhatIf</span></span>
<span data-ttu-id="b0b64-179">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0b64-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b64-180">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0b64-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b64-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b64-181">CommonParameters</span></span>
<span data-ttu-id="b0b64-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0b64-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b64-183">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b64-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b64-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0b64-184">INPUTS</span></span>

### <span data-ttu-id="b0b64-185">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b0b64-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b0b64-186">Microsoft. Azure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b0b64-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="b0b64-187">System. String</span><span class="sxs-lookup"><span data-stu-id="b0b64-187">System.String</span></span>

### <span data-ttu-id="b0b64-188">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0b64-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0b64-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0b64-189">OUTPUTS</span></span>

### <span data-ttu-id="b0b64-190">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="b0b64-190">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="b0b64-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0b64-191">NOTES</span></span>

## <span data-ttu-id="b0b64-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0b64-192">RELATED LINKS</span></span>

[<span data-ttu-id="b0b64-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b0b64-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="b0b64-194">Új – AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b0b64-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="b0b64-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b0b64-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
