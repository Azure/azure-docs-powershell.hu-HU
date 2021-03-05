---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6e7230ad6cb2bd3f58ebd3328aa20fe3c1bf2bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002501"
---
# <span data-ttu-id="7508d-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7508d-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="7508d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7508d-102">SYNOPSIS</span></span>
<span data-ttu-id="7508d-103">Tárolt hozzáférési házirendet hoz létre egy Azure-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="7508d-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="7508d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7508d-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7508d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7508d-105">DESCRIPTION</span></span>
<span data-ttu-id="7508d-106">A **New-AzStorageContainerStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet hoz létre egy Azure-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="7508d-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="7508d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7508d-107">EXAMPLES</span></span>

### <span data-ttu-id="7508d-108">1. példa: Tárolt hozzáférési házirend létrehozása egy tárolóban</span><span class="sxs-lookup"><span data-stu-id="7508d-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="7508d-109">Ez a parancs létrehoz egy Policy01 nevű hozzáférési házirendet a MyContainer nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="7508d-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="7508d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7508d-110">PARAMETERS</span></span>

### <span data-ttu-id="7508d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7508d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7508d-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7508d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7508d-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="7508d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7508d-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="7508d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7508d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7508d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7508d-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="7508d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7508d-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="7508d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7508d-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="7508d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7508d-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7508d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7508d-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7508d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7508d-121">-Container</span><span class="sxs-lookup"><span data-stu-id="7508d-121">-Container</span></span>
<span data-ttu-id="7508d-122">Az Azure-tároló tárolónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7508d-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="7508d-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7508d-123">-Context</span></span>
<span data-ttu-id="7508d-124">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7508d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7508d-125">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7508d-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7508d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7508d-126">-DefaultProfile</span></span>
<span data-ttu-id="7508d-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7508d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7508d-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7508d-128">-ExpiryTime</span></span>
<span data-ttu-id="7508d-129">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="7508d-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7508d-130">-Engedély</span><span class="sxs-lookup"><span data-stu-id="7508d-130">-Permission</span></span>
<span data-ttu-id="7508d-131">A tároló eléréséhez szükséges engedélyeket adja meg a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="7508d-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="7508d-132">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="7508d-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7508d-133">-Házirend</span><span class="sxs-lookup"><span data-stu-id="7508d-133">-Policy</span></span>
<span data-ttu-id="7508d-134">Egy tárolt hozzáférési házirendet ad meg, amely tartalmazza az SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="7508d-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="7508d-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7508d-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7508d-136">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7508d-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7508d-137">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="7508d-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7508d-138">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="7508d-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7508d-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7508d-139">-StartTime</span></span>
<span data-ttu-id="7508d-140">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="7508d-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7508d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7508d-141">CommonParameters</span></span>
<span data-ttu-id="7508d-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7508d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7508d-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7508d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7508d-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7508d-144">INPUTS</span></span>

### <span data-ttu-id="7508d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7508d-145">System.String</span></span>

### <span data-ttu-id="7508d-146">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7508d-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7508d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7508d-147">OUTPUTS</span></span>

### <span data-ttu-id="7508d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7508d-148">System.String</span></span>

## <span data-ttu-id="7508d-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7508d-149">NOTES</span></span>

## <span data-ttu-id="7508d-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7508d-150">RELATED LINKS</span></span>

[<span data-ttu-id="7508d-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7508d-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7508d-152">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="7508d-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7508d-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7508d-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7508d-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7508d-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


