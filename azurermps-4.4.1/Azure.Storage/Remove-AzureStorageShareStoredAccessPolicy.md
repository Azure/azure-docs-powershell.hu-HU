---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b88a03f38ff3e88b6fbbe7b966498e547f8cc026
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493903"
---
# <span data-ttu-id="87529-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87529-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="87529-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87529-102">SYNOPSIS</span></span>
<span data-ttu-id="87529-103">Egy tárolt Access-házirend eltávolítása a tárterület-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="87529-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87529-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87529-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87529-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87529-105">DESCRIPTION</span></span>
<span data-ttu-id="87529-106">A **Remove-AzureStorageShareStoredAccessPolicy** parancsmag az Azure tárhely-megosztásból eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="87529-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="87529-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87529-107">EXAMPLES</span></span>

### <span data-ttu-id="87529-108">1. példa: a tárolt hozzáférés-házirend eltávolítása Azure-tárhelyről</span><span class="sxs-lookup"><span data-stu-id="87529-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="87529-109">Ez a parancs eltávolítja a GeneralPolicy nevű, a ContosoShare nevű, tárolt elérési házirendet.</span><span class="sxs-lookup"><span data-stu-id="87529-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="87529-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87529-110">PARAMETERS</span></span>

### <span data-ttu-id="87529-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87529-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="87529-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="87529-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="87529-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="87529-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="87529-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="87529-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="87529-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="87529-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="87529-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="87529-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="87529-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="87529-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="87529-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="87529-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="87529-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="87529-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="87529-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="87529-120">The default value is 10.</span></span>

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

### <span data-ttu-id="87529-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="87529-121">-Context</span></span>
<span data-ttu-id="87529-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87529-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="87529-123">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87529-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="87529-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87529-124">-PassThru</span></span>
<span data-ttu-id="87529-125">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="87529-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="87529-126">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="87529-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="87529-127">-Házirend</span><span class="sxs-lookup"><span data-stu-id="87529-127">-Policy</span></span>
<span data-ttu-id="87529-128">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="87529-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="87529-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87529-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="87529-130">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="87529-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="87529-131">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="87529-131">-ShareName</span></span>
<span data-ttu-id="87529-132">Annak a tárolási megosztásnak a neve, amelyhez ez a parancsmag eltávolítja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="87529-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="87529-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87529-133">-Confirm</span></span>
<span data-ttu-id="87529-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87529-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87529-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87529-135">-WhatIf</span></span>
<span data-ttu-id="87529-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87529-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87529-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87529-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87529-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87529-138">CommonParameters</span></span>
<span data-ttu-id="87529-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87529-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87529-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87529-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87529-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87529-141">INPUTS</span></span>

### <span data-ttu-id="87529-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87529-142">IStorageContext</span></span>

<span data-ttu-id="87529-143">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="87529-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="87529-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87529-144">OUTPUTS</span></span>

### <span data-ttu-id="87529-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87529-145">System.Boolean</span></span>

## <span data-ttu-id="87529-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87529-146">NOTES</span></span>

## <span data-ttu-id="87529-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87529-147">RELATED LINKS</span></span>

[<span data-ttu-id="87529-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87529-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="87529-149">Új – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87529-149">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="87529-150">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="87529-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="87529-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87529-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
