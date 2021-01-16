---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479397"
---
# <span data-ttu-id="8b178-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="8b178-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="8b178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b178-102">SYNOPSIS</span></span>
<span data-ttu-id="8b178-103">Eltávolítja egy társzolgáltatás CORS-ját.</span><span class="sxs-lookup"><span data-stu-id="8b178-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="8b178-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8b178-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8b178-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8b178-105">DESCRIPTION</span></span>
<span data-ttu-id="8b178-106">A **Remove-AzStorageCORSRule** parancsmag eltávolítja a több forrásból való erőforrás-megosztást (CORS) egy Azure Storage-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8b178-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="8b178-107">Ez a parancsmag törli a társzolgáltatás-típus összes CORS-szabályát.</span><span class="sxs-lookup"><span data-stu-id="8b178-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="8b178-108">A parancsmag társzolgáltatásának típusai a blob, a tábla, a várólista és a fájl.</span><span class="sxs-lookup"><span data-stu-id="8b178-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="8b178-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8b178-109">EXAMPLES</span></span>

### <span data-ttu-id="8b178-110">1. példa: A BLOB-szolgáltatás CORS-szabályainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8b178-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="8b178-111">Ez a parancs eltávolítja a Blob szolgáltatástípus CORS-szabályait.</span><span class="sxs-lookup"><span data-stu-id="8b178-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="8b178-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b178-112">PARAMETERS</span></span>

### <span data-ttu-id="8b178-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b178-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8b178-114">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8b178-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8b178-115">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="8b178-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8b178-116">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8b178-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b178-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8b178-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8b178-118">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="8b178-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8b178-119">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="8b178-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8b178-120">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="8b178-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8b178-121">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8b178-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8b178-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8b178-122">The default value is 10.</span></span>

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

### <span data-ttu-id="8b178-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8b178-123">-Context</span></span>
<span data-ttu-id="8b178-124">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8b178-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8b178-125">A tárolási környezet lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8b178-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8b178-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b178-126">-DefaultProfile</span></span>
<span data-ttu-id="8b178-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b178-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b178-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b178-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8b178-129">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b178-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8b178-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="8b178-130">-ServiceType</span></span>
<span data-ttu-id="8b178-131">Azt az Azure Storage szolgáltatástípust adja meg, amelyből a parancsmag eltávolítja a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="8b178-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="8b178-132">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8b178-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b178-133">Blob</span><span class="sxs-lookup"><span data-stu-id="8b178-133">Blob</span></span> 
- <span data-ttu-id="8b178-134">Táblázat</span><span class="sxs-lookup"><span data-stu-id="8b178-134">Table</span></span> 
- <span data-ttu-id="8b178-135">Várólistán</span><span class="sxs-lookup"><span data-stu-id="8b178-135">Queue</span></span> 
- <span data-ttu-id="8b178-136">Fájl</span><span class="sxs-lookup"><span data-stu-id="8b178-136">File</span></span>

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

### <span data-ttu-id="8b178-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b178-137">CommonParameters</span></span>
<span data-ttu-id="8b178-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b178-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b178-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b178-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b178-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b178-140">INPUTS</span></span>

### <span data-ttu-id="8b178-141">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b178-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8b178-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b178-142">OUTPUTS</span></span>

### <span data-ttu-id="8b178-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="8b178-143">System.Void</span></span>

## <span data-ttu-id="8b178-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8b178-144">NOTES</span></span>

## <span data-ttu-id="8b178-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b178-145">RELATED LINKS</span></span>

[<span data-ttu-id="8b178-146">Get-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="8b178-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="8b178-147">Set-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="8b178-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


