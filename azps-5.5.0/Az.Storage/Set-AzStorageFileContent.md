---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207751"
---
# <span data-ttu-id="c275c-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c275c-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="c275c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c275c-102">SYNOPSIS</span></span>
<span data-ttu-id="c275c-103">Feltölti egy fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="c275c-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="c275c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c275c-104">SYNTAX</span></span>

### <span data-ttu-id="c275c-105">ShareName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c275c-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="c275c-106">Megosztás</span><span class="sxs-lookup"><span data-stu-id="c275c-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="c275c-107">Címtár</span><span class="sxs-lookup"><span data-stu-id="c275c-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="c275c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c275c-108">DESCRIPTION</span></span>
<span data-ttu-id="c275c-109">A **Set-AzStorageFileContent** parancsmag egy adott megosztáson található fájlba tölti fel a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="c275c-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="c275c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c275c-110">EXAMPLES</span></span>

### <span data-ttu-id="c275c-111">1. példa: Fájl feltöltése az aktuális mappába</span><span class="sxs-lookup"><span data-stu-id="c275c-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="c275c-112">Ez a parancs egy DataFile37 nevű fájlt tölt fel az aktuális mappába CurrentDataFile néven a ContosoWorkingFolder mappában.</span><span class="sxs-lookup"><span data-stu-id="c275c-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="c275c-113">2. példa: Az aktuális mappa összes fájljának feltöltése</span><span class="sxs-lookup"><span data-stu-id="c275c-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="c275c-114">Ez a példa számos gyakori Windows PowerShell-parancsmagot és az aktuális parancsmagot használva tölti fel az aktuális mappában lévő összes fájlt a ContosoShare06 tároló gyökérmappába.</span><span class="sxs-lookup"><span data-stu-id="c275c-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="c275c-115">Az első parancs az aktuális mappa nevét kapja meg, és a $CurrentFolder tárolja.</span><span class="sxs-lookup"><span data-stu-id="c275c-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="c275c-116">A második parancs **a Get-AzStorageShare** parancsmagot használva szerezze be a ContosoShare06 nevű fájlmegosztást, majd tárolja azt a $Container változóban.</span><span class="sxs-lookup"><span data-stu-id="c275c-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c275c-117">Az utolsó parancs az aktuális mappa tartalmát kapja meg, és a folyamat műveleti Where-Object átadja mindegyiket a Where-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c275c-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c275c-118">Ez a parancsmag kiszűri azokat az objektumokat, amelyek nem fájlok, majd átadja a fájlokat a ForEach-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c275c-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="c275c-119">Ez a parancsmag minden fájlhoz futtat egy parancsfájlblokkot, amely létrehozza a megfelelő elérési utat, majd az aktuális parancsmag használatával tölti fel a fájlt.</span><span class="sxs-lookup"><span data-stu-id="c275c-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="c275c-120">Az eredménynek ugyanaz a neve és relatív pozíciója, mint az ebben a példában feltöltött többi fájl esetében.</span><span class="sxs-lookup"><span data-stu-id="c275c-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="c275c-121">A parancsfájlblokkokkal kapcsolatos további információkért írja be a `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="c275c-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="c275c-122">3. példa: Töltsön fel egy helyi fájlt egy Azure-fájlba, és tartsa meg a helyi SMB-tulajdonságokat (Fájl-hozzárendelések, Fájl létrehozási idő, Fájl legutóbbi írási ideje) az Azure-fájlban.</span><span class="sxs-lookup"><span data-stu-id="c275c-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="c275c-123">Ebben a példában egy helyi fájlt töltünk fel egy Azure-fájlba, és az Azure-fájl helyi SMB-tulajdonságait (Fájl-hozzárendelések, Fájlkészítési idő, Legutóbbi írási idő) is kiszolgaljuk.</span><span class="sxs-lookup"><span data-stu-id="c275c-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="c275c-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c275c-124">PARAMETERS</span></span>

### <span data-ttu-id="c275c-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c275c-125">-AsJob</span></span>
<span data-ttu-id="c275c-126">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="c275c-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c275c-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c275c-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c275c-128">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c275c-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c275c-129">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="c275c-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c275c-130">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c275c-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c275c-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c275c-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c275c-132">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="c275c-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c275c-133">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="c275c-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c275c-134">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="c275c-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c275c-135">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c275c-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c275c-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c275c-136">The default value is 10.</span></span>

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

