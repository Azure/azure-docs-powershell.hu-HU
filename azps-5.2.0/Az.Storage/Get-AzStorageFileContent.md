---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349637"
---
# <span data-ttu-id="7d98e-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d98e-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="7d98e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d98e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d98e-103">Letölti egy fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="7d98e-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="7d98e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7d98e-104">SYNTAX</span></span>

### <span data-ttu-id="7d98e-105">ShareName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d98e-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7d98e-106">Megosztás</span><span class="sxs-lookup"><span data-stu-id="7d98e-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7d98e-107">Címtár</span><span class="sxs-lookup"><span data-stu-id="7d98e-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7d98e-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="7d98e-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="7d98e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7d98e-109">DESCRIPTION</span></span>
<span data-ttu-id="7d98e-110">A **Get-AzStorageFileContent** parancsmag letölti egy fájl tartalmát, majd egy Ön által megadott célhelyre menti.</span><span class="sxs-lookup"><span data-stu-id="7d98e-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="7d98e-111">Ez a parancsmag nem adja vissza a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="7d98e-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="7d98e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7d98e-112">EXAMPLES</span></span>

### <span data-ttu-id="7d98e-113">1. példa: Fájl letöltése egy mappából</span><span class="sxs-lookup"><span data-stu-id="7d98e-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="7d98e-114">Ez a parancs letölt egy CurrentDataFile nevű fájlt a ContosoWorkingFolder mappából a ContosoShare06 fájlból az aktuális mappába.</span><span class="sxs-lookup"><span data-stu-id="7d98e-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="7d98e-115">2. példa: A mintafájlmegosztás alatti fájlok letöltése</span><span class="sxs-lookup"><span data-stu-id="7d98e-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="7d98e-116">Ez a példa letölti a mintafájlmegosztás alatti fájlokat</span><span class="sxs-lookup"><span data-stu-id="7d98e-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="7d98e-117">3. példa: Töltsön le egy Azure-fájlt egy helyi fájlba, és a helyi fájlban tartsa meg az Azure-fájl SMB-tulajdonságait (fájl-hozzárendelések, fájl létrehozási ideje, legutóbbi írási idő).</span><span class="sxs-lookup"><span data-stu-id="7d98e-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="7d98e-118">Ez a példa letölt egy Azure-fájlt egy helyi fájlba, és a helyi fájlban az Azure-fájl SMB-tulajdonságait (Fájl-hozzárendelések, Fájlkészítési idő, Fájl legutóbbi írási ideje) is használja.</span><span class="sxs-lookup"><span data-stu-id="7d98e-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="7d98e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d98e-119">PARAMETERS</span></span>

### <span data-ttu-id="7d98e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d98e-120">-AsJob</span></span>
<span data-ttu-id="7d98e-121">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="7d98e-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7d98e-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="7d98e-122">-CheckMd5</span></span>
<span data-ttu-id="7d98e-123">Azt adja meg, hogy ellenőrizze-e a letöltött fájl Md5-ös összegét.</span><span class="sxs-lookup"><span data-stu-id="7d98e-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="7d98e-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d98e-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7d98e-125">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7d98e-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="7d98e-126">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="7d98e-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="7d98e-127">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="7d98e-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7d98e-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7d98e-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7d98e-129">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="7d98e-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="7d98e-130">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="7d98e-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="7d98e-131">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="7d98e-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="7d98e-132">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7d98e-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="7d98e-133">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7d98e-133">The default value is 10.</span></span>

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

