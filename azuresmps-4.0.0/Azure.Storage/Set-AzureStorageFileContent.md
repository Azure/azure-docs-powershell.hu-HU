---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd066a57ac63b0126120652750c669e6afde36bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491091"
---
# <span data-ttu-id="d80c9-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d80c9-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="d80c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d80c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d80c9-103">Feltölti a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="d80c9-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="d80c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d80c9-104">SYNTAX</span></span>

### <span data-ttu-id="d80c9-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d80c9-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80c9-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="d80c9-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80c9-107">Directory</span><span class="sxs-lookup"><span data-stu-id="d80c9-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d80c9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d80c9-108">DESCRIPTION</span></span>
<span data-ttu-id="d80c9-109">A **set-AzureStorageFileContent** parancsmag a fájl tartalmát egy megadott megosztásban lévő fájlba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="d80c9-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="d80c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d80c9-110">EXAMPLES</span></span>

### <span data-ttu-id="d80c9-111">1. példa: fájl feltöltése az aktuális mappában</span><span class="sxs-lookup"><span data-stu-id="d80c9-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="d80c9-112">A parancs feltölti a DataFile37 nevű fájlt az aktuális mappában egy CurrentDataFile nevű fájlként a ContosoWorkingFolder nevű mappában.</span><span class="sxs-lookup"><span data-stu-id="d80c9-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="d80c9-113">2. példa: az aktuális mappa összes fájljának feltöltése</span><span class="sxs-lookup"><span data-stu-id="d80c9-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="d80c9-114">Ez a példa számos gyakori Windows PowerShell-parancsmagot és a jelenlegi parancsmagot használ, így az aktuális mappából az összes fájlt feltöltheti a tároló ContosoShare06 gyökérkönyvtárába.</span><span class="sxs-lookup"><span data-stu-id="d80c9-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="d80c9-115">Az első parancs megkapja az aktuális mappa nevét, és a $CurrentFolder változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d80c9-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="d80c9-116">A második parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beszerzéséhez, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d80c9-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d80c9-117">A végleges parancs beolvassa az aktuális mappa tartalmát, és átadja őket az Where-Object parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="d80c9-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d80c9-118">Ez a parancsmag kiszűri a fájlokat nem tartalmazó objektumokat, majd átadja a fájlokat az ForEach-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d80c9-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="d80c9-119">A parancsmag minden olyan fájlhoz parancsfájl-zárolást futtat, amely a megfelelő elérési utat hozza létre, majd az aktuális parancsmagot használja a fájl feltöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="d80c9-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="d80c9-120">Az eredmény ugyanazt a nevet és relatív pozíciót veszi figyelembe az egyéb, a példa által feltöltött fájlokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="d80c9-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="d80c9-121">A parancsfájl-blokkokról a következő témakörben olvashat bővebben: `Get-Help about_Script_Blocks`</span><span class="sxs-lookup"><span data-stu-id="d80c9-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="d80c9-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d80c9-122">PARAMETERS</span></span>

### <span data-ttu-id="d80c9-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d80c9-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d80c9-124">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="d80c9-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d80c9-125">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="d80c9-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d80c9-126">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d80c9-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d80c9-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d80c9-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d80c9-128">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d80c9-129">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d80c9-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d80c9-130">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="d80c9-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d80c9-131">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="d80c9-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d80c9-132">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="d80c9-132">The default value is 10.</span></span>

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

### <span data-ttu-id="d80c9-133">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d80c9-133">-Context</span></span>
<span data-ttu-id="d80c9-134">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d80c9-135">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d80c9-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d80c9-136">-Címtár</span><span class="sxs-lookup"><span data-stu-id="d80c9-136">-Directory</span></span>
<span data-ttu-id="d80c9-137">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="d80c9-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d80c9-138">Ez a parancsmag feltölti a fájlt a paraméter által megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="d80c9-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="d80c9-139">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d80c9-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d80c9-140">A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="d80c9-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="d80c9-141">-Force</span><span class="sxs-lookup"><span data-stu-id="d80c9-141">-Force</span></span>
<span data-ttu-id="d80c9-142">Jelzi, hogy ez a parancsmag felülír egy meglévő Azure-tárterületet.</span><span class="sxs-lookup"><span data-stu-id="d80c9-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c9-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d80c9-143">-PassThru</span></span>
<span data-ttu-id="d80c9-144">Azt jelzi, hogy ez a parancsmag az általa létrehozott vagy feltöltött **AzureStorageFile** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d80c9-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c9-145">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d80c9-145">-Path</span></span>
<span data-ttu-id="d80c9-146">A fájl vagy mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="d80c9-147">Ezzel a parancsmaggal a program feltölti a tartalmat a paraméter által megadott fájlba vagy a paraméter által megadott mappában lévő fájlba.</span><span class="sxs-lookup"><span data-stu-id="d80c9-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="d80c9-148">Ha megad egy mappát, a parancsmag a forrásfájl nevével megegyező nevű fájlt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d80c9-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="d80c9-149">Ha olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat.</span><span class="sxs-lookup"><span data-stu-id="d80c9-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="d80c9-150">Ha olyan fájlt ad meg, amely már létezik, és az _erő_ paramétert adja meg, ez a parancsmag felülírja a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="d80c9-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="d80c9-151">Ha olyan fájlt ad meg, amely már létezik, és nem adja meg az _erő_ lehetőséget, ez a parancsmag nem változtatja meg, és hibát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d80c9-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="d80c9-152">Ha olyan mappa elérési útját adja meg, amely nem létezik, akkor ez a parancsmag nem változtatja meg a hibát, és hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d80c9-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c9-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d80c9-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d80c9-154">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d80c9-155">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="d80c9-155">-Share</span></span>
<span data-ttu-id="d80c9-156">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d80c9-157">Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="d80c9-158">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d80c9-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="d80c9-159">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d80c9-159">This object contains the storage context.</span></span>
<span data-ttu-id="d80c9-160">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d80c9-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="d80c9-161">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="d80c9-161">-ShareName</span></span>
<span data-ttu-id="d80c9-162">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="d80c9-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="d80c9-163">Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="d80c9-164">-Forrás</span><span class="sxs-lookup"><span data-stu-id="d80c9-164">-Source</span></span>
<span data-ttu-id="d80c9-165">A parancsmag által feltöltött forrásfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d80c9-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="d80c9-166">Ha olyan fájlt ad meg, amely nem létezik, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d80c9-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d80c9-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d80c9-167">-Confirm</span></span>
<span data-ttu-id="d80c9-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d80c9-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c9-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80c9-169">-WhatIf</span></span>
<span data-ttu-id="d80c9-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d80c9-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80c9-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d80c9-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80c9-172">CommonParameters</span></span>
<span data-ttu-id="d80c9-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d80c9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80c9-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80c9-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80c9-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d80c9-175">INPUTS</span></span>

## <span data-ttu-id="d80c9-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d80c9-176">OUTPUTS</span></span>

## <span data-ttu-id="d80c9-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d80c9-177">NOTES</span></span>

## <span data-ttu-id="d80c9-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d80c9-178">RELATED LINKS</span></span>

[<span data-ttu-id="d80c9-179">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d80c9-179">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="d80c9-180">Új – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d80c9-180">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="d80c9-181">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d80c9-181">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
