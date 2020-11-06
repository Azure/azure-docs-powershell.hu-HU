---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 66662899694f7b1fb93dd109e1dccefee5e00182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503360"
---
# <span data-ttu-id="4a3a5-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4a3a5-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="4a3a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3a5-103">Fájl megosztásának törlése</span><span class="sxs-lookup"><span data-stu-id="4a3a5-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a3a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a3a5-104">SYNTAX</span></span>

### <span data-ttu-id="4a3a5-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a3a5-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3a5-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="4a3a5-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a3a5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a3a5-107">DESCRIPTION</span></span>
<span data-ttu-id="4a3a5-108">A **Remove-AzureStorageShare** parancsmag törli a fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="4a3a5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4a3a5-109">EXAMPLES</span></span>

### <span data-ttu-id="4a3a5-110">1. példa: fájlmegosztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4a3a5-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4a3a5-111">Ez a parancs eltávolítja a ContosoShare06 nevű fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="4a3a5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a3a5-112">PARAMETERS</span></span>

### <span data-ttu-id="4a3a5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4a3a5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4a3a5-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4a3a5-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4a3a5-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4a3a5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4a3a5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4a3a5-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4a3a5-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4a3a5-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4a3a5-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="4a3a5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4a3a5-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="4a3a5-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4a3a5-123">-Context</span></span>
<span data-ttu-id="4a3a5-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4a3a5-125">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4a3a5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4a3a5-126">-Force</span></span>
<span data-ttu-id="4a3a5-127">A megosztás és az összes tartalom eltávolításának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="4a3a5-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="4a3a5-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a3a5-128">-Name</span></span>
<span data-ttu-id="4a3a5-129">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="4a3a5-130">Ez a parancsmag törli azt a fájlt, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a3a5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a3a5-131">-PassThru</span></span>
<span data-ttu-id="4a3a5-132">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4a3a5-133">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4a3a5-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4a3a5-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4a3a5-135">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4a3a5-136">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="4a3a5-136">-Share</span></span>
<span data-ttu-id="4a3a5-137">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4a3a5-138">Ez a parancsmag eltávolítja azt az objektumot, amelyre a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="4a3a5-139">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="4a3a5-140">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-140">This object contains the storage context.</span></span>
<span data-ttu-id="4a3a5-141">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="4a3a5-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a3a5-142">-Confirm</span></span>
<span data-ttu-id="4a3a5-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3a5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3a5-144">-WhatIf</span></span>
<span data-ttu-id="4a3a5-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a3a5-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a3a5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3a5-147">CommonParameters</span></span>
<span data-ttu-id="4a3a5-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a3a5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3a5-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a3a5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3a5-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a3a5-150">INPUTS</span></span>

### <span data-ttu-id="4a3a5-151">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a3a5-151">IStorageContext</span></span>

<span data-ttu-id="4a3a5-152">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4a3a5-152">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4a3a5-153">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="4a3a5-153">String</span></span>

<span data-ttu-id="4a3a5-154">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4a3a5-154">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4a3a5-155">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4a3a5-155">CloudFileShare</span></span>

<span data-ttu-id="4a3a5-156">A "share" paraméter értéke "CloudFileShare" típusú értéket ad a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4a3a5-156">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="4a3a5-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a3a5-157">OUTPUTS</span></span>

## <span data-ttu-id="4a3a5-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a3a5-158">NOTES</span></span>

## <span data-ttu-id="4a3a5-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a3a5-159">RELATED LINKS</span></span>

[<span data-ttu-id="4a3a5-160">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4a3a5-160">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4a3a5-161">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a3a5-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4a3a5-162">Új – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4a3a5-162">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
