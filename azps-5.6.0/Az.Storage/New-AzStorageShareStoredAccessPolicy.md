---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 3604d6e8d3c9394a53c59e220bdef31662a75f88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002341"
---
# <span data-ttu-id="b5989-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b5989-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="b5989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5989-102">SYNOPSIS</span></span>
<span data-ttu-id="b5989-103">Tárterület-megosztáson tárolt hozzáférési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5989-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="b5989-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5989-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b5989-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5989-105">DESCRIPTION</span></span>
<span data-ttu-id="b5989-106">A **New-AzStorageShareStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet hoz létre egy Azure Storage-megosztáson.</span><span class="sxs-lookup"><span data-stu-id="b5989-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="b5989-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5989-107">EXAMPLES</span></span>

### <span data-ttu-id="b5989-108">1. példa: Tárolt hozzáférési házirend létrehozása egy megosztásban</span><span class="sxs-lookup"><span data-stu-id="b5989-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="b5989-109">Ez a parancs egy olyan tárolt hozzáférési házirendet hoz létre, amely teljes engedéllyel rendelkezik egy megosztásban.</span><span class="sxs-lookup"><span data-stu-id="b5989-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="b5989-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5989-110">PARAMETERS</span></span>

### <span data-ttu-id="b5989-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5989-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b5989-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b5989-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b5989-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="b5989-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b5989-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b5989-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b5989-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b5989-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b5989-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="b5989-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b5989-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="b5989-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b5989-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="b5989-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b5989-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b5989-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b5989-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b5989-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b5989-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b5989-121">-Context</span></span>
<span data-ttu-id="b5989-122">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5989-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b5989-123">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="b5989-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b5989-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5989-124">-DefaultProfile</span></span>
<span data-ttu-id="b5989-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5989-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5989-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b5989-126">-ExpiryTime</span></span>
<span data-ttu-id="b5989-127">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="b5989-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="b5989-128">-Engedély</span><span class="sxs-lookup"><span data-stu-id="b5989-128">-Permission</span></span>
<span data-ttu-id="b5989-129">Engedélyeket ad meg a tárolt hozzáférési házirendben a tárterület-megosztáshoz vagy az alatta lévő fájlokhoz való hozzáféréshez.</span><span class="sxs-lookup"><span data-stu-id="b5989-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="b5989-130">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="b5989-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b5989-131">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b5989-131">-Policy</span></span>
<span data-ttu-id="b5989-132">Megadja a tárolt hozzáférési házirend nevét.</span><span class="sxs-lookup"><span data-stu-id="b5989-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="b5989-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5989-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b5989-134">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5989-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b5989-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b5989-135">-ShareName</span></span>
<span data-ttu-id="b5989-136">A tárterület-megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5989-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="b5989-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b5989-137">-StartTime</span></span>
<span data-ttu-id="b5989-138">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="b5989-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="b5989-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5989-139">CommonParameters</span></span>
<span data-ttu-id="b5989-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5989-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5989-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5989-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5989-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5989-142">INPUTS</span></span>

### <span data-ttu-id="b5989-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b5989-143">System.String</span></span>

### <span data-ttu-id="b5989-144">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5989-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b5989-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5989-145">OUTPUTS</span></span>

### <span data-ttu-id="b5989-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b5989-146">System.String</span></span>

## <span data-ttu-id="b5989-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5989-147">NOTES</span></span>

## <span data-ttu-id="b5989-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5989-148">RELATED LINKS</span></span>

[<span data-ttu-id="b5989-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b5989-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b5989-150">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="b5989-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b5989-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b5989-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b5989-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b5989-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
