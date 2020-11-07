---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 7ee939d489bdc66d9268a3af1e9ee9fe46818fd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839704"
---
# <span data-ttu-id="15d28-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="15d28-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="15d28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15d28-102">SYNOPSIS</span></span>
<span data-ttu-id="15d28-103">A fájlmegosztás, a fájl vagy a fájl fájljainak a fájljait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="15d28-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="15d28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15d28-104">SYNTAX</span></span>

### <span data-ttu-id="15d28-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15d28-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="15d28-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="15d28-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="15d28-107">Directory</span><span class="sxs-lookup"><span data-stu-id="15d28-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="15d28-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="15d28-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="15d28-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="15d28-109">DESCRIPTION</span></span>
<span data-ttu-id="15d28-110">A **Get-AzStorageFileHandle** parancsmag a fájlmegosztás, a fájl vagy a fájl könyvtárát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="15d28-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="15d28-111">Példák</span><span class="sxs-lookup"><span data-stu-id="15d28-111">EXAMPLES</span></span>

### <span data-ttu-id="15d28-112">1. példa: a fájlmegosztás minden fájlleíró rekurzív módon, az ClientIp és a OpenTime szerint rendezve</span><span class="sxs-lookup"><span data-stu-id="15d28-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="15d28-113">Ez a parancs felsorolja a fájlok megosztását, és a kimenetet ClientIp, majd a OpenTime szerint rendezi.</span><span class="sxs-lookup"><span data-stu-id="15d28-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="15d28-114">2. példa: a fájl első 2 fájlleíró-fogópontjának listája rekurzívan</span><span class="sxs-lookup"><span data-stu-id="15d28-114">Example 2: List first 2 file handles on a file directory recursively</span></span> 
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="15d28-115">Ez a parancs az első 2 fájlleíró rekurzív módon jeleníti meg a fájl könyvtárát.</span><span class="sxs-lookup"><span data-stu-id="15d28-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="15d28-116">3. példa: a harmadik a 6. fájl fogópontjának felsorolása egy fájlon</span><span class="sxs-lookup"><span data-stu-id="15d28-116">Example 3: List the 3rd to the 6th file handles on a file</span></span> 
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="15d28-117">Ez a parancs felsorolja a 3 a 6 a fájlon lévő fogópontokat.</span><span class="sxs-lookup"><span data-stu-id="15d28-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="15d28-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15d28-118">PARAMETERS</span></span>

### <span data-ttu-id="15d28-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="15d28-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="15d28-120">Az ügyféloldali kérelmek maximális végrehajtási ideje másodpercben.</span><span class="sxs-lookup"><span data-stu-id="15d28-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="15d28-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="15d28-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="15d28-122">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="15d28-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="15d28-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="15d28-123">The default value is 10.</span></span>

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

### <span data-ttu-id="15d28-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="15d28-124">-Context</span></span>
<span data-ttu-id="15d28-125">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="15d28-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="15d28-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d28-126">-DefaultProfile</span></span>
<span data-ttu-id="15d28-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15d28-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d28-128">-Címtár</span><span class="sxs-lookup"><span data-stu-id="15d28-128">-Directory</span></span>
<span data-ttu-id="15d28-129">CloudFileDirectory objektum: azt az alapmappát jelezte, ahol a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="15d28-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="15d28-130">-Fájl</span><span class="sxs-lookup"><span data-stu-id="15d28-130">-File</span></span>
<span data-ttu-id="15d28-131">CloudFile objektum: a fájl a fájllista fogópontokat jelölte ki.</span><span class="sxs-lookup"><span data-stu-id="15d28-131">CloudFile object indicated the file to list File Handles.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15d28-132">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="15d28-132">-Path</span></span>
<span data-ttu-id="15d28-133">Meglévő fájl vagy könyvtár elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="15d28-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d28-134">-Rekurzív</span><span class="sxs-lookup"><span data-stu-id="15d28-134">-Recursive</span></span>
<span data-ttu-id="15d28-135">A lista rekurzív módon kezeli a listákat.</span><span class="sxs-lookup"><span data-stu-id="15d28-135">List handles Recursively.</span></span>
<span data-ttu-id="15d28-136">Csak a fájl címtárban működik.</span><span class="sxs-lookup"><span data-stu-id="15d28-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="15d28-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="15d28-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="15d28-138">A kiszolgáló az egyes kérésekhez másodpercben megadott időpontot.</span><span class="sxs-lookup"><span data-stu-id="15d28-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="15d28-139">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="15d28-139">-Share</span></span>
<span data-ttu-id="15d28-140">A CloudFileShare objektum azt a megosztást jelezte, ahol a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="15d28-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="15d28-141">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="15d28-141">-ShareName</span></span>
<span data-ttu-id="15d28-142">Annak a fájlnak a neve, amelyben a fájlok/könyvtárak szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="15d28-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="15d28-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="15d28-143">-IncludeTotalCount</span></span>
<span data-ttu-id="15d28-144">Az adathalmazban lévő objektumok (egy egész) számát, majd az objektumok számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="15d28-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="15d28-145">Ha a parancsmag nem tudja megállapítani a teljes számlálást, az "ismeretlen összeg számítása" értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="15d28-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="15d28-146">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="15d28-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="15d28-147">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="15d28-147">-Skip</span></span>
<span data-ttu-id="15d28-148">Figyelmen kívül hagyja az első ' n ' objektumokat, majd a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="15d28-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d28-149">– Első</span><span class="sxs-lookup"><span data-stu-id="15d28-149">-First</span></span>
<span data-ttu-id="15d28-150">Csak az első ' n ' objektumokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15d28-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d28-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d28-151">CommonParameters</span></span>
<span data-ttu-id="15d28-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15d28-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d28-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d28-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d28-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15d28-154">INPUTS</span></span>

### <span data-ttu-id="15d28-155">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="15d28-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="15d28-156">Microsoft. Azure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="15d28-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="15d28-157">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="15d28-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="15d28-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15d28-158">OUTPUTS</span></span>

### <span data-ttu-id="15d28-159">Microsoft. Azure. Storage. file. FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="15d28-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="15d28-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15d28-160">NOTES</span></span>

## <span data-ttu-id="15d28-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15d28-161">RELATED LINKS</span></span>
