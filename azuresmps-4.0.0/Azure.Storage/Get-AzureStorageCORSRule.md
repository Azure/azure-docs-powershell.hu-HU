---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c65daf144708340649b9f7b1566c5e5f2dd81e45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491739"
---
# <span data-ttu-id="fc144-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fc144-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="fc144-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc144-102">SYNOPSIS</span></span>
<span data-ttu-id="fc144-103">Beolvassa a tárolási CORS vonatkozó szabályokat.</span><span class="sxs-lookup"><span data-stu-id="fc144-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="fc144-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc144-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc144-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc144-105">DESCRIPTION</span></span>
<span data-ttu-id="fc144-106">A **Get-AzureStorageCORSRule** parancsmagban az Azure Storage Service Type (CORS) erőforrás-megosztási szabályokat kapja.</span><span class="sxs-lookup"><span data-stu-id="fc144-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="fc144-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc144-107">EXAMPLES</span></span>

### <span data-ttu-id="fc144-108">1. példa: a blob-szolgáltatás CORS szabályainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="fc144-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="fc144-109">Ez a parancs a blob-CORS vonatkozó szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fc144-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="fc144-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc144-110">PARAMETERS</span></span>

### <span data-ttu-id="fc144-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc144-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fc144-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="fc144-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fc144-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="fc144-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fc144-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="fc144-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fc144-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fc144-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fc144-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc144-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fc144-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="fc144-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fc144-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="fc144-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fc144-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="fc144-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fc144-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="fc144-120">The default value is 10.</span></span>

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

### <span data-ttu-id="fc144-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fc144-121">-Context</span></span>
<span data-ttu-id="fc144-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc144-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="fc144-123">Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fc144-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fc144-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc144-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fc144-125">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc144-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fc144-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fc144-126">-ServiceType</span></span>
<span data-ttu-id="fc144-127">Annak az Azure Storage Service típusnak a megadása, amelyhez a parancsmag CORS-szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="fc144-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="fc144-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fc144-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc144-129">BLOB</span><span class="sxs-lookup"><span data-stu-id="fc144-129">Blob</span></span> 
- <span data-ttu-id="fc144-130">Táblázat</span><span class="sxs-lookup"><span data-stu-id="fc144-130">Table</span></span> 
- <span data-ttu-id="fc144-131">Várólista</span><span class="sxs-lookup"><span data-stu-id="fc144-131">Queue</span></span> 
- <span data-ttu-id="fc144-132">Fájl</span><span class="sxs-lookup"><span data-stu-id="fc144-132">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc144-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc144-133">CommonParameters</span></span>
<span data-ttu-id="fc144-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc144-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc144-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc144-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc144-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc144-136">INPUTS</span></span>

## <span data-ttu-id="fc144-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc144-137">OUTPUTS</span></span>

###  
<span data-ttu-id="fc144-138">Ez a parancsmag a **PSCORSRule** -objektumok egy olyan sorát ad eredményül, amely a CORS szabályait képviseli jelenleg a szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="fc144-138">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="fc144-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc144-139">NOTES</span></span>

## <span data-ttu-id="fc144-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc144-140">RELATED LINKS</span></span>

[<span data-ttu-id="fc144-141">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fc144-141">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="fc144-142">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fc144-142">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


