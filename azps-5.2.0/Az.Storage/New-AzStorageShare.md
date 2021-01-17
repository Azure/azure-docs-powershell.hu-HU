---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 4fa89a13f9b4124232d9459d7d3eff54a6f55a5c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324684"
---
# <span data-ttu-id="0dc49-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0dc49-101">New-AzStorageShare</span></span>

## <span data-ttu-id="0dc49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc49-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc49-103">Fájlmegosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0dc49-103">Creates a file share.</span></span>

## <span data-ttu-id="0dc49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0dc49-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dc49-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0dc49-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc49-106">A **New-AzStorageShare** parancsmag létrehoz egy fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="0dc49-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="0dc49-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0dc49-107">EXAMPLES</span></span>

### <span data-ttu-id="0dc49-108">1. példa: Fájlmegosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="0dc49-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="0dc49-109">Ez a parancs létrehoz egy ContosoShare06 nevű fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="0dc49-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="0dc49-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dc49-110">PARAMETERS</span></span>

### <span data-ttu-id="0dc49-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0dc49-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0dc49-112">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="0dc49-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0dc49-113">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="0dc49-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0dc49-114">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="0dc49-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0dc49-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0dc49-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0dc49-116">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="0dc49-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0dc49-117">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="0dc49-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0dc49-118">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="0dc49-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0dc49-119">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="0dc49-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0dc49-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0dc49-120">The default value is 10.</span></span>

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

### <span data-ttu-id="0dc49-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0dc49-121">-Context</span></span>
<span data-ttu-id="0dc49-122">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0dc49-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0dc49-123">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="0dc49-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0dc49-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc49-124">-DefaultProfile</span></span>
<span data-ttu-id="0dc49-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0dc49-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dc49-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0dc49-126">-Name</span></span>
<span data-ttu-id="0dc49-127">Egy fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0dc49-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="0dc49-128">Ez a parancsmag létrehoz egy fájlmegosztást, amely a paraméter által megadott néven rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0dc49-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc49-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0dc49-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0dc49-130">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0dc49-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0dc49-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc49-131">CommonParameters</span></span>
<span data-ttu-id="0dc49-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc49-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc49-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc49-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc49-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0dc49-134">INPUTS</span></span>

### <span data-ttu-id="0dc49-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0dc49-135">System.String</span></span>

### <span data-ttu-id="0dc49-136">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0dc49-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0dc49-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dc49-137">OUTPUTS</span></span>

### <span data-ttu-id="0dc49-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="0dc49-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="0dc49-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0dc49-139">NOTES</span></span>

## <span data-ttu-id="0dc49-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0dc49-140">RELATED LINKS</span></span>

[<span data-ttu-id="0dc49-141">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="0dc49-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="0dc49-142">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="0dc49-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0dc49-143">Remove-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="0dc49-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
