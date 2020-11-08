---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180783"
---
# <span data-ttu-id="774c0-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="774c0-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="774c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="774c0-102">SYNOPSIS</span></span>
<span data-ttu-id="774c0-103">A másolási művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="774c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="774c0-104">SYNTAX</span></span>

### <span data-ttu-id="774c0-105">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="774c0-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="774c0-106">Fájl</span><span class="sxs-lookup"><span data-stu-id="774c0-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="774c0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="774c0-107">DESCRIPTION</span></span>
<span data-ttu-id="774c0-108">A **Get-AzStorageFileCopyState** parancsmag az Azure-tárterület fájlmásolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="774c0-109">A fájl másolása fájlból kell futnia.</span><span class="sxs-lookup"><span data-stu-id="774c0-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="774c0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="774c0-110">EXAMPLES</span></span>

### <span data-ttu-id="774c0-111">Példa 1: a másolati állapot beolvasása fájlnév szerint</span><span class="sxs-lookup"><span data-stu-id="774c0-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="774c0-112">Ez a parancs a megadott nevű fájl másolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="774c0-113">2. példa: a másolás és a csővezeték másolása a másolási állapot eléréséhez</span><span class="sxs-lookup"><span data-stu-id="774c0-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="774c0-114">Az első parancs elindítja a "contosofile" fájlt "contosofile_copy"-ra, és a kimenetet a destiantion-fájl objektumba.</span><span class="sxs-lookup"><span data-stu-id="774c0-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="774c0-115">A második parancs a destiantion a Get-AzStorageFileCopyState-ra, hogy másolja a vágólapra a fájlmásolási állapotot.</span><span class="sxs-lookup"><span data-stu-id="774c0-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="774c0-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="774c0-116">PARAMETERS</span></span>

### <span data-ttu-id="774c0-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="774c0-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="774c0-118">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="774c0-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="774c0-119">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="774c0-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="774c0-120">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="774c0-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="774c0-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="774c0-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="774c0-122">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="774c0-123">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="774c0-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="774c0-124">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="774c0-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="774c0-125">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="774c0-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="774c0-126">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="774c0-126">The default value is 10.</span></span>

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

### <span data-ttu-id="774c0-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="774c0-127">-Context</span></span>
<span data-ttu-id="774c0-128">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="774c0-129">Környezet beolvasásához használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="774c0-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="774c0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="774c0-130">-DefaultProfile</span></span>
<span data-ttu-id="774c0-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="774c0-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="774c0-132">-Fájl</span><span class="sxs-lookup"><span data-stu-id="774c0-132">-File</span></span>
<span data-ttu-id="774c0-133">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="774c0-134">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="774c0-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="774c0-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="774c0-135">-FilePath</span></span>
<span data-ttu-id="774c0-136">A fájl elérési útját adja meg egy Azure-tárterülethez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="774c0-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="774c0-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="774c0-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="774c0-138">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="774c0-139">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="774c0-139">-ShareName</span></span>
<span data-ttu-id="774c0-140">A megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="774c0-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="774c0-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="774c0-141">-WaitForComplete</span></span>
<span data-ttu-id="774c0-142">Jelzi, hogy ez a parancsmag várja a másolat befejezését.</span><span class="sxs-lookup"><span data-stu-id="774c0-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="774c0-143">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadott eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="774c0-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="774c0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="774c0-144">CommonParameters</span></span>
<span data-ttu-id="774c0-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="774c0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="774c0-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="774c0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="774c0-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="774c0-147">INPUTS</span></span>

### <span data-ttu-id="774c0-148">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="774c0-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="774c0-149">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="774c0-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="774c0-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="774c0-150">OUTPUTS</span></span>

### <span data-ttu-id="774c0-151">Microsoft. Azure. Storage. file. CopyState</span><span class="sxs-lookup"><span data-stu-id="774c0-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="774c0-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="774c0-152">NOTES</span></span>

## <span data-ttu-id="774c0-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="774c0-153">RELATED LINKS</span></span>

[<span data-ttu-id="774c0-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="774c0-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="774c0-155">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="774c0-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="774c0-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="774c0-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="774c0-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="774c0-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
