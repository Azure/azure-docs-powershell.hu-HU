---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150371"
---
# <span data-ttu-id="709d9-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="709d9-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="709d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="709d9-102">SYNOPSIS</span></span>
<span data-ttu-id="709d9-103">Megkezdi a forrásfájl másolását.</span><span class="sxs-lookup"><span data-stu-id="709d9-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="709d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="709d9-104">SYNTAX</span></span>

### <span data-ttu-id="709d9-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="709d9-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="709d9-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="709d9-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709d9-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="709d9-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709d9-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="709d9-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709d9-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="709d9-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="709d9-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="709d9-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709d9-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="709d9-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709d9-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="709d9-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709d9-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="709d9-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709d9-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="709d9-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="709d9-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="709d9-115">DESCRIPTION</span></span>
<span data-ttu-id="709d9-116">A **Start-AzStorageFileCopy** parancsmag megkezdi a forrásfájl célfájlba másolását.</span><span class="sxs-lookup"><span data-stu-id="709d9-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="709d9-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="709d9-117">EXAMPLES</span></span>

### <span data-ttu-id="709d9-118">1. példa: Másolási művelet kezdése fájlról fájlra megosztási név és fájlnév használatával</span><span class="sxs-lookup"><span data-stu-id="709d9-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="709d9-119">Ez a parancs egy másolási műveletet kezd fájlról fájlra.</span><span class="sxs-lookup"><span data-stu-id="709d9-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="709d9-120">A parancs megadja a megosztás nevét és a fájlnevet</span><span class="sxs-lookup"><span data-stu-id="709d9-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="709d9-121">2. példa: Másolási művelet indítása blobból fájlba tárolónév és blobnév használatával</span><span class="sxs-lookup"><span data-stu-id="709d9-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="709d9-122">Ez a parancs másolási műveletet kezd blobról fájlra.</span><span class="sxs-lookup"><span data-stu-id="709d9-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="709d9-123">A parancs megadja a tároló és a blob nevét</span><span class="sxs-lookup"><span data-stu-id="709d9-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="709d9-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="709d9-124">PARAMETERS</span></span>

### <span data-ttu-id="709d9-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="709d9-125">-AbsoluteUri</span></span>
<span data-ttu-id="709d9-126">A forrásfájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="709d9-127">Ha a forráshely hitelesítő adatokat igényel, meg kell adnia egyet.</span><span class="sxs-lookup"><span data-stu-id="709d9-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="709d9-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="709d9-129">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="709d9-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="709d9-130">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="709d9-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="709d9-131">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="709d9-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="709d9-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="709d9-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="709d9-133">Megadja a maximális párhuzamos hálózati hívást.</span><span class="sxs-lookup"><span data-stu-id="709d9-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="709d9-134">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="709d9-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="709d9-135">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="709d9-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="709d9-136">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="709d9-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="709d9-137">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="709d9-137">The default value is 10.</span></span>

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

### <span data-ttu-id="709d9-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="709d9-138">-Context</span></span>
<span data-ttu-id="709d9-139">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="709d9-140">Környezet lekérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="709d9-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709d9-141">-DefaultProfile</span></span>
<span data-ttu-id="709d9-142">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="709d9-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="709d9-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="709d9-143">-DestContext</span></span>
<span data-ttu-id="709d9-144">Megadja a cél Azure Storage környezetét.</span><span class="sxs-lookup"><span data-stu-id="709d9-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="709d9-145">Környezet beszerzéséhez használja a **New-AzStorageContext függvényt.**</span><span class="sxs-lookup"><span data-stu-id="709d9-145">To obtain a context, use **New-AzStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="709d9-146">-DestFile</span></span>
<span data-ttu-id="709d9-147">Egy **CloudFile-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="709d9-148">Létrehozhat felhőfájlt, vagy beszerezhet egyet a Get-AzStorageFile parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="709d9-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="709d9-149">-DestFilePath</span></span>
<span data-ttu-id="709d9-150">A célfájl elérési útját adja meg a célmegosztáshoz képest.</span><span class="sxs-lookup"><span data-stu-id="709d9-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="709d9-151">-DestShareName</span></span>
<span data-ttu-id="709d9-152">A cél megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-153">-Force</span><span class="sxs-lookup"><span data-stu-id="709d9-153">-Force</span></span>
<span data-ttu-id="709d9-154">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="709d9-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="709d9-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="709d9-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="709d9-156">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="709d9-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="709d9-157">-SrcBlob</span></span>
<span data-ttu-id="709d9-158">Egy **CloudBlob-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="709d9-159">Létrehozhat felhő blobot, vagy beszerezhet egyet a Get-AzStorageBlob parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="709d9-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="709d9-160">-SrcBlobName</span></span>
<span data-ttu-id="709d9-161">A forrás blob nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="709d9-162">-SrcContainer</span></span>
<span data-ttu-id="709d9-163">Egy felhőbeli blobtároló-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="709d9-164">Létrehozhat felhőbeli blobtároló objektumot, vagy használhatja a Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="709d9-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="709d9-165">-SrcContainerName</span></span>
<span data-ttu-id="709d9-166">A forrástároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="709d9-167">-SrcFile</span></span>
<span data-ttu-id="709d9-168">Egy **CloudFile-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="709d9-169">Felhőfájlt a **Get-AzStorageFile** használatával hozhat létre vagy szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="709d9-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="709d9-170">-SrcFilePath</span></span>
<span data-ttu-id="709d9-171">A forrásfájl elérési útját adja meg a forráscímtárhoz vagy a forrásmegosztáshoz képest.</span><span class="sxs-lookup"><span data-stu-id="709d9-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="709d9-172">-SrcShare</span></span>
<span data-ttu-id="709d9-173">Egy felhőalapú fájlmegosztási objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="709d9-174">Létrehozhat felhőalapú fájlmegosztást, vagy beszerezhet egyet a Get-AzStorageShare parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="709d9-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="709d9-175">-SrcShareName</span></span>
<span data-ttu-id="709d9-176">A forrás megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="709d9-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709d9-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="709d9-177">-Confirm</span></span>
<span data-ttu-id="709d9-178">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="709d9-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="709d9-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="709d9-179">-WhatIf</span></span>
<span data-ttu-id="709d9-180">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="709d9-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="709d9-181">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="709d9-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="709d9-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709d9-182">CommonParameters</span></span>
<span data-ttu-id="709d9-183">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709d9-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709d9-184">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="709d9-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709d9-185">INPUTS</span><span class="sxs-lookup"><span data-stu-id="709d9-185">INPUTS</span></span>

### <span data-ttu-id="709d9-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="709d9-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="709d9-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="709d9-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="709d9-188">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="709d9-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="709d9-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="709d9-189">OUTPUTS</span></span>

### <span data-ttu-id="709d9-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="709d9-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="709d9-191">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="709d9-191">NOTES</span></span>

## <span data-ttu-id="709d9-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="709d9-192">RELATED LINKS</span></span>

[<span data-ttu-id="709d9-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="709d9-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="709d9-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="709d9-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="709d9-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="709d9-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="709d9-196">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="709d9-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="709d9-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="709d9-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="709d9-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="709d9-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
