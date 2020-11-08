---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180762"
---
# <span data-ttu-id="96e09-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96e09-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="96e09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96e09-102">SYNOPSIS</span></span>
<span data-ttu-id="96e09-103">Egy, az Azure-tároló tárolójának tárolt hozzáférési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="96e09-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="96e09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96e09-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96e09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96e09-105">DESCRIPTION</span></span>
<span data-ttu-id="96e09-106">A **set-AzStorageContainerStoredAccessPolicy** parancsmag az Azure-tárolók tárolt elérési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="96e09-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="96e09-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96e09-107">EXAMPLES</span></span>

### <span data-ttu-id="96e09-108">1. példa: tárolt hozzáférés-házirend beállítása egy tárterület-tárolóban teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="96e09-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="96e09-109">Ez a parancs a Policy06 nevű, MyContainer nevű tárterület-tároló elérési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="96e09-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="96e09-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96e09-110">PARAMETERS</span></span>

### <span data-ttu-id="96e09-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96e09-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="96e09-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="96e09-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="96e09-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="96e09-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="96e09-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="96e09-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="96e09-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="96e09-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="96e09-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="96e09-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="96e09-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="96e09-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="96e09-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="96e09-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="96e09-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="96e09-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="96e09-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="96e09-120">The default value is 10.</span></span>

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

### <span data-ttu-id="96e09-121">-Container</span><span class="sxs-lookup"><span data-stu-id="96e09-121">-Container</span></span>
<span data-ttu-id="96e09-122">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96e09-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="96e09-123">-Context</span></span>
<span data-ttu-id="96e09-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96e09-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96e09-125">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96e09-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e09-126">-DefaultProfile</span></span>
<span data-ttu-id="96e09-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96e09-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96e09-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="96e09-128">-ExpiryTime</span></span>
<span data-ttu-id="96e09-129">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="96e09-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="96e09-130">-NoExpiryTime</span></span>
<span data-ttu-id="96e09-131">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="96e09-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="96e09-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="96e09-132">-NoStartTime</span></span>
<span data-ttu-id="96e09-133">A $Null kezdési időpontját állítja be.</span><span class="sxs-lookup"><span data-stu-id="96e09-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="96e09-134">– Engedély</span><span class="sxs-lookup"><span data-stu-id="96e09-134">-Permission</span></span>
<span data-ttu-id="96e09-135">A tároló elérési házirendjében található engedélyeket adja meg a tároló tároló eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="96e09-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="96e09-136">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="96e09-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-137">-Házirend</span><span class="sxs-lookup"><span data-stu-id="96e09-137">-Policy</span></span>
<span data-ttu-id="96e09-138">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96e09-138">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96e09-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="96e09-140">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="96e09-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="96e09-141">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="96e09-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="96e09-142">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="96e09-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="96e09-143">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="96e09-143">-StartTime</span></span>
<span data-ttu-id="96e09-144">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="96e09-144">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96e09-145">-Confirm</span></span>
<span data-ttu-id="96e09-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96e09-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e09-147">-WhatIf</span></span>
<span data-ttu-id="96e09-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96e09-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96e09-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96e09-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e09-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e09-150">CommonParameters</span></span>
<span data-ttu-id="96e09-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96e09-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e09-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e09-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e09-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e09-153">INPUTS</span></span>

### <span data-ttu-id="96e09-154">System. String</span><span class="sxs-lookup"><span data-stu-id="96e09-154">System.String</span></span>

### <span data-ttu-id="96e09-155">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96e09-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="96e09-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e09-156">OUTPUTS</span></span>

### <span data-ttu-id="96e09-157">System. String</span><span class="sxs-lookup"><span data-stu-id="96e09-157">System.String</span></span>

## <span data-ttu-id="96e09-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96e09-158">NOTES</span></span>

## <span data-ttu-id="96e09-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96e09-159">RELATED LINKS</span></span>

[<span data-ttu-id="96e09-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96e09-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="96e09-161">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="96e09-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="96e09-162">Új – AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96e09-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="96e09-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96e09-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
