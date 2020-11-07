---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 0b734acb6d1a0d491a0b9e6397f7ae9af2645b35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848585"
---
# <span data-ttu-id="442ab-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="442ab-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="442ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="442ab-102">SYNOPSIS</span></span>
<span data-ttu-id="442ab-103">Beolvassa a tárolt hozzáférés házirendjének vagy házirendjeinek egy Azure Storage tárolót.</span><span class="sxs-lookup"><span data-stu-id="442ab-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="442ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="442ab-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="442ab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="442ab-105">DESCRIPTION</span></span>
<span data-ttu-id="442ab-106">A **Get-AzureStorageContainerStoredAccessPolicy** parancsmag felsorolja az Azure-tárolók tárolt hozzáférési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="442ab-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="442ab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="442ab-107">EXAMPLES</span></span>

### <span data-ttu-id="442ab-108">Példa 1: tárolt hozzáférés-házirend beszerzése tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="442ab-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="442ab-109">Ez a parancs a Policy22 nevű Access-házirendet a Container07 nevű tároló tárolóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="442ab-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="442ab-110">2. példa: az összes tárolt hozzáférés-házirend beolvasása egy tárterület-tárolóban</span><span class="sxs-lookup"><span data-stu-id="442ab-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="442ab-111">Ez a parancs a Container07 nevű tároló tárolóban minden hozzáférési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="442ab-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="442ab-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="442ab-112">PARAMETERS</span></span>

### <span data-ttu-id="442ab-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="442ab-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="442ab-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="442ab-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="442ab-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="442ab-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="442ab-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="442ab-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="442ab-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="442ab-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="442ab-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="442ab-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="442ab-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="442ab-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="442ab-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="442ab-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="442ab-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="442ab-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="442ab-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="442ab-122">The default value is 10.</span></span>

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

### <span data-ttu-id="442ab-123">-Container</span><span class="sxs-lookup"><span data-stu-id="442ab-123">-Container</span></span>
<span data-ttu-id="442ab-124">Az Azure Storage tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442ab-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="442ab-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="442ab-125">-Context</span></span>
<span data-ttu-id="442ab-126">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442ab-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="442ab-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442ab-127">-DefaultProfile</span></span>
<span data-ttu-id="442ab-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="442ab-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442ab-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="442ab-129">-Policy</span></span>
<span data-ttu-id="442ab-130">Az Azure tárolt hozzáférés házirendjének megadása.</span><span class="sxs-lookup"><span data-stu-id="442ab-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="442ab-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="442ab-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="442ab-132">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="442ab-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="442ab-133">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="442ab-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="442ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442ab-134">CommonParameters</span></span>
<span data-ttu-id="442ab-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="442ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442ab-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442ab-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442ab-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="442ab-137">INPUTS</span></span>

### <span data-ttu-id="442ab-138">System. String</span><span class="sxs-lookup"><span data-stu-id="442ab-138">System.String</span></span>

### <span data-ttu-id="442ab-139">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="442ab-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="442ab-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="442ab-140">OUTPUTS</span></span>

### <span data-ttu-id="442ab-141">Microsoft. WindowsAzure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="442ab-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="442ab-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="442ab-142">NOTES</span></span>

## <span data-ttu-id="442ab-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="442ab-143">RELATED LINKS</span></span>

[<span data-ttu-id="442ab-144">Új – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="442ab-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="442ab-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="442ab-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="442ab-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="442ab-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)

