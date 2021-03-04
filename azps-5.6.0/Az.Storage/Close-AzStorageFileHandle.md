---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 71985cc978425c343e535e6455172f61e5397934
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937313"
---
# <span data-ttu-id="8032b-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8032b-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="8032b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8032b-102">SYNOPSIS</span></span>
<span data-ttu-id="8032b-103">Bezárja egy fájlmegosztás, egy fájlkönyvtár vagy egy fájl fogópontját.</span><span class="sxs-lookup"><span data-stu-id="8032b-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="8032b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8032b-104">SYNTAX</span></span>

### <span data-ttu-id="8032b-105">ShareNameCloseAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8032b-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8032b-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="8032b-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8032b-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="8032b-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8032b-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="8032b-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8032b-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="8032b-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8032b-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="8032b-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8032b-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8032b-111">DESCRIPTION</span></span>
<span data-ttu-id="8032b-112">Az **Close-AzStorageFileHandle** parancsmag bezárja egy fájlmegosztás, illetve fájlkönyvtár vagy fájl fogópontját.</span><span class="sxs-lookup"><span data-stu-id="8032b-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="8032b-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8032b-113">EXAMPLES</span></span>

### <span data-ttu-id="8032b-114">1. példa: Felsorolja az aktuális tárfiók összes fájlmegosztását, és rekurzív módon zárja be a fájlmegosztások összes fájlfogópontját.</span><span class="sxs-lookup"><span data-stu-id="8032b-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="8032b-115">Ez a parancs felsorolja az aktuális tárfiók összes fájlmegosztását, és rekurzív módon zárja be a fájlmegosztások összes fájlfogópontját.</span><span class="sxs-lookup"><span data-stu-id="8032b-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="8032b-116">2. példa: Egy fájlkönyvtár összes fogópontját zárja be rekurzív módon, és mutassa a bezárt fájlfogópont számát.</span><span class="sxs-lookup"><span data-stu-id="8032b-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="8032b-117">Ez a parancs bezárja a fájlkönyvtár összes fogópontját, és a bezárt fogópont számát mutatja.</span><span class="sxs-lookup"><span data-stu-id="8032b-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="8032b-118">3. példa: Az összes olyan fájlkezelő fogópont bezárása, amelyet egy nappal ezelőtt nyitottak meg egy fájlkönyvtárban</span><span class="sxs-lookup"><span data-stu-id="8032b-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="8032b-119">Ez a parancs felsorolja a fájlkönyvtárak rekurzív fájlkezelőit, kiszűri az 1 napja megnyitott fogópontokat, majd bezárja őket.</span><span class="sxs-lookup"><span data-stu-id="8032b-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="8032b-120">4. példa: Fájl összes fogópontának bezárása</span><span class="sxs-lookup"><span data-stu-id="8032b-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="8032b-121">Ez a parancs bezárja a fájl összes fájlfogópontját.</span><span class="sxs-lookup"><span data-stu-id="8032b-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="8032b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8032b-122">PARAMETERS</span></span>

### <span data-ttu-id="8032b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8032b-123">-AsJob</span></span>
<span data-ttu-id="8032b-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8032b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8032b-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8032b-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8032b-126">Az ügyféloldali maximális végrehajtási idő másodpercben minden egyes kéréshez.</span><span class="sxs-lookup"><span data-stu-id="8032b-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="8032b-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="8032b-127">-CloseAll</span></span>
<span data-ttu-id="8032b-128">Kényszerítsen minden fájlfogópontot.</span><span class="sxs-lookup"><span data-stu-id="8032b-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8032b-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8032b-130">Az egyidejű aszinkron feladatok teljes mennyisége.</span><span class="sxs-lookup"><span data-stu-id="8032b-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="8032b-131">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8032b-131">The default value is 10.</span></span>

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

### <span data-ttu-id="8032b-132">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8032b-132">-Context</span></span>
<span data-ttu-id="8032b-133">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="8032b-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8032b-134">-DefaultProfile</span></span>
<span data-ttu-id="8032b-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8032b-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8032b-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="8032b-136">-Directory</span></span>
<span data-ttu-id="8032b-137">A CloudFileDirectory objektum azt az alapmappát jelölte meg, amelyben a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="8032b-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-138">-File</span><span class="sxs-lookup"><span data-stu-id="8032b-138">-File</span></span>
<span data-ttu-id="8032b-139">A CloudFile objektum a fogópontot bezárni kívánt fájlnak jelölte.</span><span class="sxs-lookup"><span data-stu-id="8032b-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="8032b-140">-FileHandle</span></span>
<span data-ttu-id="8032b-141">A bezárni kívánt fájlfogópont.</span><span class="sxs-lookup"><span data-stu-id="8032b-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8032b-142">-PassThru</span></span>
<span data-ttu-id="8032b-143">A bezárt fogópontokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8032b-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="8032b-144">-Path</span><span class="sxs-lookup"><span data-stu-id="8032b-144">-Path</span></span>
<span data-ttu-id="8032b-145">Egy meglévő fájl/könyvtár elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8032b-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-146">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="8032b-146">-Recursive</span></span>
<span data-ttu-id="8032b-147">Listafogópontokat rekurzív módon.</span><span class="sxs-lookup"><span data-stu-id="8032b-147">List handles Recursively.</span></span>
<span data-ttu-id="8032b-148">Csak a fájlkönyvtárban működik.</span><span class="sxs-lookup"><span data-stu-id="8032b-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8032b-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8032b-150">A kiszolgáló másodpercek alatt időkorrektaidőt ad az egyes kérések számára.</span><span class="sxs-lookup"><span data-stu-id="8032b-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="8032b-151">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="8032b-151">-Share</span></span>
<span data-ttu-id="8032b-152">A CloudFileShare objektum azt a megosztást jelölte meg, ahol a fájlok/könyvtárak fel vannak sorolva.</span><span class="sxs-lookup"><span data-stu-id="8032b-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8032b-153">-ShareName</span></span>
<span data-ttu-id="8032b-154">Annak a fájlmegosztásnak a neve, amelyben a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="8032b-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8032b-155">-Confirm</span></span>
<span data-ttu-id="8032b-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8032b-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8032b-157">-WhatIf</span></span>
<span data-ttu-id="8032b-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8032b-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8032b-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8032b-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8032b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8032b-160">CommonParameters</span></span>
<span data-ttu-id="8032b-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8032b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8032b-162">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8032b-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8032b-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8032b-163">INPUTS</span></span>

### <span data-ttu-id="8032b-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8032b-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="8032b-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8032b-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="8032b-166">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8032b-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8032b-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8032b-167">OUTPUTS</span></span>

### <span data-ttu-id="8032b-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="8032b-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="8032b-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8032b-169">NOTES</span></span>

## <span data-ttu-id="8032b-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8032b-170">RELATED LINKS</span></span>
