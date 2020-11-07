---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecorsrule
schema: 2.0.0
ms.openlocfilehash: 9bf9d6d2f37173c9c64c395f4efbb007efa127da
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849417"
---
# <span data-ttu-id="a6fe3-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a6fe3-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="a6fe3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fe3-103">Eltávolítja a CORS a tárterület-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6fe3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6fe3-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a6fe3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="a6fe3-106">A **Remove-AzureStorageCORSRule** parancsmag eltávolítja a Cross-Origin Resource Sharing (CORS) szolgáltatást az Azure-tárterületeken.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="a6fe3-107">Ez a parancsmag törli az összes CORS-szabályt egy tárterület-típusban.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="a6fe3-108">Az e parancsmaghoz tartozó tárolási szolgáltatások típusa blob, táblázat, várólista és fájl.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="a6fe3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a6fe3-109">EXAMPLES</span></span>

### <span data-ttu-id="a6fe3-110">1. példa: a blob-szolgáltatás CORS-szabályainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a6fe3-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="a6fe3-111">Ez a parancs eltávolítja a CORS-szabályokat a blob-szolgáltatás típusához.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="a6fe3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6fe3-112">PARAMETERS</span></span>

### <span data-ttu-id="a6fe3-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6fe3-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a6fe3-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a6fe3-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a6fe3-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a6fe3-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a6fe3-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a6fe3-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a6fe3-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a6fe3-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a6fe3-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="a6fe3-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a6fe3-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a6fe3-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a6fe3-123">-Context</span></span>
<span data-ttu-id="a6fe3-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a6fe3-125">A tárolási környezet (New-AzureStorageContext parancsmag) beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a6fe3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6fe3-126">-DefaultProfile</span></span>
<span data-ttu-id="a6fe3-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6fe3-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6fe3-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a6fe3-129">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a6fe3-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a6fe3-130">-ServiceType</span></span>
<span data-ttu-id="a6fe3-131">Annak az Azure Storage Service-típusnak a megadása, amelyhez a parancsmag eltávolítja a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="a6fe3-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="a6fe3-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a6fe3-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6fe3-133">BLOB</span><span class="sxs-lookup"><span data-stu-id="a6fe3-133">Blob</span></span> 
- <span data-ttu-id="a6fe3-134">Táblázat</span><span class="sxs-lookup"><span data-stu-id="a6fe3-134">Table</span></span> 
- <span data-ttu-id="a6fe3-135">Várólista</span><span class="sxs-lookup"><span data-stu-id="a6fe3-135">Queue</span></span> 
- <span data-ttu-id="a6fe3-136">Fájl</span><span class="sxs-lookup"><span data-stu-id="a6fe3-136">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6fe3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fe3-137">CommonParameters</span></span>
<span data-ttu-id="a6fe3-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6fe3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fe3-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6fe3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fe3-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6fe3-140">INPUTS</span></span>

### <span data-ttu-id="a6fe3-141">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6fe3-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6fe3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6fe3-142">OUTPUTS</span></span>

### <span data-ttu-id="a6fe3-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="a6fe3-143">System.Void</span></span>

## <span data-ttu-id="a6fe3-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6fe3-144">NOTES</span></span>

## <span data-ttu-id="a6fe3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6fe3-145">RELATED LINKS</span></span>

[<span data-ttu-id="a6fe3-146">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a6fe3-146">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="a6fe3-147">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a6fe3-147">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


