---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: d8c9e0e49ba7a5caa9cb93290ef5e96b60fd4430
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466901"
---
# <span data-ttu-id="314f6-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="314f6-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="314f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="314f6-102">SYNOPSIS</span></span>
<span data-ttu-id="314f6-103">Egy tárolt hozzáférési házirend eltávolítása egy tárterület-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="314f6-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="314f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="314f6-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="314f6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="314f6-105">DESCRIPTION</span></span>
<span data-ttu-id="314f6-106">A **Remove-AzStorageShareStoredAccessPolicy** parancsmag eltávolít egy tárolt hozzáférési házirendet egy Azure Storage-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="314f6-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="314f6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="314f6-107">EXAMPLES</span></span>

### <span data-ttu-id="314f6-108">1. példa: Tárolt hozzáférési házirend eltávolítása Azure Storage-megosztásból</span><span class="sxs-lookup"><span data-stu-id="314f6-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="314f6-109">Ez a parancs eltávolítja a GeneralPolicy nevű tárolt hozzáférési házirendet a ContosoShare szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="314f6-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="314f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="314f6-110">PARAMETERS</span></span>

### <span data-ttu-id="314f6-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="314f6-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="314f6-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="314f6-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="314f6-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="314f6-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="314f6-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="314f6-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="314f6-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="314f6-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="314f6-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="314f6-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="314f6-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="314f6-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="314f6-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="314f6-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="314f6-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="314f6-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="314f6-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="314f6-120">The default value is 10.</span></span>

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

### <span data-ttu-id="314f6-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="314f6-121">-Context</span></span>
<span data-ttu-id="314f6-122">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="314f6-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="314f6-123">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="314f6-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="314f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314f6-124">-DefaultProfile</span></span>
<span data-ttu-id="314f6-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="314f6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="314f6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="314f6-126">-PassThru</span></span>
<span data-ttu-id="314f6-127">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="314f6-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="314f6-128">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="314f6-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="314f6-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="314f6-129">-Policy</span></span>
<span data-ttu-id="314f6-130">A parancsmag által eltávolított tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="314f6-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="314f6-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="314f6-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="314f6-132">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="314f6-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="314f6-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="314f6-133">-ShareName</span></span>
<span data-ttu-id="314f6-134">Azt a tárterület-megosztásnevet adja meg, amelynek a parancsmagja eltávolít egy házirendet.</span><span class="sxs-lookup"><span data-stu-id="314f6-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="314f6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="314f6-135">-Confirm</span></span>
<span data-ttu-id="314f6-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="314f6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="314f6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="314f6-137">-WhatIf</span></span>
<span data-ttu-id="314f6-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="314f6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="314f6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="314f6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="314f6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314f6-140">CommonParameters</span></span>
<span data-ttu-id="314f6-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314f6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314f6-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314f6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314f6-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="314f6-143">INPUTS</span></span>

### <span data-ttu-id="314f6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="314f6-144">System.String</span></span>

### <span data-ttu-id="314f6-145">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="314f6-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="314f6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="314f6-146">OUTPUTS</span></span>

### <span data-ttu-id="314f6-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="314f6-147">System.Boolean</span></span>

## <span data-ttu-id="314f6-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="314f6-148">NOTES</span></span>

## <span data-ttu-id="314f6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="314f6-149">RELATED LINKS</span></span>

[<span data-ttu-id="314f6-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="314f6-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="314f6-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="314f6-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="314f6-152">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="314f6-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="314f6-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="314f6-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
