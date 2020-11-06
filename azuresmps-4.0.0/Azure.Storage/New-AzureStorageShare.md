---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
ms.openlocfilehash: 381bfc62ed3a80b650b61b11790a87658a75ee9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491335"
---
# <span data-ttu-id="18e6c-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="18e6c-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="18e6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="18e6c-103">Létrehozza a fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="18e6c-103">Creates a file share.</span></span>

## <span data-ttu-id="18e6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18e6c-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="18e6c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="18e6c-106">A **New-AzureStorageShare** parancsmag létrehoz egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="18e6c-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="18e6c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="18e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="18e6c-108">Példa 1: fájlmegosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="18e6c-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="18e6c-109">Ez a parancs létrehoz egy ContosoShare06 nevű fájlmegosztás-megosztást.</span><span class="sxs-lookup"><span data-stu-id="18e6c-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="18e6c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="18e6c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="18e6c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="18e6c-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="18e6c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="18e6c-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="18e6c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="18e6c-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="18e6c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="18e6c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="18e6c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="18e6c-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e6c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="18e6c-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="18e6c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="18e6c-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="18e6c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="18e6c-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="18e6c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="18e6c-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="18e6c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="18e6c-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="18e6c-121">-Context</span></span>
<span data-ttu-id="18e6c-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e6c-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="18e6c-123">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="18e6c-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="18e6c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18e6c-124">-Name</span></span>
<span data-ttu-id="18e6c-125">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e6c-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="18e6c-126">Ez a parancsmag létrehoz egy olyan fájlmegosztás nevű fájlt, amely a paraméter által megadott névvel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="18e6c-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18e6c-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="18e6c-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="18e6c-128">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e6c-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="18e6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e6c-129">CommonParameters</span></span>
<span data-ttu-id="18e6c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18e6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e6c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e6c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e6c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18e6c-132">INPUTS</span></span>

## <span data-ttu-id="18e6c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18e6c-133">OUTPUTS</span></span>

## <span data-ttu-id="18e6c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18e6c-134">NOTES</span></span>

## <span data-ttu-id="18e6c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18e6c-135">RELATED LINKS</span></span>

[<span data-ttu-id="18e6c-136">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="18e6c-136">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="18e6c-137">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="18e6c-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="18e6c-138">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="18e6c-138">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
