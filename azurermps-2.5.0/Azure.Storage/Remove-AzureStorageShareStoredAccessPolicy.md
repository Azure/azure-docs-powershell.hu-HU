---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6a00bbe0a80218dfdd29666fffaf6ec314c41f01
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850490"
---
# <span data-ttu-id="347c6-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="347c6-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="347c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="347c6-102">SYNOPSIS</span></span>
<span data-ttu-id="347c6-103">Egy tárolt Access-házirend eltávolítása a tárterület-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="347c6-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="347c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="347c6-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="347c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="347c6-105">DESCRIPTION</span></span>
<span data-ttu-id="347c6-106">A **Remove-AzureStorageShareStoredAccessPolicy** parancsmag az Azure tárhely-megosztásból eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="347c6-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="347c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="347c6-107">EXAMPLES</span></span>

### <span data-ttu-id="347c6-108">1. példa: a tárolt hozzáférés-házirend eltávolítása Azure-tárhelyről</span><span class="sxs-lookup"><span data-stu-id="347c6-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="347c6-109">Ez a parancs eltávolítja a GeneralPolicy nevű, a ContosoShare nevű, tárolt elérési házirendet.</span><span class="sxs-lookup"><span data-stu-id="347c6-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="347c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="347c6-110">PARAMETERS</span></span>

### <span data-ttu-id="347c6-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="347c6-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="347c6-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="347c6-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="347c6-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="347c6-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="347c6-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="347c6-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="347c6-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="347c6-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="347c6-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="347c6-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="347c6-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="347c6-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="347c6-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="347c6-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="347c6-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="347c6-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="347c6-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="347c6-120">The default value is 10.</span></span>

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

### <span data-ttu-id="347c6-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="347c6-121">-Context</span></span>
<span data-ttu-id="347c6-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="347c6-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="347c6-123">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="347c6-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="347c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="347c6-124">-DefaultProfile</span></span>
<span data-ttu-id="347c6-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="347c6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="347c6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="347c6-126">-PassThru</span></span>
<span data-ttu-id="347c6-127">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="347c6-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="347c6-128">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="347c6-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="347c6-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="347c6-129">-Policy</span></span>
<span data-ttu-id="347c6-130">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="347c6-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="347c6-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="347c6-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="347c6-132">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="347c6-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="347c6-133">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="347c6-133">-ShareName</span></span>
<span data-ttu-id="347c6-134">Annak a tárolási megosztásnak a neve, amelyhez ez a parancsmag eltávolítja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="347c6-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="347c6-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="347c6-135">-Confirm</span></span>
<span data-ttu-id="347c6-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="347c6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="347c6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="347c6-137">-WhatIf</span></span>
<span data-ttu-id="347c6-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="347c6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="347c6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="347c6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="347c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="347c6-140">CommonParameters</span></span>
<span data-ttu-id="347c6-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="347c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="347c6-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="347c6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="347c6-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="347c6-143">INPUTS</span></span>

### <span data-ttu-id="347c6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="347c6-144">System.String</span></span>

### <span data-ttu-id="347c6-145">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="347c6-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="347c6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="347c6-146">OUTPUTS</span></span>

### <span data-ttu-id="347c6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="347c6-147">System.Boolean</span></span>

## <span data-ttu-id="347c6-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="347c6-148">NOTES</span></span>

## <span data-ttu-id="347c6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="347c6-149">RELATED LINKS</span></span>

[<span data-ttu-id="347c6-150">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="347c6-150">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="347c6-151">Új – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="347c6-151">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="347c6-152">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="347c6-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="347c6-153">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="347c6-153">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
