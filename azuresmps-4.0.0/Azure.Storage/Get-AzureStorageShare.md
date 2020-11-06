---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491718"
---
# <span data-ttu-id="78b4c-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="78b4c-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="78b4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="78b4c-103">Megkapja a fájlmegosztás listáját.</span><span class="sxs-lookup"><span data-stu-id="78b4c-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="78b4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78b4c-104">SYNTAX</span></span>

### <span data-ttu-id="78b4c-105">MatchingPrefix (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78b4c-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-106">Adott</span><span class="sxs-lookup"><span data-stu-id="78b4c-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="78b4c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="78b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="78b4c-108">A **Get-AzureStorageShare** parancsmag a tárolási fiókban található fájlmegosztás listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="78b4c-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="78b4c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="78b4c-109">EXAMPLES</span></span>

### <span data-ttu-id="78b4c-110">Példa 1: fájlmegosztás beszerzése</span><span class="sxs-lookup"><span data-stu-id="78b4c-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="78b4c-111">Ez a parancs a ContosoShare06 nevű fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="78b4c-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="78b4c-112">2. példa: a karakterláncmal kezdődő összes fájlmegosztás beolvasása</span><span class="sxs-lookup"><span data-stu-id="78b4c-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="78b4c-113">Ez a parancs minden olyan fájlmegosztás esetén beilleszti a fájlt, amelyben a contoso kezdetű nevek szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="78b4c-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="78b4c-114">3. példa: az összes fájlmegosztás beolvasása egy megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="78b4c-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="78b4c-115">Az első parancs a **New-AzureStorageContext** parancsmagot használja a *helyi* paraméterrel létrehozott környezet létrehozásához, majd a $Context változóban tárolja a környezet objektumát.</span><span class="sxs-lookup"><span data-stu-id="78b4c-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="78b4c-116">A második parancs beolvassa a $Contextban tárolt környezeti objektumhoz tartozó fájlokat.</span><span class="sxs-lookup"><span data-stu-id="78b4c-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="78b4c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78b4c-117">PARAMETERS</span></span>

### <span data-ttu-id="78b4c-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78b4c-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="78b4c-119">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="78b4c-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="78b4c-120">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="78b4c-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="78b4c-121">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="78b4c-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="78b4c-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="78b4c-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="78b4c-123">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="78b4c-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="78b4c-124">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="78b4c-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="78b4c-125">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="78b4c-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="78b4c-126">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="78b4c-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="78b4c-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="78b4c-127">The default value is 10.</span></span>

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

### <span data-ttu-id="78b4c-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="78b4c-128">-Context</span></span>
<span data-ttu-id="78b4c-129">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78b4c-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="78b4c-130">Környezet beolvasásához használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="78b4c-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78b4c-131">-Name</span></span>
<span data-ttu-id="78b4c-132">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="78b4c-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="78b4c-133">Ez a parancsmag a fájl megosztását adja meg, vagy semmit, ha nem létező fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78b4c-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-134">-Prefix</span><span class="sxs-lookup"><span data-stu-id="78b4c-134">-Prefix</span></span>
<span data-ttu-id="78b4c-135">A fájlmegosztás előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="78b4c-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="78b4c-136">Ez a parancsmag olyan fájlmegosztásokat kap, amelyek megegyeznek a paraméter által megadott előtaggal, vagy ha nincs fájlmegosztás, ha nem egyeznek meg a megadott előtaggal.</span><span class="sxs-lookup"><span data-stu-id="78b4c-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78b4c-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="78b4c-138">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="78b4c-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="78b4c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b4c-139">CommonParameters</span></span>
<span data-ttu-id="78b4c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78b4c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b4c-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b4c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b4c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78b4c-142">INPUTS</span></span>

## <span data-ttu-id="78b4c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78b4c-143">OUTPUTS</span></span>

## <span data-ttu-id="78b4c-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78b4c-144">NOTES</span></span>

## <span data-ttu-id="78b4c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78b4c-145">RELATED LINKS</span></span>

[<span data-ttu-id="78b4c-146">Új – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="78b4c-146">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="78b4c-147">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="78b4c-147">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
