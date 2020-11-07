---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
ms.openlocfilehash: cf9f4b3a6d58754c4b992163625887afcb3439b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849442"
---
# <span data-ttu-id="e1bd3-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e1bd3-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="e1bd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bd3-103">Beolvassa a tárolási CORS vonatkozó szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1bd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1bd3-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e1bd3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1bd3-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bd3-106">A **Get-AzureStorageCORSRule** parancsmagban az Azure Storage Service Type (CORS) erőforrás-megosztási szabályokat kapja.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="e1bd3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1bd3-107">EXAMPLES</span></span>

### <span data-ttu-id="e1bd3-108">1. példa: a blob-szolgáltatás CORS szabályainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e1bd3-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="e1bd3-109">Ez a parancs a blob-CORS vonatkozó szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="e1bd3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1bd3-110">PARAMETERS</span></span>

### <span data-ttu-id="e1bd3-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1bd3-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e1bd3-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e1bd3-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e1bd3-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e1bd3-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e1bd3-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e1bd3-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e1bd3-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e1bd3-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e1bd3-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="e1bd3-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e1bd3-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e1bd3-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e1bd3-121">-Context</span></span>
<span data-ttu-id="e1bd3-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e1bd3-123">Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e1bd3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bd3-124">-DefaultProfile</span></span>
<span data-ttu-id="e1bd3-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bd3-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1bd3-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e1bd3-127">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e1bd3-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e1bd3-128">-ServiceType</span></span>
<span data-ttu-id="e1bd3-129">Annak az Azure Storage Service típusnak a megadása, amelyhez a parancsmag CORS-szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="e1bd3-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="e1bd3-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e1bd3-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1bd3-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="e1bd3-131">Blob</span></span> 
- <span data-ttu-id="e1bd3-132">Táblázat</span><span class="sxs-lookup"><span data-stu-id="e1bd3-132">Table</span></span> 
- <span data-ttu-id="e1bd3-133">Várólista</span><span class="sxs-lookup"><span data-stu-id="e1bd3-133">Queue</span></span> 
- <span data-ttu-id="e1bd3-134">Fájl</span><span class="sxs-lookup"><span data-stu-id="e1bd3-134">File</span></span>

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

### <span data-ttu-id="e1bd3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bd3-135">CommonParameters</span></span>
<span data-ttu-id="e1bd3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1bd3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bd3-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1bd3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bd3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1bd3-138">INPUTS</span></span>

### <span data-ttu-id="e1bd3-139">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1bd3-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1bd3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1bd3-140">OUTPUTS</span></span>

### <span data-ttu-id="e1bd3-141">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="e1bd3-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="e1bd3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1bd3-142">NOTES</span></span>

## <span data-ttu-id="e1bd3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1bd3-143">RELATED LINKS</span></span>

[<span data-ttu-id="e1bd3-144">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e1bd3-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="e1bd3-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e1bd3-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


