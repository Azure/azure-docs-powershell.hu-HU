---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: b56875f1afd30a1861365c8134e4567c9a229a4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501007"
---
# <span data-ttu-id="637bc-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="637bc-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="637bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="637bc-102">SYNOPSIS</span></span>
<span data-ttu-id="637bc-103">Az elérési utakhoz tartozó könyvtárak és fájlok felsorolása.</span><span class="sxs-lookup"><span data-stu-id="637bc-103">Lists directories and files for a path.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="637bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="637bc-104">SYNTAX</span></span>

### <span data-ttu-id="637bc-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="637bc-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="637bc-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="637bc-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="637bc-107">Directory</span><span class="sxs-lookup"><span data-stu-id="637bc-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="637bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="637bc-108">DESCRIPTION</span></span>
<span data-ttu-id="637bc-109">A **Get-AzureStorageFile** parancsmag a megadott megosztás vagy könyvtár könyvtárait és fájljait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="637bc-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="637bc-110">Adja meg az *elérésiút* -paramétert, hogy egy adott könyvtár vagy fájl példányát beolvassa a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="637bc-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="637bc-111">Ez a parancsmag **AzureStorageFile** -és **AzureStorageDirectory** -objektumokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="637bc-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="637bc-112">A **IsDirectory** tulajdonsággal megkülönböztetheti a mappákat és a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="637bc-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="637bc-113">Példák</span><span class="sxs-lookup"><span data-stu-id="637bc-113">EXAMPLES</span></span>

### <span data-ttu-id="637bc-114">Példa 1: megosztásban lévő könyvtárak listázása</span><span class="sxs-lookup"><span data-stu-id="637bc-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="637bc-115">Ez a parancs csak a megosztás ContosoShare06 lévő könyvtárakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="637bc-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="637bc-116">Először a fájlok és könyvtárak beolvasása után átadja őket a **Where** operátornak a pipeline operátor segítségével, majd elveti azokat az objektumokat, amelyeknek a típusa nem "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="637bc-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="637bc-117">2. példa: egy fájl címtárának listázása</span><span class="sxs-lookup"><span data-stu-id="637bc-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="637bc-118">Ez a parancs felsorolja a címtár ContosoWorkingFolder a megosztás ContosoShare06 csoportban található fájlokat és mappákat.</span><span class="sxs-lookup"><span data-stu-id="637bc-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="637bc-119">Először megkapja a címtár-példányt, majd a " **Get-AzureStorageFile** parancsmag" értékre helyezi a címtár listáját.</span><span class="sxs-lookup"><span data-stu-id="637bc-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="637bc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="637bc-120">PARAMETERS</span></span>

### <span data-ttu-id="637bc-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="637bc-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="637bc-122">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="637bc-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="637bc-123">Ha az előző hívás nem sikerült a megadott intervallumon belül, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="637bc-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="637bc-124">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="637bc-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="637bc-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="637bc-126">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="637bc-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="637bc-127">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="637bc-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="637bc-128">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="637bc-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="637bc-129">Ez a paraméter csökkentheti a hálózati kapcsolat problémáinak enyhítését az alacsony sávszélességű környezetekben, például 100 kilobit/másodperc.</span><span class="sxs-lookup"><span data-stu-id="637bc-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="637bc-130">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="637bc-130">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-131">-Környezet</span><span class="sxs-lookup"><span data-stu-id="637bc-131">-Context</span></span>
<span data-ttu-id="637bc-132">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="637bc-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="637bc-133">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="637bc-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-134">-Címtár</span><span class="sxs-lookup"><span data-stu-id="637bc-134">-Directory</span></span>
<span data-ttu-id="637bc-135">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="637bc-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="637bc-136">Ez a parancsmag a paraméter által megadott mappát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="637bc-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="637bc-137">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="637bc-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="637bc-138">A **Get-AzureStorageFile** parancsmag használatával is beszerezhet egy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="637bc-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-139">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="637bc-139">-Path</span></span>
<span data-ttu-id="637bc-140">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="637bc-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="637bc-141">Ha kihagyja a *path* paramétert, a **Get-AzureStorageFile** felsorolja a megadott fájlmegosztás vagy címtárban lévő könyvtárakat és fájlokat.</span><span class="sxs-lookup"><span data-stu-id="637bc-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="637bc-142">Ha a *path* paramétert adja meg, a **Get-AzureStorageFile** a megadott elérési úton lévő könyvtár vagy fájl példányát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="637bc-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="637bc-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="637bc-144">A szolgáltatás-időkorlátot adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="637bc-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="637bc-145">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="637bc-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-146">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="637bc-146">-Share</span></span>
<span data-ttu-id="637bc-147">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="637bc-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="637bc-148">Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="637bc-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="637bc-149">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="637bc-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="637bc-150">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="637bc-150">This object contains the Storage context.</span></span>
<span data-ttu-id="637bc-151">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="637bc-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-152">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="637bc-152">-ShareName</span></span>
<span data-ttu-id="637bc-153">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="637bc-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="637bc-154">Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="637bc-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637bc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637bc-155">CommonParameters</span></span>
<span data-ttu-id="637bc-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="637bc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637bc-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="637bc-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637bc-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="637bc-158">INPUTS</span></span>

### <span data-ttu-id="637bc-159">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="637bc-159">IStorageContext</span></span>

<span data-ttu-id="637bc-160">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="637bc-160">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="637bc-161">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="637bc-161">CloudFileDirectory</span></span>

<span data-ttu-id="637bc-162">A "címtár" paraméter elfogadja a "CloudFileDirectory" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="637bc-162">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="637bc-163">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="637bc-163">CloudFileShare</span></span>

<span data-ttu-id="637bc-164">A "share" paraméter értéke "CloudFileShare" típusú értéket ad a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="637bc-164">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="637bc-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="637bc-165">OUTPUTS</span></span>

## <span data-ttu-id="637bc-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="637bc-166">NOTES</span></span>

## <span data-ttu-id="637bc-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="637bc-167">RELATED LINKS</span></span>

[<span data-ttu-id="637bc-168">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="637bc-168">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="637bc-169">Új – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="637bc-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="637bc-170">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="637bc-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="637bc-171">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="637bc-171">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="637bc-172">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="637bc-172">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


