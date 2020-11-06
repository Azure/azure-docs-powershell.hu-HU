---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75e94fe8270287410902b215ec4e33ac9cd51624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491730"
---
# <span data-ttu-id="8922c-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="8922c-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="8922c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8922c-102">SYNOPSIS</span></span>
<span data-ttu-id="8922c-103">A másolási művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="8922c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8922c-104">SYNTAX</span></span>

### <span data-ttu-id="8922c-105">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="8922c-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8922c-106">Fájl</span><span class="sxs-lookup"><span data-stu-id="8922c-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8922c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8922c-107">DESCRIPTION</span></span>
<span data-ttu-id="8922c-108">A **Get-AzureStorageFileCopyState** parancsmag az Azure-tárterület fájlmásolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="8922c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8922c-109">EXAMPLES</span></span>

### <span data-ttu-id="8922c-110">Példa 1: a másolati állapot beolvasása fájlnév szerint</span><span class="sxs-lookup"><span data-stu-id="8922c-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="8922c-111">Ez a parancs a megadott nevű fájl másolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="8922c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8922c-112">PARAMETERS</span></span>

### <span data-ttu-id="8922c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8922c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8922c-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="8922c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8922c-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="8922c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8922c-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="8922c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8922c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8922c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8922c-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8922c-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="8922c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8922c-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="8922c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8922c-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="8922c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8922c-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8922c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="8922c-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8922c-123">-Context</span></span>
<span data-ttu-id="8922c-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="8922c-125">Környezet beolvasásához használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8922c-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8922c-126">-Fájl</span><span class="sxs-lookup"><span data-stu-id="8922c-126">-File</span></span>
<span data-ttu-id="8922c-127">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="8922c-128">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzureStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8922c-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8922c-129">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8922c-129">-FilePath</span></span>
<span data-ttu-id="8922c-130">A fájl elérési útját adja meg egy Azure-tárterülethez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="8922c-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8922c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8922c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8922c-132">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8922c-133">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="8922c-133">-ShareName</span></span>
<span data-ttu-id="8922c-134">A megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8922c-134">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="8922c-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8922c-135">-WaitForComplete</span></span>
<span data-ttu-id="8922c-136">Jelzi, hogy ez a parancsmag várja a másolat befejezését.</span><span class="sxs-lookup"><span data-stu-id="8922c-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="8922c-137">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadott eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="8922c-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="8922c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8922c-138">CommonParameters</span></span>
<span data-ttu-id="8922c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8922c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8922c-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8922c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8922c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8922c-141">INPUTS</span></span>

## <span data-ttu-id="8922c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8922c-142">OUTPUTS</span></span>

## <span data-ttu-id="8922c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8922c-143">NOTES</span></span>

## <span data-ttu-id="8922c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8922c-144">RELATED LINKS</span></span>

[<span data-ttu-id="8922c-145">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8922c-145">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="8922c-146">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8922c-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8922c-147">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8922c-147">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="8922c-148">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8922c-148">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
