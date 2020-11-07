---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 08b3ec17476e959aa7190cfb914468eb8ab73775
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672663"
---
# <span data-ttu-id="dae7d-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dae7d-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="dae7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dae7d-102">SYNOPSIS</span></span>
<span data-ttu-id="dae7d-103">Egy tárolt hozzáférés-házirend eltávolítása az Azure Storage tárolóból.</span><span class="sxs-lookup"><span data-stu-id="dae7d-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dae7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dae7d-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dae7d-105">DESCRIPTION</span></span>
<span data-ttu-id="dae7d-106">A **Remove-AzureStorageContainerStoredAccessPolicy** parancsmag az Azure Storage tárolóból távolítja el a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="dae7d-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="dae7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dae7d-107">EXAMPLES</span></span>

### <span data-ttu-id="dae7d-108">1. példa: tárolt hozzáférési házirend eltávolítása tároló tárolóból</span><span class="sxs-lookup"><span data-stu-id="dae7d-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="dae7d-109">Ez a parancs eltávolítja a Policy03 nevű Access-házirendet a MyContainer nevű tároló tárolóból.</span><span class="sxs-lookup"><span data-stu-id="dae7d-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="dae7d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dae7d-110">PARAMETERS</span></span>

### <span data-ttu-id="dae7d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dae7d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dae7d-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="dae7d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dae7d-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="dae7d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dae7d-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="dae7d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dae7d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dae7d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dae7d-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="dae7d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dae7d-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="dae7d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dae7d-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="dae7d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dae7d-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="dae7d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dae7d-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="dae7d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="dae7d-121">-Container</span><span class="sxs-lookup"><span data-stu-id="dae7d-121">-Container</span></span>
<span data-ttu-id="dae7d-122">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dae7d-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="dae7d-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dae7d-123">-Context</span></span>
<span data-ttu-id="dae7d-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dae7d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dae7d-125">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dae7d-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dae7d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dae7d-126">-PassThru</span></span>
<span data-ttu-id="dae7d-127">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="dae7d-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="dae7d-128">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="dae7d-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="dae7d-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="dae7d-129">-Policy</span></span>
<span data-ttu-id="dae7d-130">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="dae7d-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dae7d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dae7d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dae7d-132">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="dae7d-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dae7d-133">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="dae7d-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dae7d-134">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="dae7d-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dae7d-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dae7d-135">-Confirm</span></span>
<span data-ttu-id="dae7d-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dae7d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae7d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae7d-137">-WhatIf</span></span>
<span data-ttu-id="dae7d-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dae7d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dae7d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dae7d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae7d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae7d-140">CommonParameters</span></span>
<span data-ttu-id="dae7d-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dae7d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae7d-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae7d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae7d-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dae7d-143">INPUTS</span></span>

### <span data-ttu-id="dae7d-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dae7d-144">IStorageContext</span></span>

<span data-ttu-id="dae7d-145">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dae7d-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="dae7d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dae7d-146">OUTPUTS</span></span>

### <span data-ttu-id="dae7d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dae7d-147">System.Boolean</span></span>

## <span data-ttu-id="dae7d-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dae7d-148">NOTES</span></span>

## <span data-ttu-id="dae7d-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dae7d-149">RELATED LINKS</span></span>

[<span data-ttu-id="dae7d-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dae7d-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="dae7d-151">Új – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dae7d-151">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="dae7d-152">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dae7d-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dae7d-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dae7d-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
