---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 5159e09d4e56b45e9b7ce61bae3e9d8e5fd115c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185757"
---
# <span data-ttu-id="ca1fa-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca1fa-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="ca1fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca1fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1fa-103">A tárolt hozzáférési házirendet frissíti egy tárterület-megosztáson.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="ca1fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca1fa-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca1fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca1fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ca1fa-106">A **set-AzStorageShareStoredAccessPolicy** parancsmag egy Azure tárhely-megosztáson frissíti a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="ca1fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca1fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ca1fa-108">Példa 1: tárolt hozzáférés-házirend frissítése a tárterület-megosztásban</span><span class="sxs-lookup"><span data-stu-id="ca1fa-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="ca1fa-109">Ez a parancs olyan tárolt hozzáférés-házirendet frissít, amely teljes hozzáféréssel rendelkezik egy megosztásban.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="ca1fa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca1fa-110">PARAMETERS</span></span>

### <span data-ttu-id="ca1fa-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca1fa-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ca1fa-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ca1fa-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ca1fa-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ca1fa-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ca1fa-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ca1fa-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ca1fa-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ca1fa-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ca1fa-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="ca1fa-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ca1fa-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ca1fa-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ca1fa-121">-Context</span></span>
<span data-ttu-id="ca1fa-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ca1fa-123">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ca1fa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1fa-124">-DefaultProfile</span></span>
<span data-ttu-id="ca1fa-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca1fa-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca1fa-126">-ExpiryTime</span></span>
<span data-ttu-id="ca1fa-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ca1fa-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca1fa-128">-NoExpiryTime</span></span>
<span data-ttu-id="ca1fa-129">Jelzi, hogy ez a parancsmag törli a **ExpiryTime** tulajdonságot a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="ca1fa-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="ca1fa-130">-NoStartTime</span></span>
<span data-ttu-id="ca1fa-131">Azt jelzi, hogy ez a parancsmag törli az **időpont** tulajdonságot a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="ca1fa-132">– Engedély</span><span class="sxs-lookup"><span data-stu-id="ca1fa-132">-Permission</span></span>
<span data-ttu-id="ca1fa-133">A tárolt elérési házirend engedélyeinek megadása az alatta lévő megosztás vagy fájlok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="ca1fa-134">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="ca1fa-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ca1fa-135">-Házirend</span><span class="sxs-lookup"><span data-stu-id="ca1fa-135">-Policy</span></span>
<span data-ttu-id="ca1fa-136">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="ca1fa-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca1fa-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ca1fa-138">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ca1fa-139">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="ca1fa-139">-ShareName</span></span>
<span data-ttu-id="ca1fa-140">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="ca1fa-141">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="ca1fa-141">-StartTime</span></span>
<span data-ttu-id="ca1fa-142">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ca1fa-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca1fa-143">-Confirm</span></span>
<span data-ttu-id="ca1fa-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca1fa-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1fa-145">-WhatIf</span></span>
<span data-ttu-id="ca1fa-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca1fa-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca1fa-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca1fa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1fa-148">CommonParameters</span></span>
<span data-ttu-id="ca1fa-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca1fa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1fa-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca1fa-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1fa-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca1fa-151">INPUTS</span></span>

### <span data-ttu-id="ca1fa-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ca1fa-152">System.String</span></span>

### <span data-ttu-id="ca1fa-153">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca1fa-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca1fa-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca1fa-154">OUTPUTS</span></span>

### <span data-ttu-id="ca1fa-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ca1fa-155">System.String</span></span>

## <span data-ttu-id="ca1fa-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca1fa-156">NOTES</span></span>

## <span data-ttu-id="ca1fa-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca1fa-157">RELATED LINKS</span></span>

[<span data-ttu-id="ca1fa-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca1fa-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ca1fa-159">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca1fa-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ca1fa-160">Új – AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca1fa-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ca1fa-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca1fa-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)