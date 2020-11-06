---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: c929a7e3e685fd870c57ff942262a0c5ac4a9966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493298"
---
# <span data-ttu-id="7e719-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e719-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="7e719-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e719-102">SYNOPSIS</span></span>
<span data-ttu-id="7e719-103">Fájl megosztásának törlése</span><span class="sxs-lookup"><span data-stu-id="7e719-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e719-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e719-104">SYNTAX</span></span>

### <span data-ttu-id="7e719-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e719-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e719-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="7e719-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e719-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e719-107">DESCRIPTION</span></span>
<span data-ttu-id="7e719-108">A **Remove-AzureStorageShare** parancsmag törli a fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="7e719-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="7e719-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7e719-109">EXAMPLES</span></span>

### <span data-ttu-id="7e719-110">1. példa: fájlmegosztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7e719-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="7e719-111">Ez a parancs eltávolítja a ContosoShare06 nevű fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="7e719-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="7e719-112">2. példa: fájl megosztásának és minden pillanatképének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7e719-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="7e719-113">A parancs eltávolítja a ContosoShare06 nevű fájlt és annak összes pillanatképét.</span><span class="sxs-lookup"><span data-stu-id="7e719-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="7e719-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e719-114">PARAMETERS</span></span>

### <span data-ttu-id="7e719-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e719-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7e719-116">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="7e719-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7e719-117">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="7e719-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7e719-118">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7e719-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7e719-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7e719-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7e719-120">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e719-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7e719-121">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="7e719-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7e719-122">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="7e719-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7e719-123">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="7e719-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7e719-124">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7e719-124">The default value is 10.</span></span>

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

### <span data-ttu-id="7e719-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7e719-125">-Context</span></span>
<span data-ttu-id="7e719-126">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e719-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7e719-127">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e719-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7e719-128">-Force</span><span class="sxs-lookup"><span data-stu-id="7e719-128">-Force</span></span>
<span data-ttu-id="7e719-129">Kényszerítheti a megosztás eltávolítását az összes pillanatképével, valamint a teljes tartalommal.</span><span class="sxs-lookup"><span data-stu-id="7e719-129">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="7e719-130">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="7e719-130">-IncludeAllSnapshot</span></span>
<span data-ttu-id="7e719-131">A fájl megosztásának megszüntetése az összes pillanatképével</span><span class="sxs-lookup"><span data-stu-id="7e719-131">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="7e719-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e719-132">-Name</span></span>
<span data-ttu-id="7e719-133">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="7e719-133">Specifies the name of the file share.</span></span>
<span data-ttu-id="7e719-134">Ez a parancsmag törli azt a fájlt, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7e719-134">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e719-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e719-135">-PassThru</span></span>
<span data-ttu-id="7e719-136">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="7e719-136">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7e719-137">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="7e719-137">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7e719-138">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e719-138">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7e719-139">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e719-139">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7e719-140">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="7e719-140">-Share</span></span>
<span data-ttu-id="7e719-141">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7e719-141">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7e719-142">Ez a parancsmag eltávolítja azt az objektumot, amelyre a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="7e719-142">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="7e719-143">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e719-143">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="7e719-144">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7e719-144">This object contains the storage context.</span></span>
<span data-ttu-id="7e719-145">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="7e719-145">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="7e719-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e719-146">-Confirm</span></span>
<span data-ttu-id="7e719-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e719-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e719-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e719-148">-WhatIf</span></span>
<span data-ttu-id="7e719-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e719-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e719-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e719-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e719-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e719-151">CommonParameters</span></span>
<span data-ttu-id="7e719-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e719-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e719-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e719-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e719-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e719-154">INPUTS</span></span>

### <span data-ttu-id="7e719-155">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e719-155">IStorageContext</span></span>

<span data-ttu-id="7e719-156">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7e719-156">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7e719-157">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="7e719-157">String</span></span>

<span data-ttu-id="7e719-158">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7e719-158">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7e719-159">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7e719-159">CloudFileShare</span></span>

<span data-ttu-id="7e719-160">A "share" paraméter értéke "CloudFileShare" típusú értéket ad a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7e719-160">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="7e719-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e719-161">OUTPUTS</span></span>

## <span data-ttu-id="7e719-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e719-162">NOTES</span></span>

## <span data-ttu-id="7e719-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e719-163">RELATED LINKS</span></span>

[<span data-ttu-id="7e719-164">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e719-164">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="7e719-165">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e719-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7e719-166">Új – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e719-166">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
