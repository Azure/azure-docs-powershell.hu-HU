---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24a61f071e806588976f601df69aa66dbbafc164
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491674"
---
# <span data-ttu-id="bbab7-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bbab7-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="bbab7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbab7-102">SYNOPSIS</span></span>
<span data-ttu-id="bbab7-103">Egy tárolt Access-házirend eltávolítása a tárterület-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="bbab7-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="bbab7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbab7-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbab7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbab7-105">DESCRIPTION</span></span>
<span data-ttu-id="bbab7-106">A **Remove-AzureStorageShareStoredAccessPolicy** parancsmag az Azure tárhely-megosztásból eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="bbab7-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="bbab7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bbab7-107">EXAMPLES</span></span>

### <span data-ttu-id="bbab7-108">1. példa: a tárolt hozzáférés-házirend eltávolítása Azure-tárhelyről</span><span class="sxs-lookup"><span data-stu-id="bbab7-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="bbab7-109">Ez a parancs eltávolítja a GeneralPolicy nevű, a ContosoShare nevű, tárolt elérési házirendet.</span><span class="sxs-lookup"><span data-stu-id="bbab7-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="bbab7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbab7-110">PARAMETERS</span></span>

### <span data-ttu-id="bbab7-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbab7-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bbab7-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="bbab7-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bbab7-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="bbab7-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bbab7-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="bbab7-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bbab7-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bbab7-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bbab7-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbab7-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bbab7-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="bbab7-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bbab7-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="bbab7-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bbab7-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="bbab7-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bbab7-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="bbab7-120">The default value is 10.</span></span>

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

### <span data-ttu-id="bbab7-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bbab7-121">-Context</span></span>
<span data-ttu-id="bbab7-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbab7-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bbab7-123">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bbab7-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bbab7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbab7-124">-PassThru</span></span>
<span data-ttu-id="bbab7-125">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="bbab7-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="bbab7-126">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="bbab7-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bbab7-127">-Házirend</span><span class="sxs-lookup"><span data-stu-id="bbab7-127">-Policy</span></span>
<span data-ttu-id="bbab7-128">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="bbab7-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbab7-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbab7-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bbab7-130">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbab7-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bbab7-131">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="bbab7-131">-ShareName</span></span>
<span data-ttu-id="bbab7-132">Annak a tárolási megosztásnak a neve, amelyhez ez a parancsmag eltávolítja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="bbab7-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbab7-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbab7-133">-Confirm</span></span>
<span data-ttu-id="bbab7-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbab7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbab7-135">-WhatIf</span></span>
<span data-ttu-id="bbab7-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbab7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbab7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbab7-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbab7-138">CommonParameters</span></span>
<span data-ttu-id="bbab7-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbab7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbab7-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbab7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbab7-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbab7-141">INPUTS</span></span>

## <span data-ttu-id="bbab7-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbab7-142">OUTPUTS</span></span>

## <span data-ttu-id="bbab7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbab7-143">NOTES</span></span>

## <span data-ttu-id="bbab7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbab7-144">RELATED LINKS</span></span>

[<span data-ttu-id="bbab7-145">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bbab7-145">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="bbab7-146">Új – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bbab7-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="bbab7-147">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbab7-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bbab7-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bbab7-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
