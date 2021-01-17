---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466883"
---
# <span data-ttu-id="8b3d0-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b3d0-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="8b3d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b3d0-103">Tárolt hozzáférési házirendet állít be egy Azure-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="8b3d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8b3d0-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b3d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8b3d0-105">DESCRIPTION</span></span>
<span data-ttu-id="8b3d0-106">A **Set-AzStorageContainerStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet állít be egy Azure-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="8b3d0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8b3d0-107">EXAMPLES</span></span>

### <span data-ttu-id="8b3d0-108">1. példa: Tárolt hozzáférési házirend beállítása teljes engedéllyel rendelkező tárolóban</span><span class="sxs-lookup"><span data-stu-id="8b3d0-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="8b3d0-109">Ez a parancs egy Policy06 nevű hozzáférési házirendet állít be a MyContainer nevű tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="8b3d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b3d0-110">PARAMETERS</span></span>

### <span data-ttu-id="8b3d0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b3d0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8b3d0-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8b3d0-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8b3d0-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b3d0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8b3d0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8b3d0-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8b3d0-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8b3d0-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8b3d0-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8b3d0-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8b3d0-121">-Container</span><span class="sxs-lookup"><span data-stu-id="8b3d0-121">-Container</span></span>
<span data-ttu-id="8b3d0-122">Az Azure-tároló tárolónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="8b3d0-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8b3d0-123">-Context</span></span>
<span data-ttu-id="8b3d0-124">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8b3d0-125">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8b3d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b3d0-126">-DefaultProfile</span></span>
<span data-ttu-id="8b3d0-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b3d0-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8b3d0-128">-ExpiryTime</span></span>
<span data-ttu-id="8b3d0-129">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="8b3d0-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8b3d0-130">-NoExpiryTime</span></span>
<span data-ttu-id="8b3d0-131">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="8b3d0-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="8b3d0-132">-NoStartTime</span></span>
<span data-ttu-id="8b3d0-133">Beállítja a kezdési $Null.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="8b3d0-134">-Engedély</span><span class="sxs-lookup"><span data-stu-id="8b3d0-134">-Permission</span></span>
<span data-ttu-id="8b3d0-135">Engedélyeket ad meg a tárolt hozzáférési házirendben a tároló tárolóhoz való hozzáféréshez.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="8b3d0-136">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="8b3d0-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8b3d0-137">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8b3d0-137">-Policy</span></span>
<span data-ttu-id="8b3d0-138">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="8b3d0-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b3d0-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8b3d0-140">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8b3d0-141">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8b3d0-142">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b3d0-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8b3d0-143">-StartTime</span></span>
<span data-ttu-id="8b3d0-144">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8b3d0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b3d0-145">-Confirm</span></span>
<span data-ttu-id="8b3d0-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b3d0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b3d0-147">-WhatIf</span></span>
<span data-ttu-id="8b3d0-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b3d0-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b3d0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b3d0-150">CommonParameters</span></span>
<span data-ttu-id="8b3d0-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b3d0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b3d0-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b3d0-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b3d0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b3d0-153">INPUTS</span></span>

### <span data-ttu-id="8b3d0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8b3d0-154">System.String</span></span>

### <span data-ttu-id="8b3d0-155">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b3d0-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8b3d0-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b3d0-156">OUTPUTS</span></span>

### <span data-ttu-id="8b3d0-157">System.String</span><span class="sxs-lookup"><span data-stu-id="8b3d0-157">System.String</span></span>

## <span data-ttu-id="8b3d0-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8b3d0-158">NOTES</span></span>

## <span data-ttu-id="8b3d0-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b3d0-159">RELATED LINKS</span></span>

[<span data-ttu-id="8b3d0-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b3d0-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8b3d0-161">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="8b3d0-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8b3d0-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b3d0-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8b3d0-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b3d0-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
