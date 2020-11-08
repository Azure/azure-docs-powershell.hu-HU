---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187986"
---
# <span data-ttu-id="7a5bd-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7a5bd-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="7a5bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5bd-103">Címtár törlése</span><span class="sxs-lookup"><span data-stu-id="7a5bd-103">Deletes a directory.</span></span>

## <span data-ttu-id="7a5bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a5bd-104">SYNTAX</span></span>

### <span data-ttu-id="7a5bd-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a5bd-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a5bd-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="7a5bd-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a5bd-107">Directory</span><span class="sxs-lookup"><span data-stu-id="7a5bd-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a5bd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a5bd-108">DESCRIPTION</span></span>
<span data-ttu-id="7a5bd-109">A **Remove-AzStorageDirectory** parancsmag törli a címtárat.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="7a5bd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7a5bd-110">EXAMPLES</span></span>

### <span data-ttu-id="7a5bd-111">Példa 1: mappa törlése</span><span class="sxs-lookup"><span data-stu-id="7a5bd-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="7a5bd-112">Ez a parancs törli a ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztás-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="7a5bd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a5bd-113">PARAMETERS</span></span>

### <span data-ttu-id="7a5bd-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a5bd-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7a5bd-115">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7a5bd-116">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7a5bd-117">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7a5bd-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7a5bd-119">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7a5bd-120">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7a5bd-121">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7a5bd-122">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="7a5bd-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7a5bd-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-123">The default value is 10.</span></span>

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

### <span data-ttu-id="7a5bd-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7a5bd-124">-Context</span></span>
<span data-ttu-id="7a5bd-125">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7a5bd-126">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5bd-127">-DefaultProfile</span></span>
<span data-ttu-id="7a5bd-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-129">-Címtár</span><span class="sxs-lookup"><span data-stu-id="7a5bd-129">-Directory</span></span>
<span data-ttu-id="7a5bd-130">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7a5bd-131">Ez a parancsmag eltávolítja a paraméter által megadott mappát.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="7a5bd-132">Címtár beolvasásához használja az New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7a5bd-133">A **Get-AzStorageFile** parancsmag használatával is beszerezhet egy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a5bd-134">-PassThru</span></span>
<span data-ttu-id="7a5bd-135">Jelzi, hogy ha a parancsmag sikeres, akkor az $True értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="7a5bd-136">Ha ezt a paramétert adja meg, és a parancsmag sikertelen, mert az _elérésiút_ -paraméter nem megfelelő, a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="7a5bd-137">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="7a5bd-138">-Path</span></span>
<span data-ttu-id="7a5bd-139">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="7a5bd-140">Ha a paramétert tartalmazó mappa üres, ez a parancsmag törli azt a mappát.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="7a5bd-141">Ha a mappa nem üres, ez a parancsmag nem változtatja meg a problémát, és hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a5bd-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7a5bd-143">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-143">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-144">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="7a5bd-144">-Share</span></span>
<span data-ttu-id="7a5bd-145">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7a5bd-146">Ez a parancsmag eltávolítja a mappa alatti fájlt, amely a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="7a5bd-147">**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="7a5bd-148">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-148">This object contains the storage context.</span></span>
<span data-ttu-id="7a5bd-149">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-150">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="7a5bd-150">-ShareName</span></span>
<span data-ttu-id="7a5bd-151">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="7a5bd-152">Ez a parancsmag eltávolítja a mappa alatti fájlt, amely a következő paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a5bd-153">-Confirm</span></span>
<span data-ttu-id="7a5bd-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5bd-155">-WhatIf</span></span>
<span data-ttu-id="7a5bd-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a5bd-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a5bd-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5bd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5bd-158">CommonParameters</span></span>
<span data-ttu-id="7a5bd-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a5bd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5bd-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a5bd-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5bd-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a5bd-161">INPUTS</span></span>

### <span data-ttu-id="7a5bd-162">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7a5bd-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="7a5bd-163">Microsoft. Azure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7a5bd-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="7a5bd-164">System. String</span><span class="sxs-lookup"><span data-stu-id="7a5bd-164">System.String</span></span>

### <span data-ttu-id="7a5bd-165">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a5bd-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7a5bd-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a5bd-166">OUTPUTS</span></span>

### <span data-ttu-id="7a5bd-167">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7a5bd-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="7a5bd-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a5bd-168">NOTES</span></span>

## <span data-ttu-id="7a5bd-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a5bd-169">RELATED LINKS</span></span>

[<span data-ttu-id="7a5bd-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="7a5bd-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="7a5bd-171">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a5bd-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7a5bd-172">Új – AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7a5bd-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
