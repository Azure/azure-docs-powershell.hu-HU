---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465905"
---
# <span data-ttu-id="9f6e8-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="9f6e8-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="9f6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6e8-103">Az elérési úthoz szükséges könyvtárakat és fájlokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="9f6e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f6e8-104">SYNTAX</span></span>

### <span data-ttu-id="9f6e8-105">ShareName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f6e8-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9f6e8-106">Megosztás</span><span class="sxs-lookup"><span data-stu-id="9f6e8-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f6e8-107">Címtár</span><span class="sxs-lookup"><span data-stu-id="9f6e8-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f6e8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f6e8-108">DESCRIPTION</span></span>
<span data-ttu-id="9f6e8-109">A **Get-AzStorageFile** parancsmag felsorolja a megadott megosztás vagy címtár címtárát és fájljait.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="9f6e8-110">Adja meg *a Path paramétert,* ha egy címtár vagy fájl adott elérési útba való példányát be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="9f6e8-111">Ez a parancsmag **az AzureStorageFile** és **az AzureStorageDirectory objektumokat adja** vissza.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="9f6e8-112">Az **IsDirectory** tulajdonságot használva különböztetheti meg a mappákat és a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="9f6e8-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f6e8-113">EXAMPLES</span></span>

### <span data-ttu-id="9f6e8-114">1. példa: A megosztásban található könyvtárak felsorolása</span><span class="sxs-lookup"><span data-stu-id="9f6e8-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="9f6e8-115">Ez a parancs csak a contososhare06-os megosztásban található könyvtárakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="9f6e8-116">Először beolvassa a fájlokat és  a könyvtárakat, majd a pipeline operátorral átadja őket a where operátornak, majd elvet minden olyan objektumot, amelynek a típusa nem "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="9f6e8-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="9f6e8-117">2. példa: Fájlkönyvtárak felsorolása</span><span class="sxs-lookup"><span data-stu-id="9f6e8-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="9f6e8-118">Ez a parancs felsorolja a ContosoWorkingFolder címtárban lévő fájlokat és mappákat a ContosoShare06 megosztás alatt.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="9f6e8-119">Először begyűjte a címtárpéldányt, majd a **Get-AzStorageFile** parancsmagba befuttatva felsorolja a címtárat.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="9f6e8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f6e8-120">PARAMETERS</span></span>

### <span data-ttu-id="9f6e8-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f6e8-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9f6e8-122">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9f6e8-123">Ha az előző hívás a megadott időszakon belül meghiúsul, ez a parancsmag újraüteme a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9f6e8-124">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9f6e8-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9f6e8-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9f6e8-126">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9f6e8-127">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9f6e8-128">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9f6e8-129">Ezzel a paraméterrel csökkenthetők a hálózati kapcsolattal kapcsolatos problémák alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9f6e8-130">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-130">The default value is 10.</span></span>

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

### <span data-ttu-id="9f6e8-131">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9f6e8-131">-Context</span></span>
<span data-ttu-id="9f6e8-132">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9f6e8-133">Tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9f6e8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6e8-134">-DefaultProfile</span></span>
<span data-ttu-id="9f6e8-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f6e8-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="9f6e8-136">-Directory</span></span>
<span data-ttu-id="9f6e8-137">Mappát ad meg **CloudFileDirectory objektumként.**</span><span class="sxs-lookup"><span data-stu-id="9f6e8-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9f6e8-138">Ez a parancsmag a paraméter által megadott mappát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="9f6e8-139">Címtár beszerzéséhez használja a New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="9f6e8-140">Könyvtár beszerzéséhez használhatja a **Get-AzStorageFile** parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="9f6e8-141">-Path</span><span class="sxs-lookup"><span data-stu-id="9f6e8-141">-Path</span></span>
<span data-ttu-id="9f6e8-142">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="9f6e8-143">Ha nem adja meg a *Path* paramétert, a **Get-AzStorageFile** a megadott fájlmegosztásban vagy -címtárban lévő könyvtárakat és fájlokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="9f6e8-144">Ha tartalmazza a *Path* paramétert, akkor a **Get-AzStorageFile** egy címtár vagy fájl adott példányát adja vissza a megadott elérési útban.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6e8-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f6e8-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9f6e8-146">Egy kérés szolgáltatásoldali időkorlát-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="9f6e8-147">Ha a megadott időtartam eltelik, mielőtt a szolgáltatás feldolgozná a kérelmet, a Társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="9f6e8-148">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="9f6e8-148">-Share</span></span>
<span data-ttu-id="9f6e8-149">Egy **CloudFileShare-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9f6e8-150">Ez a parancsmag a paraméter által megadott fájlmegosztásból kap egy fájlt vagy címtárat.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="9f6e8-151">**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="9f6e8-152">Ez az objektum a Tárterület környezett tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-152">This object contains the Storage context.</span></span>
<span data-ttu-id="9f6e8-153">Ha ezt a paramétert adja meg, ne adja meg a környezet *paramétert.*</span><span class="sxs-lookup"><span data-stu-id="9f6e8-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9f6e8-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9f6e8-154">-ShareName</span></span>
<span data-ttu-id="9f6e8-155">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="9f6e8-156">Ez a parancsmag a paraméter által megadott fájlmegosztásból kap egy fájlt vagy címtárat.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f6e8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6e8-157">CommonParameters</span></span>
<span data-ttu-id="9f6e8-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6e8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6e8-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6e8-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6e8-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f6e8-160">INPUTS</span></span>

### <span data-ttu-id="9f6e8-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9f6e8-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9f6e8-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9f6e8-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9f6e8-163">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9f6e8-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9f6e8-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f6e8-164">OUTPUTS</span></span>

### <span data-ttu-id="9f6e8-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="9f6e8-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="9f6e8-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f6e8-166">NOTES</span></span>

## <span data-ttu-id="9f6e8-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f6e8-167">RELATED LINKS</span></span>

[<span data-ttu-id="9f6e8-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9f6e8-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="9f6e8-169">New-AzstorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9f6e8-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="9f6e8-170">Remove-AzstorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9f6e8-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="9f6e8-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="9f6e8-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="9f6e8-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9f6e8-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


