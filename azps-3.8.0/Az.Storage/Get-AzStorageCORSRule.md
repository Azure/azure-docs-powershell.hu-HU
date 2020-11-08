---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: 1eb5803c65739c2e202d042efbf6ba4dff815394
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011235"
---
# <span data-ttu-id="e410f-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e410f-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="e410f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e410f-102">SYNOPSIS</span></span>
<span data-ttu-id="e410f-103">Beolvassa a tárolási CORS vonatkozó szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e410f-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="e410f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e410f-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e410f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e410f-105">DESCRIPTION</span></span>
<span data-ttu-id="e410f-106">A **Get-AzStorageCORSRule** parancsmagban az Azure Storage Service Type (CORS) erőforrás-megosztási szabályokat kapja.</span><span class="sxs-lookup"><span data-stu-id="e410f-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="e410f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e410f-107">EXAMPLES</span></span>

### <span data-ttu-id="e410f-108">1. példa: a blob-szolgáltatás CORS szabályainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e410f-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="e410f-109">Ez a parancs a blob-CORS vonatkozó szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e410f-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="e410f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e410f-110">PARAMETERS</span></span>

### <span data-ttu-id="e410f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e410f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e410f-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="e410f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e410f-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="e410f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e410f-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="e410f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e410f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e410f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e410f-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e410f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e410f-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="e410f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e410f-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="e410f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e410f-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="e410f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e410f-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="e410f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e410f-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e410f-121">-Context</span></span>
<span data-ttu-id="e410f-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e410f-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e410f-123">Környezet beolvasásához használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e410f-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e410f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e410f-124">-DefaultProfile</span></span>
<span data-ttu-id="e410f-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e410f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e410f-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e410f-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e410f-127">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e410f-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e410f-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e410f-128">-ServiceType</span></span>
<span data-ttu-id="e410f-129">Annak az Azure Storage Service típusnak a megadása, amelyhez a parancsmag CORS-szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="e410f-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="e410f-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e410f-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e410f-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="e410f-131">Blob</span></span> 
- <span data-ttu-id="e410f-132">Táblázat</span><span class="sxs-lookup"><span data-stu-id="e410f-132">Table</span></span> 
- <span data-ttu-id="e410f-133">Várólista</span><span class="sxs-lookup"><span data-stu-id="e410f-133">Queue</span></span> 
- <span data-ttu-id="e410f-134">Fájl</span><span class="sxs-lookup"><span data-stu-id="e410f-134">File</span></span>

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

### <span data-ttu-id="e410f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e410f-135">CommonParameters</span></span>
<span data-ttu-id="e410f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e410f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e410f-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e410f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e410f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e410f-138">INPUTS</span></span>

### <span data-ttu-id="e410f-139">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e410f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e410f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e410f-140">OUTPUTS</span></span>

### <span data-ttu-id="e410f-141">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="e410f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="e410f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e410f-142">NOTES</span></span>

## <span data-ttu-id="e410f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e410f-143">RELATED LINKS</span></span>

[<span data-ttu-id="e410f-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e410f-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="e410f-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e410f-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


