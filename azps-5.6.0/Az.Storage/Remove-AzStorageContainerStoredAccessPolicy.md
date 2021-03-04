---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 4d2828351c4007e57fd8c7534e88aa3be5543199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938442"
---
# <span data-ttu-id="20b81-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20b81-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="20b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20b81-102">SYNOPSIS</span></span>
<span data-ttu-id="20b81-103">Eltávolít egy tárolt hozzáférési házirendet egy Azure-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="20b81-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="20b81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20b81-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20b81-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20b81-105">DESCRIPTION</span></span>
<span data-ttu-id="20b81-106">A **Remove-AzStorageContainerStoredAccessPolicy** parancsmag eltávolít egy tárolt hozzáférési házirendet egy Azure-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="20b81-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="20b81-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20b81-107">EXAMPLES</span></span>

### <span data-ttu-id="20b81-108">1. példa: Tárolt hozzáférési házirend eltávolítása egy tárolóból</span><span class="sxs-lookup"><span data-stu-id="20b81-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="20b81-109">Ez a parancs eltávolítja a Policy03 nevű hozzáférési házirendet a MyContainer nevű tárolt tárolóból.</span><span class="sxs-lookup"><span data-stu-id="20b81-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="20b81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20b81-110">PARAMETERS</span></span>

### <span data-ttu-id="20b81-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="20b81-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="20b81-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="20b81-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="20b81-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="20b81-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="20b81-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="20b81-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="20b81-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="20b81-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="20b81-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="20b81-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="20b81-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="20b81-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="20b81-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="20b81-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="20b81-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="20b81-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="20b81-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="20b81-120">The default value is 10.</span></span>

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

### <span data-ttu-id="20b81-121">-Container</span><span class="sxs-lookup"><span data-stu-id="20b81-121">-Container</span></span>
<span data-ttu-id="20b81-122">Az Azure-tároló tárolónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20b81-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="20b81-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="20b81-123">-Context</span></span>
<span data-ttu-id="20b81-124">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20b81-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="20b81-125">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="20b81-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="20b81-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b81-126">-DefaultProfile</span></span>
<span data-ttu-id="20b81-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20b81-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b81-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20b81-128">-PassThru</span></span>
<span data-ttu-id="20b81-129">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="20b81-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="20b81-130">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="20b81-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="20b81-131">-Házirend</span><span class="sxs-lookup"><span data-stu-id="20b81-131">-Policy</span></span>
<span data-ttu-id="20b81-132">A parancsmag által eltávolított tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20b81-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="20b81-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="20b81-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="20b81-134">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="20b81-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="20b81-135">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="20b81-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="20b81-136">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="20b81-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="20b81-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20b81-137">-Confirm</span></span>
<span data-ttu-id="20b81-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="20b81-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b81-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b81-139">-WhatIf</span></span>
<span data-ttu-id="20b81-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="20b81-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b81-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20b81-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b81-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b81-142">CommonParameters</span></span>
<span data-ttu-id="20b81-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b81-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b81-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b81-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b81-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20b81-145">INPUTS</span></span>

### <span data-ttu-id="20b81-146">System.String</span><span class="sxs-lookup"><span data-stu-id="20b81-146">System.String</span></span>

### <span data-ttu-id="20b81-147">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="20b81-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="20b81-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20b81-148">OUTPUTS</span></span>

### <span data-ttu-id="20b81-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20b81-149">System.Boolean</span></span>

## <span data-ttu-id="20b81-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20b81-150">NOTES</span></span>

## <span data-ttu-id="20b81-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20b81-151">RELATED LINKS</span></span>

[<span data-ttu-id="20b81-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20b81-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="20b81-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20b81-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="20b81-154">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="20b81-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="20b81-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20b81-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
