---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24b4ddfa86027885b5094b164f24da36e9604900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491312"
---
# <span data-ttu-id="f18ab-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="f18ab-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="f18ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f18ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f18ab-103">Töröl egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="f18ab-103">Deletes a file.</span></span>

## <span data-ttu-id="f18ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f18ab-104">SYNTAX</span></span>

### <span data-ttu-id="f18ab-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f18ab-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f18ab-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="f18ab-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f18ab-107">Directory</span><span class="sxs-lookup"><span data-stu-id="f18ab-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f18ab-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="f18ab-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f18ab-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f18ab-109">DESCRIPTION</span></span>
<span data-ttu-id="f18ab-110">A **Remove-AzureStorageFile** parancsmag töröl egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="f18ab-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="f18ab-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f18ab-111">EXAMPLES</span></span>

### <span data-ttu-id="f18ab-112">1. példa: fájl törlése a fájl-megosztásból</span><span class="sxs-lookup"><span data-stu-id="f18ab-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="f18ab-113">Ez a parancs törli a ContosoFile22 nevű fájlt a ContosoShare06 nevű fájlmegosztás-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="f18ab-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="f18ab-114">2. példa: fájlmegosztás-objektum használatával beolvashatja a fájlt a fájlból.</span><span class="sxs-lookup"><span data-stu-id="f18ab-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="f18ab-115">Ez a parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beszerzéséhez, majd a csővezeték-kezelő segítségével átadja az objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="f18ab-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f18ab-116">A jelenlegi parancs törli a ContosoFile22 nevű fájlt a ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f18ab-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="f18ab-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f18ab-117">PARAMETERS</span></span>

### <span data-ttu-id="f18ab-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f18ab-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f18ab-119">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="f18ab-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f18ab-120">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="f18ab-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f18ab-121">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="f18ab-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f18ab-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f18ab-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f18ab-123">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="f18ab-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f18ab-124">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="f18ab-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f18ab-125">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="f18ab-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f18ab-126">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="f18ab-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f18ab-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="f18ab-127">The default value is 10.</span></span>

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

### <span data-ttu-id="f18ab-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f18ab-128">-Context</span></span>
<span data-ttu-id="f18ab-129">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f18ab-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f18ab-130">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f18ab-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f18ab-131">-Címtár</span><span class="sxs-lookup"><span data-stu-id="f18ab-131">-Directory</span></span>
<span data-ttu-id="f18ab-132">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="f18ab-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="f18ab-133">Ez a parancsmag eltávolítja a fájl azon mappáját, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f18ab-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="f18ab-134">-Fájl</span><span class="sxs-lookup"><span data-stu-id="f18ab-134">-File</span></span>
<span data-ttu-id="f18ab-135">A fájlt **CloudFile** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="f18ab-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="f18ab-136">Ez a parancsmag eltávolítja a paraméter által megadott fájlt.</span><span class="sxs-lookup"><span data-stu-id="f18ab-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="f18ab-137">**CloudFile** objektum beolvasásához használja az Get-AzureStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f18ab-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f18ab-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f18ab-138">-PassThru</span></span>
<span data-ttu-id="f18ab-139">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="f18ab-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f18ab-140">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="f18ab-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f18ab-141">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="f18ab-141">-Path</span></span>
<span data-ttu-id="f18ab-142">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f18ab-142">Specifies the path of a file.</span></span>
<span data-ttu-id="f18ab-143">Ez a parancsmag törli a paraméter által megadott fájlt.</span><span class="sxs-lookup"><span data-stu-id="f18ab-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f18ab-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f18ab-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f18ab-145">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f18ab-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f18ab-146">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="f18ab-146">-Share</span></span>
<span data-ttu-id="f18ab-147">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f18ab-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f18ab-148">Ez a parancsmag eltávolítja a fájlt a megosztás ebben a paraméterben beállításban.</span><span class="sxs-lookup"><span data-stu-id="f18ab-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="f18ab-149">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f18ab-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="f18ab-150">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f18ab-150">This object contains the storage context.</span></span>
<span data-ttu-id="f18ab-151">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f18ab-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="f18ab-152">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="f18ab-152">-ShareName</span></span>
<span data-ttu-id="f18ab-153">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="f18ab-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="f18ab-154">Ez a parancsmag eltávolítja a fájlt a megosztás ebben a paraméterben beállításban.</span><span class="sxs-lookup"><span data-stu-id="f18ab-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="f18ab-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f18ab-155">-Confirm</span></span>
<span data-ttu-id="f18ab-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f18ab-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f18ab-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f18ab-157">-WhatIf</span></span>
<span data-ttu-id="f18ab-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f18ab-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f18ab-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f18ab-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f18ab-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f18ab-160">CommonParameters</span></span>
<span data-ttu-id="f18ab-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f18ab-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f18ab-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f18ab-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f18ab-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f18ab-163">INPUTS</span></span>

## <span data-ttu-id="f18ab-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f18ab-164">OUTPUTS</span></span>

## <span data-ttu-id="f18ab-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f18ab-165">NOTES</span></span>

## <span data-ttu-id="f18ab-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f18ab-166">RELATED LINKS</span></span>

[<span data-ttu-id="f18ab-167">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="f18ab-167">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="f18ab-168">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f18ab-168">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="f18ab-169">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f18ab-169">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
