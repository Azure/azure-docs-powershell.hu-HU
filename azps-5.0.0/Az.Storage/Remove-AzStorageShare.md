---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185800"
---
# <span data-ttu-id="4e694-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4e694-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="4e694-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e694-102">SYNOPSIS</span></span>
<span data-ttu-id="4e694-103">Fájl megosztásának törlése</span><span class="sxs-lookup"><span data-stu-id="4e694-103">Deletes a file share.</span></span>

## <span data-ttu-id="4e694-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e694-104">SYNTAX</span></span>

### <span data-ttu-id="4e694-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e694-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e694-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="4e694-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e694-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e694-107">DESCRIPTION</span></span>
<span data-ttu-id="4e694-108">A **Remove-AzStorageShare** parancsmag törli a fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="4e694-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="4e694-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4e694-109">EXAMPLES</span></span>

### <span data-ttu-id="4e694-110">1. példa: fájlmegosztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4e694-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4e694-111">Ez a parancs eltávolítja a ContosoShare06 nevű fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="4e694-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="4e694-112">2. példa: fájl megosztásának és minden pillanatképének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4e694-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="4e694-113">A parancs eltávolítja a ContosoShare06 nevű fájlt és annak összes pillanatképét.</span><span class="sxs-lookup"><span data-stu-id="4e694-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="4e694-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e694-114">PARAMETERS</span></span>

### <span data-ttu-id="4e694-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e694-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4e694-116">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="4e694-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4e694-117">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="4e694-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4e694-118">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="4e694-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4e694-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4e694-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4e694-120">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e694-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4e694-121">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="4e694-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4e694-122">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="4e694-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4e694-123">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="4e694-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4e694-124">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="4e694-124">The default value is 10.</span></span>

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

### <span data-ttu-id="4e694-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4e694-125">-Context</span></span>
<span data-ttu-id="4e694-126">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e694-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4e694-127">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4e694-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4e694-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e694-128">-DefaultProfile</span></span>
<span data-ttu-id="4e694-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e694-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e694-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4e694-130">-Force</span></span>
<span data-ttu-id="4e694-131">Kényszerítheti a megosztás eltávolítását az összes pillanatképével, valamint a teljes tartalommal.</span><span class="sxs-lookup"><span data-stu-id="4e694-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="4e694-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="4e694-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="4e694-133">A fájl megosztásának megszüntetése az összes pillanatképével</span><span class="sxs-lookup"><span data-stu-id="4e694-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="4e694-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e694-134">-Name</span></span>
<span data-ttu-id="4e694-135">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="4e694-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="4e694-136">Ez a parancsmag törli azt a fájlt, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="4e694-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e694-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e694-137">-PassThru</span></span>
<span data-ttu-id="4e694-138">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="4e694-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4e694-139">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="4e694-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4e694-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e694-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4e694-141">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e694-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4e694-142">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="4e694-142">-Share</span></span>
<span data-ttu-id="4e694-143">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4e694-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4e694-144">Ez a parancsmag eltávolítja azt az objektumot, amelyre a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="4e694-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="4e694-145">**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4e694-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="4e694-146">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4e694-146">This object contains the storage context.</span></span>
<span data-ttu-id="4e694-147">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="4e694-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="4e694-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e694-148">-Confirm</span></span>
<span data-ttu-id="4e694-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e694-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e694-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e694-150">-WhatIf</span></span>
<span data-ttu-id="4e694-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e694-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e694-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e694-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e694-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e694-153">CommonParameters</span></span>
<span data-ttu-id="4e694-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e694-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e694-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e694-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e694-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e694-156">INPUTS</span></span>

### <span data-ttu-id="4e694-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4e694-157">System.String</span></span>

### <span data-ttu-id="4e694-158">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4e694-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4e694-159">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e694-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e694-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e694-160">OUTPUTS</span></span>

### <span data-ttu-id="4e694-161">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="4e694-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="4e694-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e694-162">NOTES</span></span>

## <span data-ttu-id="4e694-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e694-163">RELATED LINKS</span></span>

[<span data-ttu-id="4e694-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4e694-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4e694-165">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e694-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4e694-166">Új – AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4e694-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
