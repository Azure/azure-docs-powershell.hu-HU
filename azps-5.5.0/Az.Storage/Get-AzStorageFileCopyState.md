---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207807"
---
# <span data-ttu-id="7e245-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="7e245-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="7e245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e245-102">SYNOPSIS</span></span>
<span data-ttu-id="7e245-103">A másolási művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e245-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="7e245-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e245-104">SYNTAX</span></span>

### <span data-ttu-id="7e245-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="7e245-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7e245-106">Fájl</span><span class="sxs-lookup"><span data-stu-id="7e245-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e245-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e245-107">DESCRIPTION</span></span>
<span data-ttu-id="7e245-108">A **Get-AzStorageFileCopyState** parancsmag egy Azure Storage-tárfájl másolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e245-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="7e245-109">A fájlnak a másolási célfájlon kell futnia.</span><span class="sxs-lookup"><span data-stu-id="7e245-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="7e245-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e245-110">EXAMPLES</span></span>

### <span data-ttu-id="7e245-111">1. példa: A másolási állapot lekérte fájlnév szerint</span><span class="sxs-lookup"><span data-stu-id="7e245-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="7e245-112">Ez a parancs a megadott nevű fájl másolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e245-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="7e245-113">2. példa: Másolás és folyamat kezdése a másolás állapotának szerezze be</span><span class="sxs-lookup"><span data-stu-id="7e245-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="7e245-114">Az első parancs a "contosofile" fájl másolását "contosofile_copy" szóra kezdi, és kimenetként kimenetet ad a destiantion fájlobjektumnak.</span><span class="sxs-lookup"><span data-stu-id="7e245-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="7e245-115">A második parancssori folyamat a destiantion fájlobjektumot Get-AzStorageFileCopyState fájl másolási állapotának be szereznie.</span><span class="sxs-lookup"><span data-stu-id="7e245-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="7e245-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e245-116">PARAMETERS</span></span>

### <span data-ttu-id="7e245-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e245-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7e245-118">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7e245-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7e245-119">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="7e245-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7e245-120">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="7e245-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7e245-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7e245-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7e245-122">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="7e245-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7e245-123">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="7e245-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7e245-124">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="7e245-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7e245-125">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7e245-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7e245-126">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7e245-126">The default value is 10.</span></span>

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

### <span data-ttu-id="7e245-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7e245-127">-Context</span></span>
<span data-ttu-id="7e245-128">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e245-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7e245-129">Környezet beszerzéséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e245-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7e245-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e245-130">-DefaultProfile</span></span>
<span data-ttu-id="7e245-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e245-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e245-132">-File</span><span class="sxs-lookup"><span data-stu-id="7e245-132">-File</span></span>
<span data-ttu-id="7e245-133">Egy **CloudFile-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="7e245-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="7e245-134">Létrehozhat felhőfájlt, vagy beszerezhet egyet a Get-AzStorageFile parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="7e245-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e245-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7e245-135">-FilePath</span></span>
<span data-ttu-id="7e245-136">A fájl elérési útját adja meg egy Azure Storage-megosztáshoz képest.</span><span class="sxs-lookup"><span data-stu-id="7e245-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e245-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e245-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7e245-138">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e245-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7e245-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7e245-139">-ShareName</span></span>
<span data-ttu-id="7e245-140">Egy megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e245-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="7e245-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7e245-141">-WaitForComplete</span></span>
<span data-ttu-id="7e245-142">Azt jelzi, hogy a parancsmag a másolat befejezéséig vár.</span><span class="sxs-lookup"><span data-stu-id="7e245-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="7e245-143">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadja az eredményt.</span><span class="sxs-lookup"><span data-stu-id="7e245-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="7e245-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e245-144">CommonParameters</span></span>
<span data-ttu-id="7e245-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e245-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e245-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e245-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e245-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e245-147">INPUTS</span></span>

### <span data-ttu-id="7e245-148">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="7e245-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="7e245-149">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e245-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7e245-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e245-150">OUTPUTS</span></span>

### <span data-ttu-id="7e245-151">Microsoft.Azure.Storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="7e245-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="7e245-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e245-152">NOTES</span></span>

## <span data-ttu-id="7e245-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e245-153">RELATED LINKS</span></span>

[<span data-ttu-id="7e245-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="7e245-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="7e245-155">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="7e245-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7e245-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7e245-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="7e245-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7e245-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
