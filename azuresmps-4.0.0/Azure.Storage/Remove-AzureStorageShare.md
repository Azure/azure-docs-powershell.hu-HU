---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491316"
---
# <span data-ttu-id="a794d-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a794d-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="a794d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a794d-102">SYNOPSIS</span></span>
<span data-ttu-id="a794d-103">Fájl megosztásának törlése</span><span class="sxs-lookup"><span data-stu-id="a794d-103">Deletes a file share.</span></span>

## <span data-ttu-id="a794d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a794d-104">SYNTAX</span></span>

### <span data-ttu-id="a794d-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a794d-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a794d-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="a794d-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a794d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a794d-107">DESCRIPTION</span></span>
<span data-ttu-id="a794d-108">A **Remove-AzureStorageShare** parancsmag törli a fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="a794d-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="a794d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a794d-109">EXAMPLES</span></span>

### <span data-ttu-id="a794d-110">1. példa: fájlmegosztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a794d-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="a794d-111">Ez a parancs eltávolítja a ContosoShare06 nevű fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="a794d-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="a794d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a794d-112">PARAMETERS</span></span>

### <span data-ttu-id="a794d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a794d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a794d-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="a794d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a794d-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="a794d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a794d-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a794d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a794d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a794d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a794d-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a794d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a794d-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a794d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a794d-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="a794d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a794d-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="a794d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a794d-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a794d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a794d-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a794d-123">-Context</span></span>
<span data-ttu-id="a794d-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a794d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a794d-125">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a794d-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a794d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a794d-126">-Force</span></span>
<span data-ttu-id="a794d-127">A megosztás és az összes tartalom eltávolításának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="a794d-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="a794d-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a794d-128">-Name</span></span>
<span data-ttu-id="a794d-129">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="a794d-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="a794d-130">Ez a parancsmag törli azt a fájlt, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a794d-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a794d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a794d-131">-PassThru</span></span>
<span data-ttu-id="a794d-132">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="a794d-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a794d-133">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="a794d-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a794d-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a794d-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a794d-135">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a794d-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a794d-136">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="a794d-136">-Share</span></span>
<span data-ttu-id="a794d-137">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a794d-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a794d-138">Ez a parancsmag eltávolítja azt az objektumot, amelyre a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="a794d-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="a794d-139">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a794d-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="a794d-140">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a794d-140">This object contains the storage context.</span></span>
<span data-ttu-id="a794d-141">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a794d-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a794d-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a794d-142">-Confirm</span></span>
<span data-ttu-id="a794d-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a794d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a794d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a794d-144">-WhatIf</span></span>
<span data-ttu-id="a794d-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a794d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a794d-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a794d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a794d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a794d-147">CommonParameters</span></span>
<span data-ttu-id="a794d-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a794d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a794d-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a794d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a794d-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a794d-150">INPUTS</span></span>

## <span data-ttu-id="a794d-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a794d-151">OUTPUTS</span></span>

## <span data-ttu-id="a794d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a794d-152">NOTES</span></span>

## <span data-ttu-id="a794d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a794d-153">RELATED LINKS</span></span>

[<span data-ttu-id="a794d-154">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a794d-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a794d-155">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a794d-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a794d-156">Új – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a794d-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
