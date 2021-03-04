---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 7d3d16632e2afb503bf659058643244fd8578d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922657"
---
# <span data-ttu-id="b8a5a-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8a5a-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="b8a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a5a-103">Egy Azure-tároló tárolt hozzáférési házirendet vagy házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="b8a5a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8a5a-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b8a5a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a5a-106">A **Get-AzStorageContainerStoredAccessPolicy** parancsmag egy Azure-tároló tárolt hozzáférési házirendje vagy házirendjeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="b8a5a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="b8a5a-108">1. példa: Tárolt hozzáférési házirend lekérte egy tárolóban</span><span class="sxs-lookup"><span data-stu-id="b8a5a-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="b8a5a-109">Ez a parancs a Policy22 nevű hozzáférési házirendet a Container07 nevű tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="b8a5a-110">2. példa: Az összes tárolt hozzáférési házirend lekérte egy tárolóba</span><span class="sxs-lookup"><span data-stu-id="b8a5a-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="b8a5a-111">Ez a parancs az összes hozzáférési házirendet a Container07 nevű tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="b8a5a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8a5a-112">PARAMETERS</span></span>

### <span data-ttu-id="b8a5a-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8a5a-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8a5a-114">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8a5a-115">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8a5a-116">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8a5a-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8a5a-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8a5a-118">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8a5a-119">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8a5a-120">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8a5a-121">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8a5a-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-122">The default value is 10.</span></span>

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

### <span data-ttu-id="b8a5a-123">-Container</span><span class="sxs-lookup"><span data-stu-id="b8a5a-123">-Container</span></span>
<span data-ttu-id="b8a5a-124">Az Azure-tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="b8a5a-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b8a5a-125">-Context</span></span>
<span data-ttu-id="b8a5a-126">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="b8a5a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a5a-127">-DefaultProfile</span></span>
<span data-ttu-id="b8a5a-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a5a-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b8a5a-129">-Policy</span></span>
<span data-ttu-id="b8a5a-130">Az Azure tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="b8a5a-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8a5a-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8a5a-132">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b8a5a-133">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b8a5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a5a-134">CommonParameters</span></span>
<span data-ttu-id="b8a5a-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a5a-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a5a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a5a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8a5a-137">INPUTS</span></span>

### <span data-ttu-id="b8a5a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b8a5a-138">System.String</span></span>

### <span data-ttu-id="b8a5a-139">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8a5a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b8a5a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8a5a-140">OUTPUTS</span></span>

### <span data-ttu-id="b8a5a-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="b8a5a-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="b8a5a-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8a5a-142">NOTES</span></span>

## <span data-ttu-id="b8a5a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8a5a-143">RELATED LINKS</span></span>

[<span data-ttu-id="b8a5a-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8a5a-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b8a5a-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8a5a-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b8a5a-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8a5a-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


