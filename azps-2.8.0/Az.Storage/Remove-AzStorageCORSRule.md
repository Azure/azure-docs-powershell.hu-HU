---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: 4781e5afc5fc560fdfb60dd06b412f4dad9a54cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839794"
---
# <span data-ttu-id="c6c78-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c6c78-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="c6c78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6c78-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c78-103">Eltávolítja a CORS a tárterület-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c6c78-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="c6c78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6c78-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c6c78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6c78-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c78-106">A **Remove-AzStorageCORSRule** parancsmag eltávolítja a Cross-Origin Resource Sharing (CORS) szolgáltatást az Azure-tárterületeken.</span><span class="sxs-lookup"><span data-stu-id="c6c78-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="c6c78-107">Ez a parancsmag törli az összes CORS-szabályt egy tárterület-típusban.</span><span class="sxs-lookup"><span data-stu-id="c6c78-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="c6c78-108">Az e parancsmaghoz tartozó tárolási szolgáltatások típusa blob, táblázat, várólista és fájl.</span><span class="sxs-lookup"><span data-stu-id="c6c78-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="c6c78-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c6c78-109">EXAMPLES</span></span>

### <span data-ttu-id="c6c78-110">1. példa: a blob-szolgáltatás CORS-szabályainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c6c78-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="c6c78-111">Ez a parancs eltávolítja a CORS-szabályokat a blob-szolgáltatás típusához.</span><span class="sxs-lookup"><span data-stu-id="c6c78-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="c6c78-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6c78-112">PARAMETERS</span></span>

### <span data-ttu-id="c6c78-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6c78-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c6c78-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="c6c78-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c6c78-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="c6c78-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c6c78-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="c6c78-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6c78-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c6c78-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c6c78-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6c78-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c6c78-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="c6c78-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c6c78-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="c6c78-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c6c78-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="c6c78-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c6c78-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c6c78-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c6c78-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c6c78-123">-Context</span></span>
<span data-ttu-id="c6c78-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6c78-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c6c78-125">A tárolási környezet (New-AzStorageContext parancsmag) beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="c6c78-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c6c78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c78-126">-DefaultProfile</span></span>
<span data-ttu-id="c6c78-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6c78-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c78-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6c78-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c6c78-129">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6c78-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c6c78-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c6c78-130">-ServiceType</span></span>
<span data-ttu-id="c6c78-131">Annak az Azure Storage Service-típusnak a megadása, amelyhez a parancsmag eltávolítja a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="c6c78-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="c6c78-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c6c78-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6c78-133">BLOB</span><span class="sxs-lookup"><span data-stu-id="c6c78-133">Blob</span></span> 
- <span data-ttu-id="c6c78-134">Táblázat</span><span class="sxs-lookup"><span data-stu-id="c6c78-134">Table</span></span> 
- <span data-ttu-id="c6c78-135">Várólista</span><span class="sxs-lookup"><span data-stu-id="c6c78-135">Queue</span></span> 
- <span data-ttu-id="c6c78-136">Fájl</span><span class="sxs-lookup"><span data-stu-id="c6c78-136">File</span></span>

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

### <span data-ttu-id="c6c78-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c78-137">CommonParameters</span></span>
<span data-ttu-id="c6c78-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6c78-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c78-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c78-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c78-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c78-140">INPUTS</span></span>

### <span data-ttu-id="c6c78-141">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6c78-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6c78-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c78-142">OUTPUTS</span></span>

### <span data-ttu-id="c6c78-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="c6c78-143">System.Void</span></span>

## <span data-ttu-id="c6c78-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6c78-144">NOTES</span></span>

## <span data-ttu-id="c6c78-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6c78-145">RELATED LINKS</span></span>

[<span data-ttu-id="c6c78-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c6c78-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="c6c78-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c6c78-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


