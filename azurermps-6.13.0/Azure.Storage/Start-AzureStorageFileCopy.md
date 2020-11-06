---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
ms.openlocfilehash: c5e071ddb5316f223260d3e6f239df4e75612332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498579"
---
# <span data-ttu-id="334e7-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="334e7-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="334e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="334e7-102">SYNOPSIS</span></span>
<span data-ttu-id="334e7-103">Elindítja a forrásfájl másolását.</span><span class="sxs-lookup"><span data-stu-id="334e7-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="334e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="334e7-104">SYNTAX</span></span>

### <span data-ttu-id="334e7-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="334e7-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="334e7-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="334e7-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334e7-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="334e7-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334e7-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="334e7-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="334e7-109">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="334e7-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="334e7-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="334e7-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334e7-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="334e7-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334e7-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="334e7-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="334e7-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="334e7-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334e7-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="334e7-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="334e7-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="334e7-115">DESCRIPTION</span></span>
<span data-ttu-id="334e7-116">A **Start-AzureStorageFileCopy** parancsmag a forrásfájl szövegfájlba való másolását kezdi.</span><span class="sxs-lookup"><span data-stu-id="334e7-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="334e7-117">Példák</span><span class="sxs-lookup"><span data-stu-id="334e7-117">EXAMPLES</span></span>

### <span data-ttu-id="334e7-118">1. példa: a másolási művelet indítása fájlból fájlból fájlból a megosztás név és fájlnév használatával</span><span class="sxs-lookup"><span data-stu-id="334e7-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="334e7-119">Ez a parancs a fájlból fájlból másolt műveletet indítja el.</span><span class="sxs-lookup"><span data-stu-id="334e7-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="334e7-120">A parancs a megosztás neve és a fájlnév nevet adja meg</span><span class="sxs-lookup"><span data-stu-id="334e7-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="334e7-121">2. példa: a másolási művelet indítása blobról fájlra a tároló neve és a blob neve segítségével</span><span class="sxs-lookup"><span data-stu-id="334e7-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="334e7-122">Ez a parancs egy másolati műveletet indít el a blob-fájlból.</span><span class="sxs-lookup"><span data-stu-id="334e7-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="334e7-123">A parancs a tároló nevét és a blob nevét adja meg</span><span class="sxs-lookup"><span data-stu-id="334e7-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="334e7-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="334e7-124">PARAMETERS</span></span>

### <span data-ttu-id="334e7-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="334e7-125">-AbsoluteUri</span></span>
<span data-ttu-id="334e7-126">A forrásfájl URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="334e7-127">Ha a forrás helyéhez hitelesítő adatokra van szükség, meg kell adnia egyet.</span><span class="sxs-lookup"><span data-stu-id="334e7-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="334e7-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="334e7-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="334e7-129">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="334e7-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="334e7-130">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="334e7-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="334e7-131">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="334e7-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="334e7-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="334e7-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="334e7-133">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="334e7-134">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="334e7-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="334e7-135">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="334e7-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="334e7-136">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="334e7-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="334e7-137">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="334e7-137">The default value is 10.</span></span>

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

### <span data-ttu-id="334e7-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="334e7-138">-Context</span></span>
<span data-ttu-id="334e7-139">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="334e7-140">Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="334e7-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="334e7-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334e7-141">-DefaultProfile</span></span>
<span data-ttu-id="334e7-142">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="334e7-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="334e7-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="334e7-143">-DestContext</span></span>
<span data-ttu-id="334e7-144">A cél Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="334e7-145">Környezet beolvasásához használja az **új AzureStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="334e7-145">To obtain a context, use **New-AzureStorageContext**.</span></span>

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

### <span data-ttu-id="334e7-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="334e7-146">-DestFile</span></span>
<span data-ttu-id="334e7-147">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="334e7-148">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzureStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="334e7-148">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334e7-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="334e7-149">-DestFilePath</span></span>
<span data-ttu-id="334e7-150">A célfájl elérési útját adja meg a cél megosztásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="334e7-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="334e7-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="334e7-151">-DestShareName</span></span>
<span data-ttu-id="334e7-152">A célként megadott megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="334e7-153">-Force</span><span class="sxs-lookup"><span data-stu-id="334e7-153">-Force</span></span>
<span data-ttu-id="334e7-154">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="334e7-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="334e7-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="334e7-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="334e7-156">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="334e7-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="334e7-157">-SrcBlob</span></span>
<span data-ttu-id="334e7-158">Egy **CloudBlob** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="334e7-159">A Get-AzureStorageBlob parancsmag segítségével létrehozhat egy felhőalapú blobot, vagy megadhat egyet.</span><span class="sxs-lookup"><span data-stu-id="334e7-159">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="334e7-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="334e7-160">-SrcBlobName</span></span>
<span data-ttu-id="334e7-161">A forrás blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="334e7-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="334e7-162">-SrcContainer</span></span>
<span data-ttu-id="334e7-163">Egy felhőalapú blob-tároló objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="334e7-164">Létrehozhat felhőalapú blob-tároló objektumot, vagy használhatja az Get-AzureStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="334e7-164">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334e7-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="334e7-165">-SrcContainerName</span></span>
<span data-ttu-id="334e7-166">A forrás tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="334e7-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="334e7-167">-SrcFile</span></span>
<span data-ttu-id="334e7-168">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="334e7-169">Létrehozhat egy felhőalapú fájlt, vagy beszerezhet egyet a **Get-AzureStorageFile** segítségével.</span><span class="sxs-lookup"><span data-stu-id="334e7-169">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="334e7-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="334e7-170">-SrcFilePath</span></span>
<span data-ttu-id="334e7-171">A forrásfájl elérési útvonalát adja meg a forrás vagy a forrás megosztásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="334e7-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="334e7-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="334e7-172">-SrcShare</span></span>
<span data-ttu-id="334e7-173">A felhőalapú fájlmegosztás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="334e7-174">A Get-AzureStorageShare parancsmag segítségével létrehozhatja a felhőalapú fájlokat, vagy megadhat egyet.</span><span class="sxs-lookup"><span data-stu-id="334e7-174">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334e7-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="334e7-175">-SrcShareName</span></span>
<span data-ttu-id="334e7-176">A forrás megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="334e7-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="334e7-177">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="334e7-177">-Confirm</span></span>
<span data-ttu-id="334e7-178">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="334e7-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="334e7-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="334e7-179">-WhatIf</span></span>
<span data-ttu-id="334e7-180">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="334e7-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="334e7-181">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="334e7-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="334e7-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334e7-182">CommonParameters</span></span>
<span data-ttu-id="334e7-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="334e7-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334e7-184">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334e7-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334e7-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="334e7-185">INPUTS</span></span>

### <span data-ttu-id="334e7-186">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="334e7-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="334e7-187">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="334e7-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="334e7-188">Paraméterek: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="334e7-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="334e7-189">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="334e7-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="334e7-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="334e7-190">OUTPUTS</span></span>

### <span data-ttu-id="334e7-191">System. Void</span><span class="sxs-lookup"><span data-stu-id="334e7-191">System.Void</span></span>

## <span data-ttu-id="334e7-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="334e7-192">NOTES</span></span>

## <span data-ttu-id="334e7-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="334e7-193">RELATED LINKS</span></span>

[<span data-ttu-id="334e7-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="334e7-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="334e7-195">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="334e7-195">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="334e7-196">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="334e7-196">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="334e7-197">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="334e7-197">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="334e7-198">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="334e7-198">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="334e7-199">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="334e7-199">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
