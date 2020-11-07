---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: 31a8d6cbb205b451233bdc72793fb45443350fdd
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93680923"
---
# <span data-ttu-id="9de2b-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9de2b-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="9de2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9de2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9de2b-103">Megkapja a fájlmegosztás listáját.</span><span class="sxs-lookup"><span data-stu-id="9de2b-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9de2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9de2b-104">SYNTAX</span></span>

### <span data-ttu-id="9de2b-105">MatchingPrefix (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9de2b-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="9de2b-106">Adott</span><span class="sxs-lookup"><span data-stu-id="9de2b-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9de2b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9de2b-107">DESCRIPTION</span></span>
<span data-ttu-id="9de2b-108">A **Get-AzureStorageShare** parancsmag a tárolási fiókban található fájlmegosztás listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9de2b-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="9de2b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9de2b-109">EXAMPLES</span></span>

### <span data-ttu-id="9de2b-110">Példa 1: fájlmegosztás beszerzése</span><span class="sxs-lookup"><span data-stu-id="9de2b-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="9de2b-111">Ez a parancs a ContosoShare06 nevű fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9de2b-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="9de2b-112">2. példa: a karakterláncmal kezdődő összes fájlmegosztás beolvasása</span><span class="sxs-lookup"><span data-stu-id="9de2b-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="9de2b-113">Ez a parancs minden olyan fájlmegosztás esetén beilleszti a fájlt, amelyben a contoso kezdetű nevek szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="9de2b-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="9de2b-114">3. példa: az összes fájlmegosztás beolvasása egy megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="9de2b-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="9de2b-115">Az első parancs a **New-AzureStorageContext** parancsmagot használja a *helyi* paraméterrel létrehozott környezet létrehozásához, majd a $Context változóban tárolja a környezet objektumát.</span><span class="sxs-lookup"><span data-stu-id="9de2b-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="9de2b-116">A második parancs beolvassa a $Contextban tárolt környezeti objektumhoz tartozó fájlokat.</span><span class="sxs-lookup"><span data-stu-id="9de2b-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="9de2b-117">Példa 4: fájlmegosztás-pillanatfelvétel beszerzése adott megosztási névvel és SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="9de2b-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="9de2b-118">Ez a parancs olyan fájlmegosztás-pillanatképet kap, amely adott megosztási névvel és SnapshotTime van megosztva.</span><span class="sxs-lookup"><span data-stu-id="9de2b-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="9de2b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9de2b-119">PARAMETERS</span></span>

### <span data-ttu-id="9de2b-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9de2b-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9de2b-121">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="9de2b-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9de2b-122">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="9de2b-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9de2b-123">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="9de2b-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9de2b-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9de2b-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9de2b-125">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="9de2b-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9de2b-126">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="9de2b-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9de2b-127">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="9de2b-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9de2b-128">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="9de2b-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9de2b-129">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="9de2b-129">The default value is 10.</span></span>

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

### <span data-ttu-id="9de2b-130">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9de2b-130">-Context</span></span>
<span data-ttu-id="9de2b-131">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9de2b-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9de2b-132">Környezet beolvasásához használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9de2b-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9de2b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de2b-133">-DefaultProfile</span></span>
<span data-ttu-id="9de2b-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9de2b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de2b-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9de2b-135">-Name</span></span>
<span data-ttu-id="9de2b-136">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="9de2b-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="9de2b-137">Ez a parancsmag a fájl megosztását adja meg, vagy semmit, ha nem létező fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9de2b-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="9de2b-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="9de2b-138">-Prefix</span></span>
<span data-ttu-id="9de2b-139">A fájlmegosztás előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9de2b-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="9de2b-140">Ez a parancsmag olyan fájlmegosztásokat kap, amelyek megegyeznek a paraméter által megadott előtaggal, vagy ha nincs fájlmegosztás, ha nem egyeznek meg a megadott előtaggal.</span><span class="sxs-lookup"><span data-stu-id="9de2b-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="9de2b-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9de2b-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9de2b-142">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9de2b-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9de2b-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="9de2b-143">-SnapshotTime</span></span>
<span data-ttu-id="9de2b-144">A SnapshotTime pillanatképének beérkezése</span><span class="sxs-lookup"><span data-stu-id="9de2b-144">SnapshotTime of the file share snapshot to be received.</span></span>

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

### <span data-ttu-id="9de2b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de2b-145">CommonParameters</span></span>
<span data-ttu-id="9de2b-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9de2b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de2b-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de2b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de2b-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9de2b-148">INPUTS</span></span>

### <span data-ttu-id="9de2b-149">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9de2b-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9de2b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9de2b-150">OUTPUTS</span></span>

### <span data-ttu-id="9de2b-151">Microsoft. WindowsAzure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9de2b-151">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="9de2b-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9de2b-152">NOTES</span></span>

## <span data-ttu-id="9de2b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9de2b-153">RELATED LINKS</span></span>

[<span data-ttu-id="9de2b-154">Új – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9de2b-154">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="9de2b-155">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9de2b-155">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
