---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 5159e09d4e56b45e9b7ce61bae3e9d8e5fd115c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150386"
---
# <span data-ttu-id="eef09-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eef09-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="eef09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef09-102">SYNOPSIS</span></span>
<span data-ttu-id="eef09-103">Tárterület-megosztáson tárolt hozzáférési házirend frissítése.</span><span class="sxs-lookup"><span data-stu-id="eef09-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="eef09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eef09-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eef09-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eef09-105">DESCRIPTION</span></span>
<span data-ttu-id="eef09-106">A **Set-AzStorageShareStoredAccessPolicy** parancsmag frissítései egy Azure Storage-megosztáson tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="eef09-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="eef09-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eef09-107">EXAMPLES</span></span>

### <span data-ttu-id="eef09-108">1. példa: Tárolt hozzáférési házirend frissítése a Tárterület megosztása szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="eef09-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="eef09-109">Ez a parancs frissíti a tárolt hozzáférési házirendet, amely teljes engedéllyel rendelkezik egy megosztásban.</span><span class="sxs-lookup"><span data-stu-id="eef09-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="eef09-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eef09-110">PARAMETERS</span></span>

### <span data-ttu-id="eef09-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eef09-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eef09-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="eef09-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eef09-113">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="eef09-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eef09-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="eef09-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eef09-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eef09-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eef09-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="eef09-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eef09-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="eef09-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eef09-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="eef09-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eef09-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="eef09-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eef09-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="eef09-120">The default value is 10.</span></span>

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

### <span data-ttu-id="eef09-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="eef09-121">-Context</span></span>
<span data-ttu-id="eef09-122">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eef09-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eef09-123">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="eef09-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="eef09-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef09-124">-DefaultProfile</span></span>
<span data-ttu-id="eef09-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eef09-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef09-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="eef09-126">-ExpiryTime</span></span>
<span data-ttu-id="eef09-127">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="eef09-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="eef09-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="eef09-128">-NoExpiryTime</span></span>
<span data-ttu-id="eef09-129">Azt jelzi, hogy ez a parancsmag törli a **ExpiryTime** tulajdonságot a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="eef09-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="eef09-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="eef09-130">-NoStartTime</span></span>
<span data-ttu-id="eef09-131">Azt jelzi, hogy ez a parancsmag törli a **StartTime** tulajdonságot a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="eef09-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="eef09-132">-Permission</span><span class="sxs-lookup"><span data-stu-id="eef09-132">-Permission</span></span>
<span data-ttu-id="eef09-133">A tárolt hozzáférési házirendben megadja az alatta lévő megosztás vagy fájlok eléréséhez szükséges engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="eef09-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="eef09-134">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="eef09-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="eef09-135">-Házirend</span><span class="sxs-lookup"><span data-stu-id="eef09-135">-Policy</span></span>
<span data-ttu-id="eef09-136">Megadja a tárolt hozzáférési házirend nevét.</span><span class="sxs-lookup"><span data-stu-id="eef09-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="eef09-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eef09-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eef09-138">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eef09-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="eef09-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="eef09-139">-ShareName</span></span>
<span data-ttu-id="eef09-140">A tárterület-megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eef09-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="eef09-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eef09-141">-StartTime</span></span>
<span data-ttu-id="eef09-142">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="eef09-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="eef09-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eef09-143">-Confirm</span></span>
<span data-ttu-id="eef09-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eef09-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eef09-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef09-145">-WhatIf</span></span>
<span data-ttu-id="eef09-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eef09-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eef09-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eef09-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eef09-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef09-148">CommonParameters</span></span>
<span data-ttu-id="eef09-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef09-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef09-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef09-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef09-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eef09-151">INPUTS</span></span>

### <span data-ttu-id="eef09-152">System.String</span><span class="sxs-lookup"><span data-stu-id="eef09-152">System.String</span></span>

### <span data-ttu-id="eef09-153">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eef09-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eef09-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eef09-154">OUTPUTS</span></span>

### <span data-ttu-id="eef09-155">System.String</span><span class="sxs-lookup"><span data-stu-id="eef09-155">System.String</span></span>

## <span data-ttu-id="eef09-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eef09-156">NOTES</span></span>

## <span data-ttu-id="eef09-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eef09-157">RELATED LINKS</span></span>

[<span data-ttu-id="eef09-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eef09-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="eef09-159">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="eef09-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="eef09-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eef09-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="eef09-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eef09-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
