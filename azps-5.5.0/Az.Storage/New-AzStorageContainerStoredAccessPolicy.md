---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: eb51b8c4e33f45d637354f85be049295626afdd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165651"
---
# <span data-ttu-id="c778b-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c778b-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="c778b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c778b-102">SYNOPSIS</span></span>
<span data-ttu-id="c778b-103">Tárolt hozzáférési házirendet hoz létre egy Azure-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="c778b-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="c778b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c778b-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c778b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c778b-105">DESCRIPTION</span></span>
<span data-ttu-id="c778b-106">A **New-AzStorageContainerStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet hoz létre egy Azure-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="c778b-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="c778b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c778b-107">EXAMPLES</span></span>

### <span data-ttu-id="c778b-108">1. példa: Tárolt hozzáférési házirend létrehozása egy tárolóban</span><span class="sxs-lookup"><span data-stu-id="c778b-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="c778b-109">Ez a parancs létrehoz egy Policy01 nevű hozzáférési házirendet a MyContainer nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="c778b-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="c778b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c778b-110">PARAMETERS</span></span>

### <span data-ttu-id="c778b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c778b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c778b-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c778b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c778b-113">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="c778b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c778b-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c778b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c778b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c778b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c778b-116">Megadja a maximális párhuzamos hálózati hívást.</span><span class="sxs-lookup"><span data-stu-id="c778b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c778b-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="c778b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c778b-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="c778b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c778b-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c778b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c778b-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c778b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c778b-121">-Container</span><span class="sxs-lookup"><span data-stu-id="c778b-121">-Container</span></span>
<span data-ttu-id="c778b-122">Az Azure-tároló tárolónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c778b-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="c778b-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c778b-123">-Context</span></span>
<span data-ttu-id="c778b-124">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c778b-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c778b-125">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c778b-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c778b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c778b-126">-DefaultProfile</span></span>
<span data-ttu-id="c778b-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c778b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c778b-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c778b-128">-ExpiryTime</span></span>
<span data-ttu-id="c778b-129">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="c778b-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="c778b-130">-Engedély</span><span class="sxs-lookup"><span data-stu-id="c778b-130">-Permission</span></span>
<span data-ttu-id="c778b-131">A tároló eléréséhez szükséges engedélyeket adja meg a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="c778b-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="c778b-132">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="c778b-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c778b-133">-Házirend</span><span class="sxs-lookup"><span data-stu-id="c778b-133">-Policy</span></span>
<span data-ttu-id="c778b-134">Egy tárolt hozzáférési házirendet ad meg, amely tartalmazza az SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="c778b-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="c778b-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c778b-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c778b-136">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c778b-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c778b-137">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="c778b-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c778b-138">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c778b-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c778b-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c778b-139">-StartTime</span></span>
<span data-ttu-id="c778b-140">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="c778b-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="c778b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c778b-141">CommonParameters</span></span>
<span data-ttu-id="c778b-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c778b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c778b-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c778b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c778b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c778b-144">INPUTS</span></span>

### <span data-ttu-id="c778b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c778b-145">System.String</span></span>

### <span data-ttu-id="c778b-146">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c778b-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c778b-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c778b-147">OUTPUTS</span></span>

### <span data-ttu-id="c778b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c778b-148">System.String</span></span>

## <span data-ttu-id="c778b-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c778b-149">NOTES</span></span>

## <span data-ttu-id="c778b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c778b-150">RELATED LINKS</span></span>

[<span data-ttu-id="c778b-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c778b-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c778b-152">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="c778b-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c778b-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c778b-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c778b-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c778b-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


