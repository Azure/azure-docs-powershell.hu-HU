---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324922"
---
# <span data-ttu-id="8bcca-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcca-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="8bcca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bcca-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcca-103">Tárterület-megosztáshoz tárolt hozzáférési házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="8bcca-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="8bcca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8bcca-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8bcca-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8bcca-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcca-106">A **Get-AzStorageShareStoredAccessPolicy** parancsmag tárolja egy Azure Storage-megosztás hozzáférési házirendeit.</span><span class="sxs-lookup"><span data-stu-id="8bcca-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="8bcca-107">Ha egy adott házirendet be kell szereznie, adja meg név szerint.</span><span class="sxs-lookup"><span data-stu-id="8bcca-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="8bcca-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8bcca-108">EXAMPLES</span></span>

### <span data-ttu-id="8bcca-109">1. példa: Tárolt hozzáférési házirend lekért megosztása</span><span class="sxs-lookup"><span data-stu-id="8bcca-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="8bcca-110">Ez a parancs egy GeneralPolicy nevű tárolt hozzáférési házirendet kap a ContosoShare szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8bcca-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="8bcca-111">2. példa: Az összes tárolt hozzáférési házirend megosztása</span><span class="sxs-lookup"><span data-stu-id="8bcca-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="8bcca-112">Ez a parancs a ContosoShare szolgáltatásban tárolt összes hozzáférési házirendet beveszi.</span><span class="sxs-lookup"><span data-stu-id="8bcca-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="8bcca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bcca-113">PARAMETERS</span></span>

### <span data-ttu-id="8bcca-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bcca-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8bcca-115">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8bcca-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8bcca-116">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="8bcca-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8bcca-117">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8bcca-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8bcca-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8bcca-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8bcca-119">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="8bcca-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8bcca-120">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="8bcca-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8bcca-121">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="8bcca-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8bcca-122">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="8bcca-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8bcca-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8bcca-123">The default value is 10.</span></span>

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

### <span data-ttu-id="8bcca-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8bcca-124">-Context</span></span>
<span data-ttu-id="8bcca-125">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bcca-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="8bcca-126">Környezet beszerzéséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8bcca-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8bcca-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcca-127">-DefaultProfile</span></span>
<span data-ttu-id="8bcca-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bcca-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bcca-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8bcca-129">-Policy</span></span>
<span data-ttu-id="8bcca-130">A parancsmag által tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bcca-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcca-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bcca-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8bcca-132">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bcca-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8bcca-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8bcca-133">-ShareName</span></span>
<span data-ttu-id="8bcca-134">Azt a tárterület-megosztásnevet adja meg, amelyhez a parancsmag házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="8bcca-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="8bcca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcca-135">CommonParameters</span></span>
<span data-ttu-id="8bcca-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bcca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcca-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bcca-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcca-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bcca-138">INPUTS</span></span>

### <span data-ttu-id="8bcca-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8bcca-139">System.String</span></span>

### <span data-ttu-id="8bcca-140">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bcca-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8bcca-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bcca-141">OUTPUTS</span></span>

### <span data-ttu-id="8bcca-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="8bcca-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="8bcca-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8bcca-143">NOTES</span></span>

## <span data-ttu-id="8bcca-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bcca-144">RELATED LINKS</span></span>

[<span data-ttu-id="8bcca-145">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="8bcca-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8bcca-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcca-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8bcca-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcca-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8bcca-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcca-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
