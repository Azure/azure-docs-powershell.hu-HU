---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: cca517246f548deb64cba1b4bc737de88628e7f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839600"
---
# <span data-ttu-id="a5674-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a5674-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="a5674-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5674-102">SYNOPSIS</span></span>
<span data-ttu-id="a5674-103">Bezárja a fájlmegosztás, a fájl vagy a fájl fájljait.</span><span class="sxs-lookup"><span data-stu-id="a5674-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="a5674-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5674-104">SYNTAX</span></span>

### <span data-ttu-id="a5674-105">ShareNameCloseAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5674-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5674-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="a5674-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5674-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="a5674-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5674-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="a5674-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5674-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="a5674-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5674-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="a5674-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5674-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5674-111">DESCRIPTION</span></span>
<span data-ttu-id="a5674-112">A **Close-AzStorageFileHandle** parancsmag bezárja a fájlmegosztás, a fájl vagy a fájl könyvtárát.</span><span class="sxs-lookup"><span data-stu-id="a5674-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="a5674-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a5674-113">EXAMPLES</span></span>

### <span data-ttu-id="a5674-114">Példa 1: a jelenlegi tárterület-fiók összes fájl-megosztásának felsorolása, és a fájlmegosztás minden fájlleíró rekurzív bezárása.</span><span class="sxs-lookup"><span data-stu-id="a5674-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="a5674-115">Ez a parancs felsorolja a jelenlegi tárterület-fiók összes fájl-megosztását, és bezárja a fájlmegosztás minden fájlleíró rekurzív módon.</span><span class="sxs-lookup"><span data-stu-id="a5674-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="a5674-116">2. példa: a Fájlkezelőben lévő összes fájlkezelőt rekurzív módon kikapcsolja, és a zárolt fájlleíró számát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="a5674-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="a5674-117">Ez a parancs bezárja a fájlkezelők minden fájlleíró elemét, és megjeleníti a zárolt fájlleíró számát.</span><span class="sxs-lookup"><span data-stu-id="a5674-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="a5674-118">3. példa: az összes olyan fájlleíró bezárása, amely 1 nappal ezelőtt nyílik meg a fájl könyvtárában</span><span class="sxs-lookup"><span data-stu-id="a5674-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="a5674-119">Ez a parancs felsorolja az összes fájlleíró rekurzívan, kiszűri az 1 nappal korábban megnyitott fogópontokat, majd bezárja őket.</span><span class="sxs-lookup"><span data-stu-id="a5674-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="a5674-120">Példa 4: a fájl minden fogópontjának bezárása</span><span class="sxs-lookup"><span data-stu-id="a5674-120">Example 4: Close all file handles on a file</span></span> 
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="a5674-121">Ez a parancs bezárja a fájl minden fájlleíró funkcióját.</span><span class="sxs-lookup"><span data-stu-id="a5674-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="a5674-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5674-122">PARAMETERS</span></span>

### <span data-ttu-id="a5674-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5674-123">-AsJob</span></span>
<span data-ttu-id="a5674-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a5674-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5674-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a5674-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a5674-126">Az ügyféloldali kérelmek maximális végrehajtási ideje másodpercben.</span><span class="sxs-lookup"><span data-stu-id="a5674-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="a5674-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="a5674-127">-CloseAll</span></span>
<span data-ttu-id="a5674-128">Kényszerítse az összes fájlleíró bezárását.</span><span class="sxs-lookup"><span data-stu-id="a5674-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="a5674-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a5674-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a5674-130">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="a5674-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="a5674-131">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a5674-131">The default value is 10.</span></span>

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

### <span data-ttu-id="a5674-132">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a5674-132">-Context</span></span>
<span data-ttu-id="a5674-133">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="a5674-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a5674-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5674-134">-DefaultProfile</span></span>
<span data-ttu-id="a5674-135">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5674-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5674-136">-Címtár</span><span class="sxs-lookup"><span data-stu-id="a5674-136">-Directory</span></span>
<span data-ttu-id="a5674-137">CloudFileDirectory objektum: azt az alapmappát jelezte, ahol a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="a5674-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5674-138">-Fájl</span><span class="sxs-lookup"><span data-stu-id="a5674-138">-File</span></span>
<span data-ttu-id="a5674-139">CloudFile objektum: a fájlt a záró fogópontra jelölte ki.</span><span class="sxs-lookup"><span data-stu-id="a5674-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5674-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="a5674-140">-FileHandle</span></span>
<span data-ttu-id="a5674-141">A bezárni kívánt fájlleíró</span><span class="sxs-lookup"><span data-stu-id="a5674-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="a5674-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5674-142">-PassThru</span></span>
<span data-ttu-id="a5674-143">A zárolt fájlleíró számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a5674-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="a5674-144">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a5674-144">-Path</span></span>
<span data-ttu-id="a5674-145">Meglévő fájl vagy könyvtár elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="a5674-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="a5674-146">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="a5674-146">-Recursive</span></span>
<span data-ttu-id="a5674-147">A lista rekurzív módon kezeli a listákat.</span><span class="sxs-lookup"><span data-stu-id="a5674-147">List handles Recursively.</span></span>
<span data-ttu-id="a5674-148">Csak a fájl címtárban működik.</span><span class="sxs-lookup"><span data-stu-id="a5674-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="a5674-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a5674-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a5674-150">A kiszolgáló az egyes kérésekhez másodpercben megadott időpontot.</span><span class="sxs-lookup"><span data-stu-id="a5674-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="a5674-151">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="a5674-151">-Share</span></span>
<span data-ttu-id="a5674-152">A CloudFileShare objektum azt a megosztást jelezte, ahol a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="a5674-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5674-153">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="a5674-153">-ShareName</span></span>
<span data-ttu-id="a5674-154">Annak a fájlnak a neve, amelyben a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="a5674-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="a5674-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5674-155">-Confirm</span></span>
<span data-ttu-id="a5674-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5674-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5674-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5674-157">-WhatIf</span></span>
<span data-ttu-id="a5674-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5674-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5674-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5674-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5674-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5674-160">CommonParameters</span></span>
<span data-ttu-id="a5674-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5674-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5674-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5674-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5674-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5674-163">INPUTS</span></span>

### <span data-ttu-id="a5674-164">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a5674-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="a5674-165">Microsoft. Azure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a5674-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="a5674-166">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5674-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a5674-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5674-167">OUTPUTS</span></span>

### <span data-ttu-id="a5674-168">Microsoft. Azure. Storage. file. CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="a5674-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="a5674-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5674-169">NOTES</span></span>

## <span data-ttu-id="a5674-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5674-170">RELATED LINKS</span></span>
