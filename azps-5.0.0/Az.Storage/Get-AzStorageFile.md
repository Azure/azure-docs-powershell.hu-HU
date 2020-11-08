---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186174"
---
# <span data-ttu-id="011ae-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="011ae-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="011ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="011ae-102">SYNOPSIS</span></span>
<span data-ttu-id="011ae-103">Az elérési utakhoz tartozó könyvtárak és fájlok felsorolása.</span><span class="sxs-lookup"><span data-stu-id="011ae-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="011ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="011ae-104">SYNTAX</span></span>

### <span data-ttu-id="011ae-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="011ae-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="011ae-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="011ae-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="011ae-107">Directory</span><span class="sxs-lookup"><span data-stu-id="011ae-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="011ae-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="011ae-108">DESCRIPTION</span></span>
<span data-ttu-id="011ae-109">A **Get-AzStorageFile** parancsmag a megadott megosztás vagy könyvtár könyvtárait és fájljait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="011ae-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="011ae-110">Adja meg az *elérésiút* -paramétert, hogy egy adott könyvtár vagy fájl példányát beolvassa a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="011ae-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="011ae-111">Ez a parancsmag **AzureStorageFile** -és **AzureStorageDirectory** -objektumokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="011ae-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="011ae-112">A **IsDirectory** tulajdonsággal megkülönböztetheti a mappákat és a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="011ae-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="011ae-113">Példák</span><span class="sxs-lookup"><span data-stu-id="011ae-113">EXAMPLES</span></span>

### <span data-ttu-id="011ae-114">Példa 1: megosztásban lévő könyvtárak listázása</span><span class="sxs-lookup"><span data-stu-id="011ae-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="011ae-115">Ez a parancs csak a megosztás ContosoShare06 lévő könyvtárakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="011ae-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="011ae-116">Először a fájlok és könyvtárak beolvasása után átadja őket a **Where** operátornak a pipeline operátor segítségével, majd elveti azokat az objektumokat, amelyeknek a típusa nem "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="011ae-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="011ae-117">2. példa: egy fájl címtárának listázása</span><span class="sxs-lookup"><span data-stu-id="011ae-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="011ae-118">Ez a parancs felsorolja a címtár ContosoWorkingFolder a megosztás ContosoShare06 csoportban található fájlokat és mappákat.</span><span class="sxs-lookup"><span data-stu-id="011ae-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="011ae-119">Először megkapja a címtár-példányt, majd a " **Get-AzStorageFile** parancsmag" értékre helyezi a címtár listáját.</span><span class="sxs-lookup"><span data-stu-id="011ae-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="011ae-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="011ae-120">PARAMETERS</span></span>

### <span data-ttu-id="011ae-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="011ae-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="011ae-122">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="011ae-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="011ae-123">Ha az előző hívás nem sikerült a megadott intervallumon belül, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="011ae-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="011ae-124">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="011ae-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="011ae-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="011ae-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="011ae-126">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="011ae-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="011ae-127">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="011ae-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="011ae-128">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="011ae-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="011ae-129">Ez a paraméter csökkentheti a hálózati kapcsolat problémáinak enyhítését az alacsony sávszélességű környezetekben, például 100 kilobit/másodperc.</span><span class="sxs-lookup"><span data-stu-id="011ae-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="011ae-130">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="011ae-130">The default value is 10.</span></span>

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

### <span data-ttu-id="011ae-131">-Környezet</span><span class="sxs-lookup"><span data-stu-id="011ae-131">-Context</span></span>
<span data-ttu-id="011ae-132">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="011ae-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="011ae-133">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="011ae-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="011ae-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011ae-134">-DefaultProfile</span></span>
<span data-ttu-id="011ae-135">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="011ae-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="011ae-136">-Címtár</span><span class="sxs-lookup"><span data-stu-id="011ae-136">-Directory</span></span>
<span data-ttu-id="011ae-137">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="011ae-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="011ae-138">Ez a parancsmag a paraméter által megadott mappát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="011ae-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="011ae-139">Címtár beolvasásához használja az New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="011ae-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="011ae-140">A **Get-AzStorageFile** parancsmag használatával is beszerezhet egy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="011ae-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="011ae-141">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="011ae-141">-Path</span></span>
<span data-ttu-id="011ae-142">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="011ae-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="011ae-143">Ha kihagyja a *path* paramétert, a **Get-AzStorageFile** felsorolja a megadott fájlmegosztás vagy címtárban lévő könyvtárakat és fájlokat.</span><span class="sxs-lookup"><span data-stu-id="011ae-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="011ae-144">Ha a *path* paramétert adja meg, a **Get-AzStorageFile** a megadott elérési úton lévő könyvtár vagy fájl példányát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="011ae-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="011ae-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="011ae-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="011ae-146">A szolgáltatás-időkorlátot adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="011ae-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="011ae-147">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="011ae-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="011ae-148">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="011ae-148">-Share</span></span>
<span data-ttu-id="011ae-149">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="011ae-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="011ae-150">Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="011ae-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="011ae-151">**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="011ae-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="011ae-152">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="011ae-152">This object contains the Storage context.</span></span>
<span data-ttu-id="011ae-153">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="011ae-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="011ae-154">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="011ae-154">-ShareName</span></span>
<span data-ttu-id="011ae-155">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="011ae-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="011ae-156">Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="011ae-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="011ae-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011ae-157">CommonParameters</span></span>
<span data-ttu-id="011ae-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="011ae-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011ae-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="011ae-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011ae-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="011ae-160">INPUTS</span></span>

### <span data-ttu-id="011ae-161">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="011ae-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="011ae-162">Microsoft. Azure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="011ae-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="011ae-163">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="011ae-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="011ae-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="011ae-164">OUTPUTS</span></span>

### <span data-ttu-id="011ae-165">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="011ae-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="011ae-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="011ae-166">NOTES</span></span>

## <span data-ttu-id="011ae-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="011ae-167">RELATED LINKS</span></span>

[<span data-ttu-id="011ae-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="011ae-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="011ae-169">Új – AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="011ae-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="011ae-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="011ae-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="011ae-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="011ae-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="011ae-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="011ae-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


