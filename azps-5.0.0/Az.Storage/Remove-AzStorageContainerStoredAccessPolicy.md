---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186331"
---
# <span data-ttu-id="13ce2-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13ce2-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="13ce2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="13ce2-103">Egy tárolt hozzáférés-házirend eltávolítása az Azure Storage tárolóból.</span><span class="sxs-lookup"><span data-stu-id="13ce2-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="13ce2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13ce2-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13ce2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="13ce2-106">A **Remove-AzStorageContainerStoredAccessPolicy** parancsmag az Azure Storage tárolóból távolítja el a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="13ce2-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="13ce2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13ce2-107">EXAMPLES</span></span>

### <span data-ttu-id="13ce2-108">1. példa: tárolt hozzáférési házirend eltávolítása tároló tárolóból</span><span class="sxs-lookup"><span data-stu-id="13ce2-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="13ce2-109">Ez a parancs eltávolítja a Policy03 nevű Access-házirendet a MyContainer nevű tároló tárolóból.</span><span class="sxs-lookup"><span data-stu-id="13ce2-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="13ce2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13ce2-110">PARAMETERS</span></span>

### <span data-ttu-id="13ce2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="13ce2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="13ce2-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="13ce2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="13ce2-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="13ce2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="13ce2-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="13ce2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="13ce2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="13ce2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="13ce2-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ce2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="13ce2-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="13ce2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="13ce2-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="13ce2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="13ce2-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="13ce2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="13ce2-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="13ce2-120">The default value is 10.</span></span>

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

### <span data-ttu-id="13ce2-121">-Container</span><span class="sxs-lookup"><span data-stu-id="13ce2-121">-Container</span></span>
<span data-ttu-id="13ce2-122">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ce2-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ce2-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="13ce2-123">-Context</span></span>
<span data-ttu-id="13ce2-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ce2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="13ce2-125">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="13ce2-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="13ce2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ce2-126">-DefaultProfile</span></span>
<span data-ttu-id="13ce2-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13ce2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ce2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13ce2-128">-PassThru</span></span>
<span data-ttu-id="13ce2-129">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="13ce2-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="13ce2-130">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="13ce2-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="13ce2-131">-Házirend</span><span class="sxs-lookup"><span data-stu-id="13ce2-131">-Policy</span></span>
<span data-ttu-id="13ce2-132">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="13ce2-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ce2-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="13ce2-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="13ce2-134">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="13ce2-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="13ce2-135">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="13ce2-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="13ce2-136">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="13ce2-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="13ce2-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13ce2-137">-Confirm</span></span>
<span data-ttu-id="13ce2-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13ce2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ce2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ce2-139">-WhatIf</span></span>
<span data-ttu-id="13ce2-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13ce2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13ce2-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13ce2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ce2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ce2-142">CommonParameters</span></span>
<span data-ttu-id="13ce2-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13ce2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ce2-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ce2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ce2-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ce2-145">INPUTS</span></span>

### <span data-ttu-id="13ce2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="13ce2-146">System.String</span></span>

### <span data-ttu-id="13ce2-147">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="13ce2-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="13ce2-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ce2-148">OUTPUTS</span></span>

### <span data-ttu-id="13ce2-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13ce2-149">System.Boolean</span></span>

## <span data-ttu-id="13ce2-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13ce2-150">NOTES</span></span>

## <span data-ttu-id="13ce2-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13ce2-151">RELATED LINKS</span></span>

[<span data-ttu-id="13ce2-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13ce2-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="13ce2-153">Új – AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13ce2-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="13ce2-154">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="13ce2-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="13ce2-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13ce2-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
