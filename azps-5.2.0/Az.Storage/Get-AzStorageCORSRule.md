---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: 1eb5803c65739c2e202d042efbf6ba4dff815394
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349673"
---
# <span data-ttu-id="c7c75-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c7c75-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="c7c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7c75-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c75-103">CORS-szabályokat kap egy társzolgáltatás-típushoz.</span><span class="sxs-lookup"><span data-stu-id="c7c75-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="c7c75-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7c75-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c7c75-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7c75-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c75-106">A **Get-AzStorageCORSRule** parancsmag több forrásból való erőforrás-megosztási (CORS) szabályokat kap egy Azure Storage-szolgáltatástípushoz.</span><span class="sxs-lookup"><span data-stu-id="c7c75-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="c7c75-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7c75-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c75-108">1. példa: A blobszolgáltatás CORS-szabályainak lekérte</span><span class="sxs-lookup"><span data-stu-id="c7c75-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="c7c75-109">Ez a parancs a Blob szolgáltatástípus CORS-szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c75-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="c7c75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7c75-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c75-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7c75-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c7c75-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c7c75-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c7c75-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="c7c75-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c7c75-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c7c75-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c7c75-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c7c75-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c7c75-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="c7c75-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c7c75-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="c7c75-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c7c75-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="c7c75-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c7c75-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c7c75-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c7c75-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c7c75-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c7c75-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c7c75-121">-Context</span></span>
<span data-ttu-id="c7c75-122">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c75-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c7c75-123">Környezet lekérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c7c75-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c7c75-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c75-124">-DefaultProfile</span></span>
<span data-ttu-id="c7c75-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7c75-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c75-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7c75-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c7c75-127">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c75-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c7c75-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c7c75-128">-ServiceType</span></span>
<span data-ttu-id="c7c75-129">Azt az Azure Storage szolgáltatástípust adja meg, amelyhez ez a parancsmag a CORS-szabályokat kapja.</span><span class="sxs-lookup"><span data-stu-id="c7c75-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="c7c75-130">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="c7c75-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c7c75-131">Blob</span><span class="sxs-lookup"><span data-stu-id="c7c75-131">Blob</span></span> 
- <span data-ttu-id="c7c75-132">Táblázat</span><span class="sxs-lookup"><span data-stu-id="c7c75-132">Table</span></span> 
- <span data-ttu-id="c7c75-133">Várólistán</span><span class="sxs-lookup"><span data-stu-id="c7c75-133">Queue</span></span> 
- <span data-ttu-id="c7c75-134">Fájl</span><span class="sxs-lookup"><span data-stu-id="c7c75-134">File</span></span>

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

### <span data-ttu-id="c7c75-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c75-135">CommonParameters</span></span>
<span data-ttu-id="c7c75-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c75-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c75-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c75-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c75-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7c75-138">INPUTS</span></span>

### <span data-ttu-id="c7c75-139">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7c75-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7c75-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c75-140">OUTPUTS</span></span>

### <span data-ttu-id="c7c75-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="c7c75-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="c7c75-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7c75-142">NOTES</span></span>

## <span data-ttu-id="c7c75-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7c75-143">RELATED LINKS</span></span>

[<span data-ttu-id="c7c75-144">Remove-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c7c75-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="c7c75-145">Set-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c7c75-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


