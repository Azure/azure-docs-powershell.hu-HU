---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181253"
---
# <span data-ttu-id="26314-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="26314-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="26314-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26314-102">SYNOPSIS</span></span>
<span data-ttu-id="26314-103">Elindítja a forrásfájl másolását.</span><span class="sxs-lookup"><span data-stu-id="26314-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="26314-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26314-104">SYNTAX</span></span>

### <span data-ttu-id="26314-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="26314-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26314-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="26314-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26314-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="26314-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26314-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="26314-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26314-109">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="26314-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26314-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="26314-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26314-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="26314-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26314-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="26314-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26314-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="26314-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26314-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="26314-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26314-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="26314-115">DESCRIPTION</span></span>
<span data-ttu-id="26314-116">A **Start-AzStorageFileCopy** parancsmag a forrásfájl szövegfájlba való másolását kezdi.</span><span class="sxs-lookup"><span data-stu-id="26314-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="26314-117">Példák</span><span class="sxs-lookup"><span data-stu-id="26314-117">EXAMPLES</span></span>

### <span data-ttu-id="26314-118">1. példa: a másolási művelet indítása fájlból fájlból fájlból a megosztás név és fájlnév használatával</span><span class="sxs-lookup"><span data-stu-id="26314-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="26314-119">Ez a parancs a fájlból fájlból másolt műveletet indítja el.</span><span class="sxs-lookup"><span data-stu-id="26314-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="26314-120">A parancs a megosztás neve és a fájlnév nevet adja meg</span><span class="sxs-lookup"><span data-stu-id="26314-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="26314-121">2. példa: a másolási művelet indítása blobról fájlra a tároló neve és a blob neve segítségével</span><span class="sxs-lookup"><span data-stu-id="26314-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="26314-122">Ez a parancs egy másolati műveletet indít el a blob-fájlból.</span><span class="sxs-lookup"><span data-stu-id="26314-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="26314-123">A parancs a tároló nevét és a blob nevét adja meg</span><span class="sxs-lookup"><span data-stu-id="26314-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="26314-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26314-124">PARAMETERS</span></span>

### <span data-ttu-id="26314-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="26314-125">-AbsoluteUri</span></span>
<span data-ttu-id="26314-126">A forrásfájl URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="26314-127">Ha a forrás helyéhez hitelesítő adatokra van szükség, meg kell adnia egyet.</span><span class="sxs-lookup"><span data-stu-id="26314-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="26314-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26314-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="26314-129">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="26314-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="26314-130">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="26314-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="26314-131">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="26314-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="26314-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="26314-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="26314-133">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="26314-134">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="26314-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="26314-135">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="26314-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="26314-136">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="26314-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="26314-137">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="26314-137">The default value is 10.</span></span>

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

### <span data-ttu-id="26314-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="26314-138">-Context</span></span>
<span data-ttu-id="26314-139">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="26314-140">Környezet beolvasásához használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="26314-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="26314-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26314-141">-DefaultProfile</span></span>
<span data-ttu-id="26314-142">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26314-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26314-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="26314-143">-DestContext</span></span>
<span data-ttu-id="26314-144">A cél Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="26314-145">Környezet beolvasásához használja az **új AzStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="26314-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="26314-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="26314-146">-DestFile</span></span>
<span data-ttu-id="26314-147">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="26314-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="26314-148">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="26314-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="26314-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="26314-149">-DestFilePath</span></span>
<span data-ttu-id="26314-150">A célfájl elérési útját adja meg a cél megosztásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="26314-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="26314-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="26314-151">-DestShareName</span></span>
<span data-ttu-id="26314-152">A célként megadott megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="26314-153">-Force</span><span class="sxs-lookup"><span data-stu-id="26314-153">-Force</span></span>
<span data-ttu-id="26314-154">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="26314-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26314-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26314-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="26314-156">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="26314-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="26314-157">-SrcBlob</span></span>
<span data-ttu-id="26314-158">Egy **CloudBlob** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="26314-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="26314-159">A Get-AzStorageBlob parancsmag segítségével létrehozhat egy felhőalapú blobot, vagy megadhat egyet.</span><span class="sxs-lookup"><span data-stu-id="26314-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="26314-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="26314-160">-SrcBlobName</span></span>
<span data-ttu-id="26314-161">A forrás blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="26314-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="26314-162">-SrcContainer</span></span>
<span data-ttu-id="26314-163">Egy felhőalapú blob-tároló objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="26314-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="26314-164">Létrehozhat felhőalapú blob-tároló objektumot, vagy használhatja az Get-AzStorageContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="26314-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="26314-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="26314-165">-SrcContainerName</span></span>
<span data-ttu-id="26314-166">A forrás tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="26314-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="26314-167">-SrcFile</span></span>
<span data-ttu-id="26314-168">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="26314-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="26314-169">Létrehozhat egy felhőalapú fájlt, vagy beszerezhet egyet a **Get-AzStorageFile** segítségével.</span><span class="sxs-lookup"><span data-stu-id="26314-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

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

### <span data-ttu-id="26314-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="26314-170">-SrcFilePath</span></span>
<span data-ttu-id="26314-171">A forrásfájl elérési útvonalát adja meg a forrás vagy a forrás megosztásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="26314-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="26314-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="26314-172">-SrcShare</span></span>
<span data-ttu-id="26314-173">A felhőalapú fájlmegosztás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="26314-174">A Get-AzStorageShare parancsmag segítségével létrehozhatja a felhőalapú fájlokat, vagy megadhat egyet.</span><span class="sxs-lookup"><span data-stu-id="26314-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="26314-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="26314-175">-SrcShareName</span></span>
<span data-ttu-id="26314-176">A forrás megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26314-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="26314-177">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26314-177">-Confirm</span></span>
<span data-ttu-id="26314-178">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26314-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26314-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26314-179">-WhatIf</span></span>
<span data-ttu-id="26314-180">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26314-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26314-181">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26314-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26314-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26314-182">CommonParameters</span></span>
<span data-ttu-id="26314-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26314-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26314-184">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26314-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26314-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26314-185">INPUTS</span></span>

### <span data-ttu-id="26314-186">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="26314-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="26314-187">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="26314-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="26314-188">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="26314-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="26314-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26314-189">OUTPUTS</span></span>

### <span data-ttu-id="26314-190">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="26314-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="26314-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26314-191">NOTES</span></span>

## <span data-ttu-id="26314-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26314-192">RELATED LINKS</span></span>

[<span data-ttu-id="26314-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="26314-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="26314-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="26314-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="26314-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="26314-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="26314-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="26314-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="26314-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="26314-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="26314-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="26314-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
