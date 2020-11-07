---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 30b789ac2b4b94d897379fd421396fe68aba801f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839772"
---
# <span data-ttu-id="59ce0-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59ce0-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="59ce0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="59ce0-103">Tárol egy tárolt hozzáférési házirendet egy Azure tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="59ce0-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="59ce0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59ce0-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="59ce0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="59ce0-106">A **New-AzStorageContainerStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure Storage tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="59ce0-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="59ce0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="59ce0-108">Példa 1: tárolt hozzáférés-házirend létrehozása tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="59ce0-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="59ce0-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyContainer nevű tároló tárolóban.</span><span class="sxs-lookup"><span data-stu-id="59ce0-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="59ce0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59ce0-110">PARAMETERS</span></span>

### <span data-ttu-id="59ce0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59ce0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="59ce0-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="59ce0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="59ce0-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="59ce0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="59ce0-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="59ce0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="59ce0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="59ce0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="59ce0-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="59ce0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="59ce0-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="59ce0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="59ce0-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="59ce0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="59ce0-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="59ce0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="59ce0-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="59ce0-120">The default value is 10.</span></span>

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

### <span data-ttu-id="59ce0-121">-Container</span><span class="sxs-lookup"><span data-stu-id="59ce0-121">-Container</span></span>
<span data-ttu-id="59ce0-122">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59ce0-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="59ce0-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="59ce0-123">-Context</span></span>
<span data-ttu-id="59ce0-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59ce0-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="59ce0-125">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="59ce0-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="59ce0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ce0-126">-DefaultProfile</span></span>
<span data-ttu-id="59ce0-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59ce0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59ce0-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="59ce0-128">-ExpiryTime</span></span>
<span data-ttu-id="59ce0-129">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="59ce0-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="59ce0-130">– Engedély</span><span class="sxs-lookup"><span data-stu-id="59ce0-130">-Permission</span></span>
<span data-ttu-id="59ce0-131">A tároló elérési házirendjében szereplő engedélyeket adja meg.</span><span class="sxs-lookup"><span data-stu-id="59ce0-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="59ce0-132">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="59ce0-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="59ce0-133">-Házirend</span><span class="sxs-lookup"><span data-stu-id="59ce0-133">-Policy</span></span>
<span data-ttu-id="59ce0-134">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="59ce0-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="59ce0-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59ce0-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="59ce0-136">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="59ce0-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="59ce0-137">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="59ce0-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="59ce0-138">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="59ce0-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="59ce0-139">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="59ce0-139">-StartTime</span></span>
<span data-ttu-id="59ce0-140">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="59ce0-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="59ce0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ce0-141">CommonParameters</span></span>
<span data-ttu-id="59ce0-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59ce0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ce0-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ce0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ce0-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59ce0-144">INPUTS</span></span>

### <span data-ttu-id="59ce0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="59ce0-145">System.String</span></span>

### <span data-ttu-id="59ce0-146">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59ce0-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59ce0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59ce0-147">OUTPUTS</span></span>

### <span data-ttu-id="59ce0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="59ce0-148">System.String</span></span>

## <span data-ttu-id="59ce0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59ce0-149">NOTES</span></span>

## <span data-ttu-id="59ce0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59ce0-150">RELATED LINKS</span></span>

[<span data-ttu-id="59ce0-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59ce0-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="59ce0-152">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59ce0-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="59ce0-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59ce0-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="59ce0-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59ce0-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


