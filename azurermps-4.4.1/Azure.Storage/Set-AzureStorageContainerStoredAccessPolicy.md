---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 63fd207c9d3348e17718f6d4ad8dbd53a09752af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680000"
---
# <span data-ttu-id="51bf2-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51bf2-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="51bf2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="51bf2-103">Egy, az Azure-tároló tárolójának tárolt hozzáférési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="51bf2-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51bf2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51bf2-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51bf2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51bf2-105">DESCRIPTION</span></span>
<span data-ttu-id="51bf2-106">A **set-AzureStorageContainerStoredAccessPolicy** parancsmag az Azure-tárolók tárolt elérési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="51bf2-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="51bf2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51bf2-107">EXAMPLES</span></span>

### <span data-ttu-id="51bf2-108">1. példa: tárolt hozzáférés-házirend beállítása egy tárterület-tárolóban teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="51bf2-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="51bf2-109">Ez a parancs a Policy06 nevű, MyContainer nevű tárterület-tároló elérési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="51bf2-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="51bf2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51bf2-110">PARAMETERS</span></span>

### <span data-ttu-id="51bf2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51bf2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="51bf2-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="51bf2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="51bf2-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="51bf2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="51bf2-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="51bf2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="51bf2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="51bf2-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="51bf2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="51bf2-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="51bf2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="51bf2-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="51bf2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="51bf2-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="51bf2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="51bf2-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="51bf2-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-121">-Container</span><span class="sxs-lookup"><span data-stu-id="51bf2-121">-Container</span></span>
<span data-ttu-id="51bf2-122">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51bf2-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="51bf2-123">-Context</span></span>
<span data-ttu-id="51bf2-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51bf2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="51bf2-125">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="51bf2-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="51bf2-126">-ExpiryTime</span></span>
<span data-ttu-id="51bf2-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="51bf2-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="51bf2-128">-NoExpiryTime</span></span>
<span data-ttu-id="51bf2-129">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="51bf2-129">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="51bf2-130">-NoStartTime</span></span>
<span data-ttu-id="51bf2-131">A $Null kezdési időpontját állítja be.</span><span class="sxs-lookup"><span data-stu-id="51bf2-131">Sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-132">– Engedély</span><span class="sxs-lookup"><span data-stu-id="51bf2-132">-Permission</span></span>
<span data-ttu-id="51bf2-133">A tároló elérési házirendjében található engedélyeket adja meg a tároló tároló eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="51bf2-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-134">-Házirend</span><span class="sxs-lookup"><span data-stu-id="51bf2-134">-Policy</span></span>
<span data-ttu-id="51bf2-135">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51bf2-135">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51bf2-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="51bf2-137">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="51bf2-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="51bf2-138">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="51bf2-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="51bf2-139">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="51bf2-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-140">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="51bf2-140">-StartTime</span></span>
<span data-ttu-id="51bf2-141">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="51bf2-141">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51bf2-142">-Confirm</span></span>
<span data-ttu-id="51bf2-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51bf2-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51bf2-144">-WhatIf</span></span>
<span data-ttu-id="51bf2-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51bf2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51bf2-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51bf2-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bf2-147">CommonParameters</span></span>
<span data-ttu-id="51bf2-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51bf2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bf2-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51bf2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bf2-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51bf2-150">INPUTS</span></span>

### <span data-ttu-id="51bf2-151">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="51bf2-151">String</span></span>

<span data-ttu-id="51bf2-152">A "Container" paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="51bf2-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="51bf2-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="51bf2-153">IStorageContext</span></span>

<span data-ttu-id="51bf2-154">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="51bf2-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="51bf2-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51bf2-155">OUTPUTS</span></span>

### <span data-ttu-id="51bf2-156">System. String</span><span class="sxs-lookup"><span data-stu-id="51bf2-156">System.String</span></span>

## <span data-ttu-id="51bf2-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51bf2-157">NOTES</span></span>

## <span data-ttu-id="51bf2-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51bf2-158">RELATED LINKS</span></span>

[<span data-ttu-id="51bf2-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51bf2-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="51bf2-160">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="51bf2-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="51bf2-161">Új – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51bf2-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="51bf2-162">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51bf2-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
