---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 174353aacbfe939294f654a4f5f61548bfc672dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505727"
---
# <span data-ttu-id="a0321-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0321-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="a0321-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0321-102">SYNOPSIS</span></span>
<span data-ttu-id="a0321-103">Beolvassa a tárolt hozzáférés házirendjének vagy házirendjeinek egy Azure Storage tárolót.</span><span class="sxs-lookup"><span data-stu-id="a0321-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0321-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0321-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a0321-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0321-105">DESCRIPTION</span></span>
<span data-ttu-id="a0321-106">A **Get-AzureStorageContainerStoredAccessPolicy** parancsmag felsorolja az Azure-tárolók tárolt hozzáférési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="a0321-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="a0321-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0321-107">EXAMPLES</span></span>

### <span data-ttu-id="a0321-108">Példa 1: tárolt hozzáférés-házirend beszerzése tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="a0321-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="a0321-109">Ez a parancs a Policy22 nevű Access-házirendet a Container07 nevű tároló tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0321-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="a0321-110">2. példa: az összes tárolt hozzáférés-házirend beolvasása egy tárterület-tárolóban</span><span class="sxs-lookup"><span data-stu-id="a0321-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="a0321-111">Ez a parancs a Container07 nevű tároló tárolóban minden hozzáférési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="a0321-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="a0321-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0321-112">PARAMETERS</span></span>

### <span data-ttu-id="a0321-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0321-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0321-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="a0321-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0321-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="a0321-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0321-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a0321-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0321-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0321-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0321-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0321-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0321-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a0321-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0321-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="a0321-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0321-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="a0321-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0321-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a0321-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a0321-123">-Container</span><span class="sxs-lookup"><span data-stu-id="a0321-123">-Container</span></span>
<span data-ttu-id="a0321-124">Az Azure Storage tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0321-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="a0321-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a0321-125">-Context</span></span>
<span data-ttu-id="a0321-126">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0321-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="a0321-127">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a0321-127">-Policy</span></span>
<span data-ttu-id="a0321-128">Az Azure tárolt hozzáférés házirendjének megadása.</span><span class="sxs-lookup"><span data-stu-id="a0321-128">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="a0321-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0321-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0321-130">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="a0321-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a0321-131">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a0321-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a0321-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0321-132">CommonParameters</span></span>
<span data-ttu-id="a0321-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0321-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0321-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0321-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0321-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0321-135">INPUTS</span></span>

### <span data-ttu-id="a0321-136">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="a0321-136">String</span></span>

<span data-ttu-id="a0321-137">A "Container" paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="a0321-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="a0321-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0321-138">IStorageContext</span></span>

<span data-ttu-id="a0321-139">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a0321-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="a0321-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0321-140">OUTPUTS</span></span>

### <span data-ttu-id="a0321-141">Microsoft. WindowsAzure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="a0321-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="a0321-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0321-142">NOTES</span></span>

## <span data-ttu-id="a0321-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0321-143">RELATED LINKS</span></span>

[<span data-ttu-id="a0321-144">Új – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0321-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="a0321-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0321-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="a0321-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0321-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


