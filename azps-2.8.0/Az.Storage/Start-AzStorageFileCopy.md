---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: bdd92d01c7b2a69f588b54504f014ea6b17d0aff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839627"
---
# <span data-ttu-id="e0907-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e0907-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="e0907-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0907-102">SYNOPSIS</span></span>
<span data-ttu-id="e0907-103">Elindítja a forrásfájl másolását.</span><span class="sxs-lookup"><span data-stu-id="e0907-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="e0907-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0907-104">SYNTAX</span></span>

### <span data-ttu-id="e0907-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="e0907-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0907-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e0907-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0907-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="e0907-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0907-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="e0907-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0907-109">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="e0907-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0907-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="e0907-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0907-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="e0907-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0907-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="e0907-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0907-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="e0907-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0907-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="e0907-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0907-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0907-115">DESCRIPTION</span></span>
<span data-ttu-id="e0907-116">A **Start-AzStorageFileCopy** parancsmag a forrásfájl szövegfájlba való másolását kezdi.</span><span class="sxs-lookup"><span data-stu-id="e0907-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="e0907-117">Példák</span><span class="sxs-lookup"><span data-stu-id="e0907-117">EXAMPLES</span></span>

### <span data-ttu-id="e0907-118">1. példa: a másolási művelet indítása fájlból fájlból fájlból a megosztás név és fájlnév használatával</span><span class="sxs-lookup"><span data-stu-id="e0907-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="e0907-119">Ez a parancs a fájlból fájlból másolt műveletet indítja el.</span><span class="sxs-lookup"><span data-stu-id="e0907-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="e0907-120">A parancs a megosztás neve és a fájlnév nevet adja meg</span><span class="sxs-lookup"><span data-stu-id="e0907-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="e0907-121">2. példa: a másolási művelet indítása blobról fájlra a tároló neve és a blob neve segítségével</span><span class="sxs-lookup"><span data-stu-id="e0907-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="e0907-122">Ez a parancs egy másolati műveletet indít el a blob-fájlból.</span><span class="sxs-lookup"><span data-stu-id="e0907-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="e0907-123">A parancs a tároló nevét és a blob nevét adja meg</span><span class="sxs-lookup"><span data-stu-id="e0907-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="e0907-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0907-124">PARAMETERS</span></span>

### <span data-ttu-id="e0907-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="e0907-125">-AbsoluteUri</span></span>
<span data-ttu-id="e0907-126">A forrásfájl URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="e0907-127">Ha a forrás helyéhez hitelesítő adatokra van szükség, meg kell adnia egyet.</span><span class="sxs-lookup"><span data-stu-id="e0907-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="e0907-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e0907-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e0907-129">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="e0907-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e0907-130">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="e0907-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e0907-131">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="e0907-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e0907-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e0907-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e0907-133">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e0907-134">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="e0907-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e0907-135">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="e0907-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e0907-136">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="e0907-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e0907-137">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="e0907-137">The default value is 10.</span></span>

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

### <span data-ttu-id="e0907-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e0907-138">-Context</span></span>
<span data-ttu-id="e0907-139">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e0907-140">Környezet beolvasásához használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e0907-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e0907-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0907-141">-DefaultProfile</span></span>
<span data-ttu-id="e0907-142">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0907-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0907-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="e0907-143">-DestContext</span></span>
<span data-ttu-id="e0907-144">A cél Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="e0907-145">Környezet beolvasásához használja az **új AzStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="e0907-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="e0907-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="e0907-146">-DestFile</span></span>
<span data-ttu-id="e0907-147">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e0907-148">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e0907-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="e0907-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="e0907-149">-DestFilePath</span></span>
<span data-ttu-id="e0907-150">A célfájl elérési útját adja meg a cél megosztásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="e0907-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="e0907-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="e0907-151">-DestShareName</span></span>
<span data-ttu-id="e0907-152">A célként megadott megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="e0907-153">-Force</span><span class="sxs-lookup"><span data-stu-id="e0907-153">-Force</span></span>
<span data-ttu-id="e0907-154">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e0907-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0907-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e0907-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e0907-156">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e0907-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="e0907-157">-SrcBlob</span></span>
<span data-ttu-id="e0907-158">Egy **CloudBlob** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="e0907-159">A Get-AzStorageBlob parancsmag segítségével létrehozhat egy felhőalapú blobot, vagy megadhat egyet.</span><span class="sxs-lookup"><span data-stu-id="e0907-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="e0907-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="e0907-160">-SrcBlobName</span></span>
<span data-ttu-id="e0907-161">A forrás blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="e0907-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="e0907-162">-SrcContainer</span></span>
<span data-ttu-id="e0907-163">Egy felhőalapú blob-tároló objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="e0907-164">Létrehozhat felhőalapú blob-tároló objektumot, vagy használhatja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e0907-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="e0907-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="e0907-165">-SrcContainerName</span></span>
<span data-ttu-id="e0907-166">A forrás tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="e0907-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="e0907-167">-SrcFile</span></span>
<span data-ttu-id="e0907-168">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e0907-169">Létrehozhat egy felhőalapú fájlt, vagy beszerezhet egyet a **Get-AzStorageFile** segítségével.</span><span class="sxs-lookup"><span data-stu-id="e0907-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0907-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="e0907-170">-SrcFilePath</span></span>
<span data-ttu-id="e0907-171">A forrásfájl elérési útvonalát adja meg a forrás vagy a forrás megosztásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="e0907-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="e0907-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="e0907-172">-SrcShare</span></span>
<span data-ttu-id="e0907-173">A felhőalapú fájlmegosztás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="e0907-174">A Get-AzStorageShare parancsmag segítségével létrehozhatja a felhőalapú fájlokat, vagy megadhat egyet.</span><span class="sxs-lookup"><span data-stu-id="e0907-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0907-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="e0907-175">-SrcShareName</span></span>
<span data-ttu-id="e0907-176">A forrás megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0907-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="e0907-177">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0907-177">-Confirm</span></span>
<span data-ttu-id="e0907-178">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0907-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0907-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0907-179">-WhatIf</span></span>
<span data-ttu-id="e0907-180">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0907-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0907-181">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0907-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0907-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0907-182">CommonParameters</span></span>
<span data-ttu-id="e0907-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0907-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0907-184">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0907-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0907-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0907-185">INPUTS</span></span>

### <span data-ttu-id="e0907-186">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e0907-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e0907-187">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e0907-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="e0907-188">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0907-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e0907-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0907-189">OUTPUTS</span></span>

### <span data-ttu-id="e0907-190">System. Void</span><span class="sxs-lookup"><span data-stu-id="e0907-190">System.Void</span></span>

## <span data-ttu-id="e0907-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0907-191">NOTES</span></span>

## <span data-ttu-id="e0907-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0907-192">RELATED LINKS</span></span>

[<span data-ttu-id="e0907-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e0907-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e0907-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e0907-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="e0907-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e0907-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="e0907-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="e0907-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="e0907-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="e0907-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="e0907-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e0907-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
