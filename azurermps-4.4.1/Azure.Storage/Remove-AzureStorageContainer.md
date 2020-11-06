---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 0dce586ff0b129887924e22fdcb152d818bfc526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493913"
---
# <span data-ttu-id="57a7a-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="57a7a-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="57a7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="57a7a-103">Eltávolítja a megadott tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="57a7a-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57a7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57a7a-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57a7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="57a7a-106">A **Remove-AzureStorageContainer** parancsmag eltávolítja a megadott tárterületet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="57a7a-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="57a7a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="57a7a-107">EXAMPLES</span></span>

### <span data-ttu-id="57a7a-108">1. példa: tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="57a7a-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="57a7a-109">Ez a példa eltávolítja a MyTestContainer nevű tárolót.</span><span class="sxs-lookup"><span data-stu-id="57a7a-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="57a7a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57a7a-110">PARAMETERS</span></span>

### <span data-ttu-id="57a7a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="57a7a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="57a7a-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="57a7a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="57a7a-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="57a7a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="57a7a-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="57a7a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="57a7a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="57a7a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="57a7a-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="57a7a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="57a7a-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="57a7a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="57a7a-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="57a7a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="57a7a-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="57a7a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="57a7a-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="57a7a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="57a7a-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="57a7a-121">-Context</span></span>
<span data-ttu-id="57a7a-122">Az eltávolítani kívánt tároló környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57a7a-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="57a7a-123">A New-AzureStorageContext parancsmag segítségével létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="57a7a-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="57a7a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="57a7a-124">-Force</span></span>
<span data-ttu-id="57a7a-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="57a7a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57a7a-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57a7a-126">-Name</span></span>
<span data-ttu-id="57a7a-127">Az eltávolítandó tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57a7a-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57a7a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57a7a-128">-PassThru</span></span>
<span data-ttu-id="57a7a-129">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="57a7a-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="57a7a-130">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="57a7a-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="57a7a-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="57a7a-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="57a7a-132">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="57a7a-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="57a7a-133">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="57a7a-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="57a7a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57a7a-134">-Confirm</span></span>
<span data-ttu-id="57a7a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57a7a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a7a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a7a-136">-WhatIf</span></span>
<span data-ttu-id="57a7a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57a7a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a7a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57a7a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a7a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a7a-139">CommonParameters</span></span>
<span data-ttu-id="57a7a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57a7a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a7a-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57a7a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a7a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57a7a-142">INPUTS</span></span>

### <span data-ttu-id="57a7a-143">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="57a7a-143">IStorageContext</span></span>

<span data-ttu-id="57a7a-144">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="57a7a-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="57a7a-145">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="57a7a-145">String</span></span>

<span data-ttu-id="57a7a-146">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="57a7a-146">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="57a7a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57a7a-147">OUTPUTS</span></span>

### <span data-ttu-id="57a7a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57a7a-148">System.Boolean</span></span>

## <span data-ttu-id="57a7a-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57a7a-149">NOTES</span></span>

## <span data-ttu-id="57a7a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57a7a-150">RELATED LINKS</span></span>

[<span data-ttu-id="57a7a-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="57a7a-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="57a7a-152">Új – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="57a7a-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
