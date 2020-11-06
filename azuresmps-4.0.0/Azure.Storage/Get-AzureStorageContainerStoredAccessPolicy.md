---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e9ea56c53d73b9c71d2eade4fec7025466ed82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491735"
---
# <span data-ttu-id="33b4c-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33b4c-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="33b4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="33b4c-103">Beolvassa a tárolt hozzáférés házirendjének vagy házirendjeinek egy Azure Storage tárolót.</span><span class="sxs-lookup"><span data-stu-id="33b4c-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="33b4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33b4c-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="33b4c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="33b4c-106">A **Get-AzureStorageContainerStoredAccessPolicy** parancsmag felsorolja az Azure-tárolók tárolt hozzáférési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="33b4c-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="33b4c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="33b4c-107">EXAMPLES</span></span>

### <span data-ttu-id="33b4c-108">Példa 1: tárolt hozzáférés-házirend beszerzése tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="33b4c-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="33b4c-109">Ez a parancs a Policy22 nevű Access-házirendet a Container07 nevű tároló tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="33b4c-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="33b4c-110">2. példa: az összes tárolt hozzáférés-házirend beolvasása egy tárterület-tárolóban</span><span class="sxs-lookup"><span data-stu-id="33b4c-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="33b4c-111">Ez a parancs a Container07 nevű tároló tárolóban minden hozzáférési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="33b4c-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="33b4c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33b4c-112">PARAMETERS</span></span>

### <span data-ttu-id="33b4c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33b4c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="33b4c-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="33b4c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="33b4c-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="33b4c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="33b4c-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="33b4c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="33b4c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="33b4c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="33b4c-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="33b4c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="33b4c-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="33b4c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="33b4c-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="33b4c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="33b4c-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="33b4c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="33b4c-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="33b4c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="33b4c-123">-Container</span><span class="sxs-lookup"><span data-stu-id="33b4c-123">-Container</span></span>
<span data-ttu-id="33b4c-124">Az Azure Storage tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33b4c-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33b4c-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="33b4c-125">-Context</span></span>
<span data-ttu-id="33b4c-126">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33b4c-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="33b4c-127">-Házirend</span><span class="sxs-lookup"><span data-stu-id="33b4c-127">-Policy</span></span>
<span data-ttu-id="33b4c-128">Az Azure tárolt hozzáférés házirendjének megadása.</span><span class="sxs-lookup"><span data-stu-id="33b4c-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b4c-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33b4c-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="33b4c-130">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="33b4c-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="33b4c-131">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="33b4c-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="33b4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b4c-132">CommonParameters</span></span>
<span data-ttu-id="33b4c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33b4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b4c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b4c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b4c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33b4c-135">INPUTS</span></span>

## <span data-ttu-id="33b4c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33b4c-136">OUTPUTS</span></span>

## <span data-ttu-id="33b4c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33b4c-137">NOTES</span></span>

## <span data-ttu-id="33b4c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33b4c-138">RELATED LINKS</span></span>

[<span data-ttu-id="33b4c-139">Új – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33b4c-139">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="33b4c-140">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33b4c-140">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="33b4c-141">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33b4c-141">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


