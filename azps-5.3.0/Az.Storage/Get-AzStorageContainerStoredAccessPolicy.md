---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 5a0f976d561396bc93facfeedcbb1c89c768e5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374064"
---
# <span data-ttu-id="d8023-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8023-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d8023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8023-102">SYNOPSIS</span></span>
<span data-ttu-id="d8023-103">Egy Azure-tároló tárolt hozzáférési házirendet vagy házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="d8023-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="d8023-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8023-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d8023-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8023-105">DESCRIPTION</span></span>
<span data-ttu-id="d8023-106">A **Get-AzStorageContainerStoredAccessPolicy** parancsmag egy Azure-tároló tárolt hozzáférési házirendje vagy házirendjeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d8023-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="d8023-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8023-107">EXAMPLES</span></span>

### <span data-ttu-id="d8023-108">1. példa: Tárolt hozzáférési házirend lekérte egy tárolóban</span><span class="sxs-lookup"><span data-stu-id="d8023-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="d8023-109">Ez a parancs a Policy22 nevű hozzáférési házirendet a Container07 nevű tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d8023-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="d8023-110">2. példa: Az összes tárolt hozzáférési házirend lekérte egy tárolóba</span><span class="sxs-lookup"><span data-stu-id="d8023-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="d8023-111">Ez a parancs az összes hozzáférési házirendet a Container07 nevű tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d8023-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="d8023-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8023-112">PARAMETERS</span></span>

### <span data-ttu-id="d8023-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8023-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d8023-114">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="d8023-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d8023-115">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="d8023-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d8023-116">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d8023-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d8023-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d8023-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d8023-118">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="d8023-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d8023-119">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d8023-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d8023-120">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="d8023-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d8023-121">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="d8023-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d8023-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="d8023-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d8023-123">-Container</span><span class="sxs-lookup"><span data-stu-id="d8023-123">-Container</span></span>
<span data-ttu-id="d8023-124">Az Azure-tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8023-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8023-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d8023-125">-Context</span></span>
<span data-ttu-id="d8023-126">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d8023-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="d8023-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8023-127">-DefaultProfile</span></span>
<span data-ttu-id="d8023-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8023-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8023-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="d8023-129">-Policy</span></span>
<span data-ttu-id="d8023-130">Az Azure tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8023-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8023-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8023-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d8023-132">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="d8023-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d8023-133">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d8023-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d8023-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8023-134">CommonParameters</span></span>
<span data-ttu-id="d8023-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8023-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8023-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8023-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8023-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8023-137">INPUTS</span></span>

### <span data-ttu-id="d8023-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d8023-138">System.String</span></span>

### <span data-ttu-id="d8023-139">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8023-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d8023-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8023-140">OUTPUTS</span></span>

### <span data-ttu-id="d8023-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="d8023-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="d8023-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8023-142">NOTES</span></span>

## <span data-ttu-id="d8023-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8023-143">RELATED LINKS</span></span>

[<span data-ttu-id="d8023-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8023-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d8023-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8023-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d8023-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8023-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


