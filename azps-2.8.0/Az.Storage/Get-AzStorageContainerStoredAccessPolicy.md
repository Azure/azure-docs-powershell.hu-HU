---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 71f00e9e1842eef237a7128d5e20e2ac2116e8a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839666"
---
# <span data-ttu-id="df608-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df608-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="df608-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df608-102">SYNOPSIS</span></span>
<span data-ttu-id="df608-103">Beolvassa a tárolt hozzáférés házirendjének vagy házirendjeinek egy Azure Storage tárolót.</span><span class="sxs-lookup"><span data-stu-id="df608-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="df608-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df608-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="df608-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df608-105">DESCRIPTION</span></span>
<span data-ttu-id="df608-106">A **Get-AzStorageContainerStoredAccessPolicy** parancsmag felsorolja az Azure-tárolók tárolt hozzáférési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="df608-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="df608-107">Példák</span><span class="sxs-lookup"><span data-stu-id="df608-107">EXAMPLES</span></span>

### <span data-ttu-id="df608-108">Példa 1: tárolt hozzáférés-házirend beszerzése tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="df608-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="df608-109">Ez a parancs a Policy22 nevű Access-házirendet a Container07 nevű tároló tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="df608-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="df608-110">2. példa: az összes tárolt hozzáférés-házirend beolvasása egy tárterület-tárolóban</span><span class="sxs-lookup"><span data-stu-id="df608-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="df608-111">Ez a parancs a Container07 nevű tároló tárolóban minden hozzáférési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="df608-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="df608-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df608-112">PARAMETERS</span></span>

### <span data-ttu-id="df608-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df608-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="df608-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="df608-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="df608-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="df608-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="df608-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="df608-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="df608-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="df608-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="df608-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="df608-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="df608-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="df608-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="df608-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="df608-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="df608-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="df608-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="df608-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="df608-122">The default value is 10.</span></span>

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

### <span data-ttu-id="df608-123">-Container</span><span class="sxs-lookup"><span data-stu-id="df608-123">-Container</span></span>
<span data-ttu-id="df608-124">Az Azure Storage tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df608-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="df608-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="df608-125">-Context</span></span>
<span data-ttu-id="df608-126">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df608-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="df608-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df608-127">-DefaultProfile</span></span>
<span data-ttu-id="df608-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df608-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df608-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="df608-129">-Policy</span></span>
<span data-ttu-id="df608-130">Az Azure tárolt hozzáférés házirendjének megadása.</span><span class="sxs-lookup"><span data-stu-id="df608-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="df608-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df608-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="df608-132">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="df608-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="df608-133">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="df608-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="df608-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df608-134">CommonParameters</span></span>
<span data-ttu-id="df608-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df608-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df608-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df608-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df608-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df608-137">INPUTS</span></span>

### <span data-ttu-id="df608-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df608-138">System.String</span></span>

### <span data-ttu-id="df608-139">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="df608-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df608-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df608-140">OUTPUTS</span></span>

### <span data-ttu-id="df608-141">Microsoft. Azure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="df608-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="df608-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df608-142">NOTES</span></span>

## <span data-ttu-id="df608-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df608-143">RELATED LINKS</span></span>

[<span data-ttu-id="df608-144">Új – AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df608-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="df608-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df608-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="df608-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df608-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