### <span data-ttu-id="7d98e-134">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7d98e-134">-Context</span></span>
<span data-ttu-id="7d98e-135">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="7d98e-136">Környezet lekérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7d98e-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7d98e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d98e-137">-DefaultProfile</span></span>
<span data-ttu-id="7d98e-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d98e-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d98e-139">-Destination</span><span class="sxs-lookup"><span data-stu-id="7d98e-139">-Destination</span></span>
<span data-ttu-id="7d98e-140">Megadja a cél elérési útját.</span><span class="sxs-lookup"><span data-stu-id="7d98e-140">Specifies the destination path.</span></span>
<span data-ttu-id="7d98e-141">Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="7d98e-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="7d98e-142">Ha olyan fájl elérési útját adja meg, amely nem létezik, ez a parancsmag létrehozza a fájlt, és a tartalmat az új fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="7d98e-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7d98e-143">Ha megad egy már létező fájl elérési útját, és megadja a *Force* paramétert, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="7d98e-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7d98e-144">Ha megadja egy meglévő fájl elérési útját, és nem adja meg az Kényszerítés *parancsot,* a parancsmag a továbblépés előtt megkérdezi.</span><span class="sxs-lookup"><span data-stu-id="7d98e-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7d98e-145">Ha megadja egy mappa elérési útját, ez a parancsmag megkísérli létrehozni az Azure-tárfájl nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="7d98e-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7d98e-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="7d98e-146">-Directory</span></span>
<span data-ttu-id="7d98e-147">Mappát ad meg **CloudFileDirectory objektumként.**</span><span class="sxs-lookup"><span data-stu-id="7d98e-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7d98e-148">Ez a parancsmag a paraméter által megadott mappában lévő fájl tartalmát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="7d98e-149">Címtár beszerzéséhez használja a New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7d98e-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7d98e-150">Címtár beszerzéséhez használhatja Get-AzStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="7d98e-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="7d98e-151">-File</span><span class="sxs-lookup"><span data-stu-id="7d98e-151">-File</span></span>
<span data-ttu-id="7d98e-152">Egy fájlt ad meg **CloudFile-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="7d98e-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="7d98e-153">Ez a parancsmag a paraméter által megadott fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="7d98e-154">**CloudFile-objektum** beszerzéséhez használja a Get-AzStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7d98e-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="7d98e-155">-Force</span><span class="sxs-lookup"><span data-stu-id="7d98e-155">-Force</span></span>
<span data-ttu-id="7d98e-156">Ha olyan fájl elérési útját adja meg, amely nem létezik, ez a parancsmag létrehozza a fájlt, és a tartalmat az új fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="7d98e-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7d98e-157">Ha megad egy már létező fájl elérési útját, és megadja a *Force* paramétert, a parancsmag felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="7d98e-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7d98e-158">Ha megadja egy meglévő fájl elérési útját, és nem adja meg az Kényszerítés *parancsot,* a parancsmag a továbblépés előtt megkérdezi.</span><span class="sxs-lookup"><span data-stu-id="7d98e-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7d98e-159">Ha megadja egy mappa elérési útját, ez a parancsmag megkísérli létrehozni az Azure-tárfájl nevét tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="7d98e-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7d98e-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d98e-160">-PassThru</span></span>
<span data-ttu-id="7d98e-161">Azt jelzi, hogy ez a parancsmag a letöltött **AzureStorageFile** objektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="7d98e-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="7d98e-162">-Path</span><span class="sxs-lookup"><span data-stu-id="7d98e-162">-Path</span></span>
<span data-ttu-id="7d98e-163">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-163">Specifies the path of a file.</span></span>
<span data-ttu-id="7d98e-164">Ez a parancsmag a paraméter által megadott fájl tartalmát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="7d98e-165">Ha a fájl nem létezik, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="7d98e-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7d98e-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="7d98e-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="7d98e-167">A forrásfájl SMB-tulajdonságait (Fájl-hozzárendelések, Fájl létrehozási idő, Legutóbbi írási időpont) a célfájlban tartsa meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="7d98e-168">Ez a paraméter csak Windows rendszeren érhető el.</span><span class="sxs-lookup"><span data-stu-id="7d98e-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="7d98e-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d98e-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7d98e-170">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="7d98e-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="7d98e-171">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="7d98e-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7d98e-172">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="7d98e-172">-Share</span></span>
<span data-ttu-id="7d98e-173">Egy **CloudFileShare-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7d98e-174">Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="7d98e-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="7d98e-175">**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7d98e-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="7d98e-176">Ez az objektum tartalmazza a tárterület környezetét.</span><span class="sxs-lookup"><span data-stu-id="7d98e-176">This object contains the storage context.</span></span>
<span data-ttu-id="7d98e-177">Ha ezt a paramétert adja meg, ne adja meg a környezet *paramétert.*</span><span class="sxs-lookup"><span data-stu-id="7d98e-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="7d98e-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7d98e-178">-ShareName</span></span>
<span data-ttu-id="7d98e-179">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d98e-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="7d98e-180">Ez a parancsmag letölti a fájl tartalmát a paraméter által megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="7d98e-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="7d98e-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d98e-181">-Confirm</span></span>
<span data-ttu-id="7d98e-182">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7d98e-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d98e-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d98e-183">-WhatIf</span></span>
<span data-ttu-id="7d98e-184">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7d98e-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d98e-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d98e-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d98e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d98e-186">CommonParameters</span></span>
<span data-ttu-id="7d98e-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d98e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d98e-188">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d98e-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d98e-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d98e-189">INPUTS</span></span>

### <span data-ttu-id="7d98e-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7d98e-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="7d98e-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7d98e-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="7d98e-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="7d98e-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="7d98e-193">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d98e-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7d98e-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d98e-194">OUTPUTS</span></span>

### <span data-ttu-id="7d98e-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="7d98e-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="7d98e-196">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7d98e-196">NOTES</span></span>

## <span data-ttu-id="7d98e-197">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d98e-197">RELATED LINKS</span></span>

[<span data-ttu-id="7d98e-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="7d98e-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="7d98e-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d98e-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


