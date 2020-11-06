---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 84192a4715087d5ae896067e02ab07ef27574410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492100"
---
# <span data-ttu-id="7b134-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7b134-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="7b134-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b134-102">SYNOPSIS</span></span>
<span data-ttu-id="7b134-103">Feltölti a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="7b134-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b134-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b134-104">SYNTAX</span></span>

### <span data-ttu-id="7b134-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b134-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b134-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="7b134-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b134-107">Directory</span><span class="sxs-lookup"><span data-stu-id="7b134-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b134-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b134-108">DESCRIPTION</span></span>
<span data-ttu-id="7b134-109">A **set-AzureStorageFileContent** parancsmag a fájl tartalmát egy megadott megosztásban lévő fájlba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="7b134-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="7b134-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7b134-110">EXAMPLES</span></span>

### <span data-ttu-id="7b134-111">1. példa: fájl feltöltése az aktuális mappában</span><span class="sxs-lookup"><span data-stu-id="7b134-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="7b134-112">A parancs feltölti a DataFile37 nevű fájlt az aktuális mappában egy CurrentDataFile nevű fájlként a ContosoWorkingFolder nevű mappában.</span><span class="sxs-lookup"><span data-stu-id="7b134-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="7b134-113">2. példa: az aktuális mappa összes fájljának feltöltése</span><span class="sxs-lookup"><span data-stu-id="7b134-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="7b134-114">Ez a példa számos gyakori Windows PowerShell-parancsmagot és a jelenlegi parancsmagot használ, így az aktuális mappából az összes fájlt feltöltheti a tároló ContosoShare06 gyökérkönyvtárába.</span><span class="sxs-lookup"><span data-stu-id="7b134-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="7b134-115">Az első parancs megkapja az aktuális mappa nevét, és a $CurrentFolder változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7b134-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="7b134-116">A második parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beszerzéséhez, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7b134-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7b134-117">A végleges parancs beolvassa az aktuális mappa tartalmát, és átadja őket az Where-Object parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="7b134-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b134-118">Ez a parancsmag kiszűri a fájlokat nem tartalmazó objektumokat, majd átadja a fájlokat az ForEach-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="7b134-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="7b134-119">A parancsmag minden olyan fájlhoz parancsfájl-zárolást futtat, amely a megfelelő elérési utat hozza létre, majd az aktuális parancsmagot használja a fájl feltöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="7b134-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="7b134-120">Az eredmény ugyanazt a nevet és relatív pozíciót veszi figyelembe az egyéb, a példa által feltöltött fájlokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="7b134-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="7b134-121">A parancsfájl-blokkokról a következő témakörben olvashat bővebben: `Get-Help about_Script_Blocks`</span><span class="sxs-lookup"><span data-stu-id="7b134-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="7b134-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b134-122">PARAMETERS</span></span>

### <span data-ttu-id="7b134-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7b134-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7b134-124">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="7b134-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7b134-125">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="7b134-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7b134-126">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7b134-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7b134-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7b134-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7b134-128">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7b134-129">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="7b134-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7b134-130">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="7b134-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7b134-131">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="7b134-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7b134-132">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7b134-132">The default value is 10.</span></span>

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