### <span data-ttu-id="c275c-137">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c275c-137">-Context</span></span>
<span data-ttu-id="c275c-138">Egy Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c275c-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c275c-139">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="c275c-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c275c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c275c-140">-DefaultProfile</span></span>
<span data-ttu-id="c275c-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c275c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c275c-142">-Directory</span><span class="sxs-lookup"><span data-stu-id="c275c-142">-Directory</span></span>
<span data-ttu-id="c275c-143">Mappát ad meg **CloudFileDirectory objektumként.**</span><span class="sxs-lookup"><span data-stu-id="c275c-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c275c-144">Ez a parancsmag feltölti a fájlt a paraméter által megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="c275c-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="c275c-145">Címtár beszerzéséhez használja a New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c275c-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c275c-146">Címtár beszerzéséhez használhatja Get-AzStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="c275c-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="c275c-147">-Force</span><span class="sxs-lookup"><span data-stu-id="c275c-147">-Force</span></span>
<span data-ttu-id="c275c-148">Azt jelzi, hogy ez a parancsmag felülír egy meglévő Azure-tárfájlt.</span><span class="sxs-lookup"><span data-stu-id="c275c-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="c275c-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c275c-149">-PassThru</span></span>
<span data-ttu-id="c275c-150">Azt jelzi, hogy ez a parancsmag a létrehozott vagy feltöltött **AzureStorageFile** objektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c275c-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="c275c-151">-Path</span><span class="sxs-lookup"><span data-stu-id="c275c-151">-Path</span></span>
<span data-ttu-id="c275c-152">Egy fájl vagy mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c275c-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="c275c-153">Ez a parancsmag a tartalmat a paraméter által megadott fájlba vagy a paraméter által megadott mappában lévő fájlba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="c275c-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="c275c-154">Ha mappát ad meg, ez a parancsmag a forrásfájl nevével azonos nevű fájlt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c275c-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="c275c-155">Ha olyan fájl elérési útját adja meg, amely nem létezik, ez a parancsmag létrehozza a fájlt, és annak a fájlba menti a tartalmat.</span><span class="sxs-lookup"><span data-stu-id="c275c-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="c275c-156">Ha megad egy már létező fájlt, és megadja a _Force_ paramétert, ez a parancsmag felülírja a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="c275c-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="c275c-157">Ha olyan fájlt ad meg, amely már létezik, és nem adja meg az Kényszerítve _értéket,_ ez a parancsmag nem módosítja, és hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c275c-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="c275c-158">Ha olyan mappa elérési útját adja meg, amely nem létezik, ez a parancsmag nem módosítja, és hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c275c-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="c275c-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="c275c-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="c275c-160">A forrásfájl SMB-tulajdonságait (Fájl-hozzárendelések, Fájl létrehozási idő, Legutóbbi írási időpont) a célfájlban tartsa meg.</span><span class="sxs-lookup"><span data-stu-id="c275c-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="c275c-161">Ez a paraméter csak Windows rendszeren érhető el.</span><span class="sxs-lookup"><span data-stu-id="c275c-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="c275c-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c275c-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c275c-163">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c275c-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c275c-164">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="c275c-164">-Share</span></span>
<span data-ttu-id="c275c-165">Egy **CloudFileShare-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="c275c-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c275c-166">Ez a parancsmag feltölti a paraméter által megadott fájlba.</span><span class="sxs-lookup"><span data-stu-id="c275c-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="c275c-167">**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c275c-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="c275c-168">Ez az objektum tartalmazza a tárterület környezetét.</span><span class="sxs-lookup"><span data-stu-id="c275c-168">This object contains the storage context.</span></span>
<span data-ttu-id="c275c-169">Ha ezt a paramétert adja meg, ne adja meg a környezet *paramétert.*</span><span class="sxs-lookup"><span data-stu-id="c275c-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="c275c-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c275c-170">-ShareName</span></span>
<span data-ttu-id="c275c-171">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c275c-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="c275c-172">Ez a parancsmag feltölti a paraméter által megadott fájlba.</span><span class="sxs-lookup"><span data-stu-id="c275c-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="c275c-173">-Source</span><span class="sxs-lookup"><span data-stu-id="c275c-173">-Source</span></span>
<span data-ttu-id="c275c-174">A parancsmag által feltöltött forrásfájl.</span><span class="sxs-lookup"><span data-stu-id="c275c-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="c275c-175">Ha olyan fájlt ad meg, amely nem létezik, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c275c-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c275c-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c275c-176">-Confirm</span></span>
<span data-ttu-id="c275c-177">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c275c-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c275c-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c275c-178">-WhatIf</span></span>
<span data-ttu-id="c275c-179">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c275c-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c275c-180">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c275c-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c275c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c275c-181">CommonParameters</span></span>
<span data-ttu-id="c275c-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c275c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c275c-183">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c275c-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c275c-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c275c-184">INPUTS</span></span>

### <span data-ttu-id="c275c-185">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c275c-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="c275c-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c275c-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="c275c-187">System.String</span><span class="sxs-lookup"><span data-stu-id="c275c-187">System.String</span></span>

### <span data-ttu-id="c275c-188">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c275c-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c275c-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c275c-189">OUTPUTS</span></span>

### <span data-ttu-id="c275c-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c275c-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="c275c-191">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c275c-191">NOTES</span></span>

## <span data-ttu-id="c275c-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c275c-192">RELATED LINKS</span></span>

[<span data-ttu-id="c275c-193">Remove-AzstorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c275c-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="c275c-194">New-AzstorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c275c-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="c275c-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c275c-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
