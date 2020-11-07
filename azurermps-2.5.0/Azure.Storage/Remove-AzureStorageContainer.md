---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 24eba8b6aeedb2f240fbd7da16b1b7a76ee9d759
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850494"
---
# <span data-ttu-id="95745-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95745-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="95745-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95745-102">SYNOPSIS</span></span>
<span data-ttu-id="95745-103">Eltávolítja a megadott tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="95745-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95745-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95745-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95745-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95745-105">DESCRIPTION</span></span>
<span data-ttu-id="95745-106">A **Remove-AzureStorageContainer** parancsmag eltávolítja a megadott tárterületet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="95745-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="95745-107">Példák</span><span class="sxs-lookup"><span data-stu-id="95745-107">EXAMPLES</span></span>

### <span data-ttu-id="95745-108">1. példa: tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="95745-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="95745-109">Ez a példa eltávolítja a MyTestContainer nevű tárolót.</span><span class="sxs-lookup"><span data-stu-id="95745-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="95745-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95745-110">PARAMETERS</span></span>

### <span data-ttu-id="95745-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="95745-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="95745-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="95745-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="95745-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="95745-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="95745-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="95745-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="95745-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="95745-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="95745-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="95745-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="95745-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="95745-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="95745-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="95745-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="95745-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="95745-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="95745-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="95745-120">The default value is 10.</span></span>

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

### <span data-ttu-id="95745-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="95745-121">-Context</span></span>
<span data-ttu-id="95745-122">Az eltávolítani kívánt tároló környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95745-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="95745-123">A New-AzureStorageContext parancsmag segítségével létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="95745-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="95745-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95745-124">-DefaultProfile</span></span>
<span data-ttu-id="95745-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95745-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95745-126">-Force</span><span class="sxs-lookup"><span data-stu-id="95745-126">-Force</span></span>
<span data-ttu-id="95745-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="95745-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95745-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95745-128">-Name</span></span>
<span data-ttu-id="95745-129">Az eltávolítandó tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95745-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95745-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95745-130">-PassThru</span></span>
<span data-ttu-id="95745-131">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="95745-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="95745-132">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="95745-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="95745-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="95745-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="95745-134">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="95745-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="95745-135">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="95745-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="95745-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="95745-136">-Confirm</span></span>
<span data-ttu-id="95745-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95745-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95745-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95745-138">-WhatIf</span></span>
<span data-ttu-id="95745-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="95745-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95745-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95745-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95745-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95745-141">CommonParameters</span></span>
<span data-ttu-id="95745-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95745-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95745-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95745-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95745-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95745-144">INPUTS</span></span>

### <span data-ttu-id="95745-145">System. String</span><span class="sxs-lookup"><span data-stu-id="95745-145">System.String</span></span>

### <span data-ttu-id="95745-146">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="95745-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="95745-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95745-147">OUTPUTS</span></span>

### <span data-ttu-id="95745-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95745-148">System.Boolean</span></span>

## <span data-ttu-id="95745-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95745-149">NOTES</span></span>

## <span data-ttu-id="95745-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95745-150">RELATED LINKS</span></span>

[<span data-ttu-id="95745-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95745-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="95745-152">Új – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95745-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
