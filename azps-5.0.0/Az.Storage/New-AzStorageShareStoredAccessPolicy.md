---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195055"
---
# <span data-ttu-id="d1fa2-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1fa2-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="d1fa2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fa2-103">Tárolt hozzáférési házirendet hoz létre egy tárterület-megosztásban.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="d1fa2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1fa2-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d1fa2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="d1fa2-106">A **New-AzStorageShareStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárhelyen.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="d1fa2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="d1fa2-108">Példa 1: tárolt hozzáférés-házirend létrehozása egy megosztásban</span><span class="sxs-lookup"><span data-stu-id="d1fa2-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="d1fa2-109">Ez a parancs egy olyan tárolt hozzáférési házirendet hoz létre, amely teljes hozzáféréssel rendelkezik a megosztásban.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="d1fa2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1fa2-110">PARAMETERS</span></span>

### <span data-ttu-id="d1fa2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1fa2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d1fa2-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d1fa2-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d1fa2-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d1fa2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d1fa2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d1fa2-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d1fa2-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d1fa2-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d1fa2-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="d1fa2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d1fa2-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d1fa2-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d1fa2-121">-Context</span></span>
<span data-ttu-id="d1fa2-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d1fa2-123">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d1fa2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fa2-124">-DefaultProfile</span></span>
<span data-ttu-id="d1fa2-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1fa2-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d1fa2-126">-ExpiryTime</span></span>
<span data-ttu-id="d1fa2-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="d1fa2-128">– Engedély</span><span class="sxs-lookup"><span data-stu-id="d1fa2-128">-Permission</span></span>
<span data-ttu-id="d1fa2-129">A tárolt elérési házirend engedélyeinek megadása a tárterület-megosztás vagy-fájlok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="d1fa2-130">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="d1fa2-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d1fa2-131">-Házirend</span><span class="sxs-lookup"><span data-stu-id="d1fa2-131">-Policy</span></span>
<span data-ttu-id="d1fa2-132">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="d1fa2-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1fa2-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d1fa2-134">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d1fa2-135">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="d1fa2-135">-ShareName</span></span>
<span data-ttu-id="d1fa2-136">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="d1fa2-137">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="d1fa2-137">-StartTime</span></span>
<span data-ttu-id="d1fa2-138">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="d1fa2-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d1fa2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fa2-139">CommonParameters</span></span>
<span data-ttu-id="d1fa2-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1fa2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fa2-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fa2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fa2-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1fa2-142">INPUTS</span></span>

### <span data-ttu-id="d1fa2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d1fa2-143">System.String</span></span>

### <span data-ttu-id="d1fa2-144">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1fa2-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1fa2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1fa2-145">OUTPUTS</span></span>

### <span data-ttu-id="d1fa2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d1fa2-146">System.String</span></span>

## <span data-ttu-id="d1fa2-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1fa2-147">NOTES</span></span>

## <span data-ttu-id="d1fa2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1fa2-148">RELATED LINKS</span></span>

[<span data-ttu-id="d1fa2-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1fa2-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d1fa2-150">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1fa2-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d1fa2-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1fa2-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d1fa2-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1fa2-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)