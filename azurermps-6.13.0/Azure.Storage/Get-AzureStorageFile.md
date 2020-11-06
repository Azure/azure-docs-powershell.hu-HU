---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
ms.openlocfilehash: 5f1834eb603c5023ee49722ee0d7772af40f821c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495211"
---
# <span data-ttu-id="8c450-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8c450-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="8c450-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c450-102">SYNOPSIS</span></span>
<span data-ttu-id="8c450-103">Az elérési utakhoz tartozó könyvtárak és fájlok felsorolása.</span><span class="sxs-lookup"><span data-stu-id="8c450-103">Lists directories and files for a path.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c450-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c450-104">SYNTAX</span></span>

### <span data-ttu-id="8c450-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c450-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8c450-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="8c450-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c450-107">Directory</span><span class="sxs-lookup"><span data-stu-id="8c450-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c450-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c450-108">DESCRIPTION</span></span>
<span data-ttu-id="8c450-109">A **Get-AzureStorageFile** parancsmag a megadott megosztás vagy könyvtár könyvtárait és fájljait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8c450-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="8c450-110">Adja meg az *elérésiút* -paramétert, hogy egy adott könyvtár vagy fájl példányát beolvassa a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="8c450-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="8c450-111">Ez a parancsmag **AzureStorageFile** -és **AzureStorageDirectory** -objektumokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="8c450-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="8c450-112">A **IsDirectory** tulajdonsággal megkülönböztetheti a mappákat és a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="8c450-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="8c450-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8c450-113">EXAMPLES</span></span>

### <span data-ttu-id="8c450-114">Példa 1: megosztásban lévő könyvtárak listázása</span><span class="sxs-lookup"><span data-stu-id="8c450-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="8c450-115">Ez a parancs csak a megosztás ContosoShare06 lévő könyvtárakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8c450-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="8c450-116">Először a fájlok és könyvtárak beolvasása után átadja őket a **Where** operátornak a pipeline operátor segítségével, majd elveti azokat az objektumokat, amelyeknek a típusa nem "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="8c450-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="8c450-117">2. példa: egy fájl címtárának listázása</span><span class="sxs-lookup"><span data-stu-id="8c450-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="8c450-118">Ez a parancs felsorolja a címtár ContosoWorkingFolder a megosztás ContosoShare06 csoportban található fájlokat és mappákat.</span><span class="sxs-lookup"><span data-stu-id="8c450-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="8c450-119">Először megkapja a címtár-példányt, majd a " **Get-AzureStorageFile** parancsmag" értékre helyezi a címtár listáját.</span><span class="sxs-lookup"><span data-stu-id="8c450-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="8c450-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c450-120">PARAMETERS</span></span>

### <span data-ttu-id="8c450-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8c450-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8c450-122">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="8c450-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8c450-123">Ha az előző hívás nem sikerült a megadott intervallumon belül, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="8c450-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8c450-124">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="8c450-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8c450-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8c450-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8c450-126">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c450-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8c450-127">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="8c450-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8c450-128">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="8c450-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8c450-129">Ez a paraméter csökkentheti a hálózati kapcsolat problémáinak enyhítését az alacsony sávszélességű környezetekben, például 100 kilobit/másodperc.</span><span class="sxs-lookup"><span data-stu-id="8c450-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8c450-130">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8c450-130">The default value is 10.</span></span>

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

### <span data-ttu-id="8c450-131">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8c450-131">-Context</span></span>
<span data-ttu-id="8c450-132">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c450-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="8c450-133">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8c450-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8c450-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c450-134">-DefaultProfile</span></span>
<span data-ttu-id="8c450-135">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c450-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c450-136">-Címtár</span><span class="sxs-lookup"><span data-stu-id="8c450-136">-Directory</span></span>
<span data-ttu-id="8c450-137">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="8c450-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="8c450-138">Ez a parancsmag a paraméter által megadott mappát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8c450-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="8c450-139">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8c450-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="8c450-140">A **Get-AzureStorageFile** parancsmag használatával is beszerezhet egy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="8c450-140">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c450-141">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8c450-141">-Path</span></span>
<span data-ttu-id="8c450-142">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c450-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="8c450-143">Ha kihagyja a *path* paramétert, a **Get-AzureStorageFile** felsorolja a megadott fájlmegosztás vagy címtárban lévő könyvtárakat és fájlokat.</span><span class="sxs-lookup"><span data-stu-id="8c450-143">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="8c450-144">Ha a *path* paramétert adja meg, a **Get-AzureStorageFile** a megadott elérési úton lévő könyvtár vagy fájl példányát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8c450-144">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="8c450-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8c450-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8c450-146">A szolgáltatás-időkorlátot adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="8c450-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="8c450-147">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="8c450-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="8c450-148">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="8c450-148">-Share</span></span>
<span data-ttu-id="8c450-149">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8c450-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="8c450-150">Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c450-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="8c450-151">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8c450-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="8c450-152">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8c450-152">This object contains the Storage context.</span></span>
<span data-ttu-id="8c450-153">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8c450-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c450-154">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="8c450-154">-ShareName</span></span>
<span data-ttu-id="8c450-155">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="8c450-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="8c450-156">Ez a parancsmag olyan fájlt vagy könyvtárat ad meg a fájl megosztási mappából, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c450-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c450-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c450-157">CommonParameters</span></span>
<span data-ttu-id="8c450-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c450-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c450-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c450-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c450-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c450-160">INPUTS</span></span>

### <span data-ttu-id="8c450-161">Microsoft. WindowsAzure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8c450-161">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="8c450-162">Paraméterek: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c450-162">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="8c450-163">Microsoft. WindowsAzure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8c450-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="8c450-164">Paraméterek: címtár (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c450-164">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="8c450-165">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c450-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8c450-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c450-166">OUTPUTS</span></span>

### <span data-ttu-id="8c450-167">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="8c450-167">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="8c450-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c450-168">NOTES</span></span>

## <span data-ttu-id="8c450-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c450-169">RELATED LINKS</span></span>

[<span data-ttu-id="8c450-170">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8c450-170">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="8c450-171">Új – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8c450-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="8c450-172">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8c450-172">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="8c450-173">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8c450-173">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="8c450-174">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8c450-174">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


