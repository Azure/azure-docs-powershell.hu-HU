---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: b6323cd751d25038ff6705cee45594796d782326
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374007"
---
# <span data-ttu-id="09eb5-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="09eb5-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="09eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="09eb5-103">Lekérte a fájlmegosztások listáját.</span><span class="sxs-lookup"><span data-stu-id="09eb5-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="09eb5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09eb5-104">SYNTAX</span></span>

### <span data-ttu-id="09eb5-105">MatchingPrefix (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09eb5-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="09eb5-106">Specific</span><span class="sxs-lookup"><span data-stu-id="09eb5-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="09eb5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09eb5-107">DESCRIPTION</span></span>
<span data-ttu-id="09eb5-108">A **Get-AzStorageShare** parancsmag lekérte egy tárfiók fájlmegosztási listáját.</span><span class="sxs-lookup"><span data-stu-id="09eb5-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="09eb5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09eb5-109">EXAMPLES</span></span>

### <span data-ttu-id="09eb5-110">1. példa: Fájlmegosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="09eb5-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="09eb5-111">Ez a parancs a ContosoShare06 nevű fájlmegosztást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="09eb5-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="09eb5-112">2. példa: Az összes olyan fájlmegosztás lekérte, amely karakterláncmal kezdődik</span><span class="sxs-lookup"><span data-stu-id="09eb5-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="09eb5-113">Ez a parancs a Contoso névvel kezdődik fájlmegosztásokat is beveszi.</span><span class="sxs-lookup"><span data-stu-id="09eb5-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="09eb5-114">3. példa: Az összes fájlmegosztás lekérte egy adott környezetben</span><span class="sxs-lookup"><span data-stu-id="09eb5-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="09eb5-115">Az első parancs a **New-AzStorageContext** parancsmagot használva hoz létre környezetet a *Helyi* paraméter használatával, majd ezt a környezetobjektumot a $Context változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09eb5-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="09eb5-116">A második parancs a helyi menüben tárolt környezetobjektum fájlmegosztási $Context.</span><span class="sxs-lookup"><span data-stu-id="09eb5-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="09eb5-117">4. példa: Fájlmegosztási pillanatfelvétel adott megosztási névvel és SnapshotTime-val</span><span class="sxs-lookup"><span data-stu-id="09eb5-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="09eb5-118">Ez a parancs egy fájlmegosztási pillanatképet kap adott megosztási névvel és SnapshotTime-val.</span><span class="sxs-lookup"><span data-stu-id="09eb5-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="09eb5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09eb5-119">PARAMETERS</span></span>

### <span data-ttu-id="09eb5-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09eb5-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="09eb5-121">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="09eb5-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="09eb5-122">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="09eb5-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="09eb5-123">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="09eb5-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="09eb5-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="09eb5-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="09eb5-125">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="09eb5-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="09eb5-126">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="09eb5-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="09eb5-127">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="09eb5-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="09eb5-128">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="09eb5-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="09eb5-129">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="09eb5-129">The default value is 10.</span></span>

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

### <span data-ttu-id="09eb5-130">-Környezet</span><span class="sxs-lookup"><span data-stu-id="09eb5-130">-Context</span></span>
<span data-ttu-id="09eb5-131">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09eb5-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="09eb5-132">Környezet beszerzéséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09eb5-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09eb5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09eb5-133">-DefaultProfile</span></span>
<span data-ttu-id="09eb5-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09eb5-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09eb5-135">-Name</span><span class="sxs-lookup"><span data-stu-id="09eb5-135">-Name</span></span>
<span data-ttu-id="09eb5-136">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09eb5-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="09eb5-137">Ez a parancsmag a paraméter által megadott fájlmegosztást kapja meg, vagy semmit sem, ha egy nem létező fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09eb5-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09eb5-138">-Előtag</span><span class="sxs-lookup"><span data-stu-id="09eb5-138">-Prefix</span></span>
<span data-ttu-id="09eb5-139">A fájlmegosztások előtagját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="09eb5-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="09eb5-140">Ez a parancsmag olyan fájlmegosztásokat kap, amelyek megegyeznek a paraméter által megadott előtaggal, vagy nem kap fájlmegosztásokat, ha egyetlen fájlmegosztás sem felel meg a megadott előtagnak.</span><span class="sxs-lookup"><span data-stu-id="09eb5-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09eb5-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09eb5-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="09eb5-142">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09eb5-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="09eb5-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="09eb5-143">-SnapshotTime</span></span>
<span data-ttu-id="09eb5-144">SnapshotTime of the file share snapshot to be received.</span><span class="sxs-lookup"><span data-stu-id="09eb5-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09eb5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09eb5-145">CommonParameters</span></span>
<span data-ttu-id="09eb5-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09eb5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09eb5-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09eb5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09eb5-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09eb5-148">INPUTS</span></span>

### <span data-ttu-id="09eb5-149">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="09eb5-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="09eb5-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09eb5-150">OUTPUTS</span></span>

### <span data-ttu-id="09eb5-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="09eb5-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="09eb5-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09eb5-152">NOTES</span></span>

## <span data-ttu-id="09eb5-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09eb5-153">RELATED LINKS</span></span>

[<span data-ttu-id="09eb5-154">New-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="09eb5-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="09eb5-155">Remove-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="09eb5-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
