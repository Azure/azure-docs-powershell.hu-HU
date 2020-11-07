---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: cdd52b1e1bab28956605d70e1089d7804b8ccff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672888"
---
# <span data-ttu-id="b5203-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b5203-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="b5203-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5203-102">SYNOPSIS</span></span>
<span data-ttu-id="b5203-103">Címtár törlése</span><span class="sxs-lookup"><span data-stu-id="b5203-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5203-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5203-104">SYNTAX</span></span>

### <span data-ttu-id="b5203-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5203-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5203-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="b5203-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5203-107">Directory</span><span class="sxs-lookup"><span data-stu-id="b5203-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5203-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5203-108">DESCRIPTION</span></span>
<span data-ttu-id="b5203-109">A **Remove-AzureStorageDirectory** parancsmag törli a címtárat.</span><span class="sxs-lookup"><span data-stu-id="b5203-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="b5203-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b5203-110">EXAMPLES</span></span>

### <span data-ttu-id="b5203-111">Példa 1: mappa törlése</span><span class="sxs-lookup"><span data-stu-id="b5203-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="b5203-112">Ez a parancs törli a ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztás-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="b5203-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="b5203-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5203-113">PARAMETERS</span></span>

### <span data-ttu-id="b5203-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5203-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b5203-115">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="b5203-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b5203-116">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="b5203-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b5203-117">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b5203-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b5203-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b5203-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b5203-119">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5203-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b5203-120">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="b5203-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b5203-121">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="b5203-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b5203-122">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="b5203-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b5203-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b5203-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b5203-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b5203-124">-Context</span></span>
<span data-ttu-id="b5203-125">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5203-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b5203-126">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b5203-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b5203-127">-Címtár</span><span class="sxs-lookup"><span data-stu-id="b5203-127">-Directory</span></span>
<span data-ttu-id="b5203-128">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="b5203-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b5203-129">Ez a parancsmag eltávolítja a paraméter által megadott mappát.</span><span class="sxs-lookup"><span data-stu-id="b5203-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="b5203-130">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b5203-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b5203-131">A **Get-AzureStorageFile** parancsmag használatával is beszerezhet egy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="b5203-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5203-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5203-132">-PassThru</span></span>
<span data-ttu-id="b5203-133">Jelzi, hogy ha a parancsmag sikeres, akkor az $True értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b5203-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="b5203-134">Ha ezt a paramétert adja meg, és a parancsmag sikertelen, mert az _elérésiút_ -paraméter nem megfelelő, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b5203-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="b5203-135">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="b5203-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b5203-136">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b5203-136">-Path</span></span>
<span data-ttu-id="b5203-137">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5203-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="b5203-138">Ha a paramétert tartalmazó mappa üres, ez a parancsmag törli azt a mappát.</span><span class="sxs-lookup"><span data-stu-id="b5203-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="b5203-139">Ha a mappa nem üres, ez a parancsmag nem változtatja meg a problémát, és hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="b5203-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5203-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5203-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b5203-141">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5203-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b5203-142">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="b5203-142">-Share</span></span>
<span data-ttu-id="b5203-143">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b5203-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b5203-144">Ez a parancsmag eltávolítja a mappa alatti fájlt, amely a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5203-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="b5203-145">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b5203-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="b5203-146">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b5203-146">This object contains the storage context.</span></span>
<span data-ttu-id="b5203-147">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b5203-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b5203-148">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="b5203-148">-ShareName</span></span>
<span data-ttu-id="b5203-149">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="b5203-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="b5203-150">Ez a parancsmag eltávolítja a mappa alatti fájlt, amely a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5203-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5203-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5203-151">-Confirm</span></span>
<span data-ttu-id="b5203-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5203-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5203-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5203-153">-WhatIf</span></span>
<span data-ttu-id="b5203-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5203-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5203-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5203-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5203-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5203-156">CommonParameters</span></span>
<span data-ttu-id="b5203-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5203-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5203-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5203-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5203-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5203-159">INPUTS</span></span>

### <span data-ttu-id="b5203-160">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5203-160">IStorageContext</span></span>

<span data-ttu-id="b5203-161">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b5203-161">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b5203-162">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b5203-162">CloudFileDirectory</span></span>

<span data-ttu-id="b5203-163">A "címtár" paraméter elfogadja a "CloudFileDirectory" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b5203-163">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="b5203-164">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b5203-164">CloudFileShare</span></span>

<span data-ttu-id="b5203-165">A "share" paraméter értéke "CloudFileShare" típusú értéket ad a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b5203-165">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="b5203-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5203-166">OUTPUTS</span></span>

## <span data-ttu-id="b5203-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5203-167">NOTES</span></span>

## <span data-ttu-id="b5203-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5203-168">RELATED LINKS</span></span>

[<span data-ttu-id="b5203-169">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b5203-169">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="b5203-170">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5203-170">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b5203-171">Új – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b5203-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
