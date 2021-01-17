---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 84f6ae7f80eb7af3c4fccad08b0d9d2a20b0caeb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469254"
---
# <span data-ttu-id="0d853-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0d853-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="0d853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d853-102">SYNOPSIS</span></span>
<span data-ttu-id="0d853-103">Címtárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0d853-103">Creates a directory.</span></span>

## <span data-ttu-id="0d853-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d853-104">SYNTAX</span></span>

### <span data-ttu-id="0d853-105">ShareName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d853-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0d853-106">Megosztás</span><span class="sxs-lookup"><span data-stu-id="0d853-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d853-107">Címtár</span><span class="sxs-lookup"><span data-stu-id="0d853-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d853-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d853-108">DESCRIPTION</span></span>
<span data-ttu-id="0d853-109">A **New-AzStorageDirectory** parancsmag létrehoz egy címtárat.</span><span class="sxs-lookup"><span data-stu-id="0d853-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="0d853-110">Ez a parancsmag **egy CloudFileDirectory objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="0d853-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="0d853-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d853-111">EXAMPLES</span></span>

### <span data-ttu-id="0d853-112">1. példa: Mappa létrehozása fájlmegosztásban</span><span class="sxs-lookup"><span data-stu-id="0d853-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="0d853-113">Ez a parancs létrehoz egy ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztásban.</span><span class="sxs-lookup"><span data-stu-id="0d853-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="0d853-114">2. példa: Mappa létrehozása egy fájlmegosztási objektumban megadott fájlmegosztásban</span><span class="sxs-lookup"><span data-stu-id="0d853-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="0d853-115">Ez a parancs **a Get-AzStorageShare** parancsmagot használva lekérte a ContosoShare06 nevű fájlmegosztást, majd a folyamat műveleti operátorával átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="0d853-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d853-116">Az aktuális parancsmag létrehozza a ContosoWorkingFolder nevű mappát a ContosoShare06-ban.</span><span class="sxs-lookup"><span data-stu-id="0d853-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="0d853-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d853-117">PARAMETERS</span></span>

### <span data-ttu-id="0d853-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0d853-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0d853-119">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="0d853-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0d853-120">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="0d853-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0d853-121">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="0d853-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0d853-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0d853-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0d853-123">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="0d853-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0d853-124">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="0d853-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0d853-125">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="0d853-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0d853-126">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="0d853-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0d853-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0d853-127">The default value is 10.</span></span>

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

### <span data-ttu-id="0d853-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0d853-128">-Context</span></span>
<span data-ttu-id="0d853-129">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d853-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0d853-130">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="0d853-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0d853-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d853-131">-DefaultProfile</span></span>
<span data-ttu-id="0d853-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d853-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d853-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="0d853-133">-Directory</span></span>
<span data-ttu-id="0d853-134">Mappát ad meg **CloudFileDirectory objektumként.**</span><span class="sxs-lookup"><span data-stu-id="0d853-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="0d853-135">Ez a parancsmag a paraméter által megadott helyen hozza létre a mappát.</span><span class="sxs-lookup"><span data-stu-id="0d853-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="0d853-136">Címtár beszerzéséhez használja a New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0d853-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="0d853-137">Címtár beszerzéséhez használhatja Get-AzStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="0d853-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="0d853-138">-Path</span><span class="sxs-lookup"><span data-stu-id="0d853-138">-Path</span></span>
<span data-ttu-id="0d853-139">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d853-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="0d853-140">Ez a parancsmag létrehoz egy mappát a parancsmag által megadott elérési úthoz.</span><span class="sxs-lookup"><span data-stu-id="0d853-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d853-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0d853-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0d853-142">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d853-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0d853-143">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="0d853-143">-Share</span></span>
<span data-ttu-id="0d853-144">Egy **CloudFileShare-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="0d853-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="0d853-145">Ez a parancsmag létrehoz egy mappát a paraméter által megadott fájlmegosztásban.</span><span class="sxs-lookup"><span data-stu-id="0d853-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="0d853-146">**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0d853-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="0d853-147">Ez az objektum tartalmazza a tárterület környezetét.</span><span class="sxs-lookup"><span data-stu-id="0d853-147">This object contains the storage context.</span></span>
<span data-ttu-id="0d853-148">Ha ezt a paramétert adja meg, ne adja meg a környezet *paramétert.*</span><span class="sxs-lookup"><span data-stu-id="0d853-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="0d853-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0d853-149">-ShareName</span></span>
<span data-ttu-id="0d853-150">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d853-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="0d853-151">Ez a parancsmag létrehoz egy mappát a paraméter által megadott fájlmegosztásban.</span><span class="sxs-lookup"><span data-stu-id="0d853-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="0d853-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d853-152">CommonParameters</span></span>
<span data-ttu-id="0d853-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d853-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d853-154">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d853-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d853-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d853-155">INPUTS</span></span>

### <span data-ttu-id="0d853-156">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0d853-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="0d853-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0d853-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="0d853-158">System.String</span><span class="sxs-lookup"><span data-stu-id="0d853-158">System.String</span></span>

### <span data-ttu-id="0d853-159">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0d853-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0d853-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d853-160">OUTPUTS</span></span>

### <span data-ttu-id="0d853-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0d853-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="0d853-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d853-162">NOTES</span></span>

## <span data-ttu-id="0d853-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d853-163">RELATED LINKS</span></span>

[<span data-ttu-id="0d853-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="0d853-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="0d853-165">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="0d853-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="0d853-166">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="0d853-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0d853-167">New-AzstorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0d853-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="0d853-168">Remove-AzstorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0d853-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
