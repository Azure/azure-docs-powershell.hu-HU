---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348533"
---
# <span data-ttu-id="66321-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="66321-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="66321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66321-102">SYNOPSIS</span></span>
<span data-ttu-id="66321-103">A megadott tároló eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="66321-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="66321-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66321-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66321-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66321-105">DESCRIPTION</span></span>
<span data-ttu-id="66321-106">A **Remove-AzStorageContainer** parancsmag eltávolítja a megadott tárolót az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="66321-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="66321-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66321-107">EXAMPLES</span></span>

### <span data-ttu-id="66321-108">1. példa: Tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="66321-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="66321-109">Ez a példa eltávolít egy MyTestContainer nevű tárolót.</span><span class="sxs-lookup"><span data-stu-id="66321-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="66321-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66321-110">PARAMETERS</span></span>

### <span data-ttu-id="66321-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="66321-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="66321-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="66321-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="66321-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="66321-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="66321-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="66321-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="66321-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="66321-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="66321-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="66321-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="66321-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="66321-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="66321-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="66321-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="66321-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="66321-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="66321-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="66321-120">The default value is 10.</span></span>

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

### <span data-ttu-id="66321-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="66321-121">-Context</span></span>
<span data-ttu-id="66321-122">Megadja az eltávolítani kívánt tároló környezetét.</span><span class="sxs-lookup"><span data-stu-id="66321-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="66321-123">A New-AzStorageContext létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="66321-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="66321-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66321-124">-DefaultProfile</span></span>
<span data-ttu-id="66321-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66321-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66321-126">-Force</span><span class="sxs-lookup"><span data-stu-id="66321-126">-Force</span></span>
<span data-ttu-id="66321-127">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="66321-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66321-128">-Name</span><span class="sxs-lookup"><span data-stu-id="66321-128">-Name</span></span>
<span data-ttu-id="66321-129">Az eltávolítható tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66321-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="66321-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66321-130">-PassThru</span></span>
<span data-ttu-id="66321-131">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="66321-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="66321-132">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="66321-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="66321-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="66321-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="66321-134">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="66321-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="66321-135">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="66321-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="66321-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66321-136">-Confirm</span></span>
<span data-ttu-id="66321-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="66321-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66321-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66321-138">-WhatIf</span></span>
<span data-ttu-id="66321-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="66321-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66321-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66321-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66321-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66321-141">CommonParameters</span></span>
<span data-ttu-id="66321-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66321-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66321-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66321-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66321-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66321-144">INPUTS</span></span>

### <span data-ttu-id="66321-145">System.String</span><span class="sxs-lookup"><span data-stu-id="66321-145">System.String</span></span>

### <span data-ttu-id="66321-146">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="66321-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="66321-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66321-147">OUTPUTS</span></span>

### <span data-ttu-id="66321-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66321-148">System.Boolean</span></span>

## <span data-ttu-id="66321-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66321-149">NOTES</span></span>

## <span data-ttu-id="66321-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66321-150">RELATED LINKS</span></span>

[<span data-ttu-id="66321-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="66321-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="66321-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="66321-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