### <span data-ttu-id="7b134-133">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7b134-133">-Context</span></span>
<span data-ttu-id="7b134-134">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7b134-135">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7b134-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7b134-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b134-136">-DefaultProfile</span></span>
<span data-ttu-id="7b134-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b134-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b134-138">-Címtár</span><span class="sxs-lookup"><span data-stu-id="7b134-138">-Directory</span></span>
<span data-ttu-id="7b134-139">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="7b134-139">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7b134-140">Ez a parancsmag feltölti a fájlt a paraméter által megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="7b134-140">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="7b134-141">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7b134-141">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7b134-142">A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="7b134-142">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="7b134-143">-Force</span><span class="sxs-lookup"><span data-stu-id="7b134-143">-Force</span></span>
<span data-ttu-id="7b134-144">Jelzi, hogy ez a parancsmag felülír egy meglévő Azure-tárterületet.</span><span class="sxs-lookup"><span data-stu-id="7b134-144">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="7b134-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b134-145">-PassThru</span></span>
<span data-ttu-id="7b134-146">Azt jelzi, hogy ez a parancsmag az általa létrehozott vagy feltöltött **AzureStorageFile** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7b134-146">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="7b134-147">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="7b134-147">-Path</span></span>
<span data-ttu-id="7b134-148">A fájl vagy mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-148">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="7b134-149">Ezzel a parancsmaggal a program feltölti a tartalmat a paraméter által megadott fájlba vagy a paraméter által megadott mappában lévő fájlba.</span><span class="sxs-lookup"><span data-stu-id="7b134-149">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="7b134-150">Ha megad egy mappát, a parancsmag a forrásfájl nevével megegyező nevű fájlt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7b134-150">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="7b134-151">Ha olyan fájl elérési útját adja meg, amely nem létezik, akkor ez a parancsmag hozza létre a fájlt, és menti a tartalmat.</span><span class="sxs-lookup"><span data-stu-id="7b134-151">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="7b134-152">Ha olyan fájlt ad meg, amely már létezik, és az _erő_ paramétert adja meg, ez a parancsmag felülírja a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="7b134-152">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="7b134-153">Ha olyan fájlt ad meg, amely már létezik, és nem adja meg az _erő_ lehetőséget, ez a parancsmag nem változtatja meg, és hibát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7b134-153">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="7b134-154">Ha olyan mappa elérési útját adja meg, amely nem létezik, akkor ez a parancsmag nem változtatja meg a hibát, és hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7b134-154">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b134-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7b134-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7b134-156">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7b134-157">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="7b134-157">-Share</span></span>
<span data-ttu-id="7b134-158">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-158">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7b134-159">Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-159">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="7b134-160">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7b134-160">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="7b134-161">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7b134-161">This object contains the storage context.</span></span>
<span data-ttu-id="7b134-162">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="7b134-162">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="7b134-163">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="7b134-163">-ShareName</span></span>
<span data-ttu-id="7b134-164">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="7b134-164">Specifies the name of the file share.</span></span>
<span data-ttu-id="7b134-165">Ez a parancsmag a fájlmegosztás fájljában a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-165">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="7b134-166">-Forrás</span><span class="sxs-lookup"><span data-stu-id="7b134-166">-Source</span></span>
<span data-ttu-id="7b134-167">A parancsmag által feltöltött forrásfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b134-167">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="7b134-168">Ha olyan fájlt ad meg, amely nem létezik, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7b134-168">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b134-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b134-169">-Confirm</span></span>
<span data-ttu-id="7b134-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b134-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b134-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b134-171">-WhatIf</span></span>
<span data-ttu-id="7b134-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b134-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b134-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b134-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b134-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b134-174">CommonParameters</span></span>
<span data-ttu-id="7b134-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b134-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b134-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b134-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b134-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b134-177">INPUTS</span></span>

### <span data-ttu-id="7b134-178">Microsoft. WindowsAzure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7b134-178">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="7b134-179">Paraméterek: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b134-179">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="7b134-180">Microsoft. WindowsAzure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7b134-180">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="7b134-181">Paraméterek: címtár (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b134-181">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="7b134-182">System. String</span><span class="sxs-lookup"><span data-stu-id="7b134-182">System.String</span></span>

### <span data-ttu-id="7b134-183">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b134-183">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7b134-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b134-184">OUTPUTS</span></span>

### <span data-ttu-id="7b134-185">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="7b134-185">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="7b134-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b134-186">NOTES</span></span>

## <span data-ttu-id="7b134-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b134-187">RELATED LINKS</span></span>

[<span data-ttu-id="7b134-188">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7b134-188">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="7b134-189">Új – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7b134-189">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="7b134-190">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7b134-190">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
