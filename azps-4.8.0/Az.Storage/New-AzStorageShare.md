---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 4fa89a13f9b4124232d9459d7d3eff54a6f55a5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180777"
---
# <span data-ttu-id="93d4b-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="93d4b-101">New-AzStorageShare</span></span>

## <span data-ttu-id="93d4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="93d4b-103">Létrehozza a fájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="93d4b-103">Creates a file share.</span></span>

## <span data-ttu-id="93d4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93d4b-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="93d4b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="93d4b-106">A **New-AzStorageShare** parancsmag létrehoz egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="93d4b-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="93d4b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93d4b-107">EXAMPLES</span></span>

### <span data-ttu-id="93d4b-108">Példa 1: fájlmegosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="93d4b-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="93d4b-109">Ez a parancs létrehoz egy ContosoShare06 nevű fájlmegosztás-megosztást.</span><span class="sxs-lookup"><span data-stu-id="93d4b-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="93d4b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93d4b-110">PARAMETERS</span></span>

### <span data-ttu-id="93d4b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93d4b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="93d4b-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="93d4b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="93d4b-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="93d4b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="93d4b-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="93d4b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="93d4b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="93d4b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="93d4b-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="93d4b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="93d4b-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="93d4b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="93d4b-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="93d4b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="93d4b-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="93d4b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="93d4b-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="93d4b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="93d4b-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="93d4b-121">-Context</span></span>
<span data-ttu-id="93d4b-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93d4b-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="93d4b-123">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="93d4b-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="93d4b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d4b-124">-DefaultProfile</span></span>
<span data-ttu-id="93d4b-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93d4b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93d4b-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93d4b-126">-Name</span></span>
<span data-ttu-id="93d4b-127">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93d4b-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="93d4b-128">Ez a parancsmag létrehoz egy olyan fájlmegosztás nevű fájlt, amely a paraméter által megadott névvel van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="93d4b-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="93d4b-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93d4b-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="93d4b-130">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="93d4b-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="93d4b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d4b-131">CommonParameters</span></span>
<span data-ttu-id="93d4b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93d4b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d4b-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d4b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d4b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93d4b-134">INPUTS</span></span>

### <span data-ttu-id="93d4b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="93d4b-135">System.String</span></span>

### <span data-ttu-id="93d4b-136">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="93d4b-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93d4b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93d4b-137">OUTPUTS</span></span>

### <span data-ttu-id="93d4b-138">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="93d4b-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="93d4b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93d4b-139">NOTES</span></span>

## <span data-ttu-id="93d4b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93d4b-140">RELATED LINKS</span></span>

[<span data-ttu-id="93d4b-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="93d4b-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="93d4b-142">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="93d4b-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="93d4b-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="93d4b-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
