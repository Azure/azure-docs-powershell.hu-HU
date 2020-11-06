---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac818fd403df9b159671f5889e068bda82a086d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491432"
---
# <span data-ttu-id="78bc0-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="78bc0-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="78bc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="78bc0-103">Egy Access-aláírási tokent hoz létre egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="78bc0-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="78bc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78bc0-104">SYNTAX</span></span>

### <span data-ttu-id="78bc0-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="78bc0-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="78bc0-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="78bc0-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="78bc0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="78bc0-107">DESCRIPTION</span></span>
<span data-ttu-id="78bc0-108">A **New-AzureStorageQueueSASToken** parancsmag egy Azure-tárterület-várólista esetén létrehoz egy megosztott Access-aláírási jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="78bc0-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="78bc0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="78bc0-109">EXAMPLES</span></span>

### <span data-ttu-id="78bc0-110">1. példa: a várólista-jogkivonat létrehozása teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="78bc0-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="78bc0-111">Ebben a példában egy biztonsági várólista-tokent hoz létre teljes hozzáféréssel.</span><span class="sxs-lookup"><span data-stu-id="78bc0-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="78bc0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78bc0-112">PARAMETERS</span></span>

### <span data-ttu-id="78bc0-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="78bc0-113">-Context</span></span>
<span data-ttu-id="78bc0-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78bc0-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="78bc0-115">New-AzureStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="78bc0-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="78bc0-116">-ExpiryTime</span></span>
<span data-ttu-id="78bc0-117">Azt adja meg, hogy a megosztott hozzáférés aláírása már nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="78bc0-117">Specifies when the shared access signature is no longer valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="78bc0-118">-FullUri</span></span>
<span data-ttu-id="78bc0-119">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="78bc0-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="78bc0-120">-IPAddressOrRange</span></span>
<span data-ttu-id="78bc0-121">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="78bc0-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="78bc0-122">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="78bc0-122">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78bc0-123">-Name</span></span>
<span data-ttu-id="78bc0-124">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="78bc0-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-125">– Engedély</span><span class="sxs-lookup"><span data-stu-id="78bc0-125">-Permission</span></span>
<span data-ttu-id="78bc0-126">Megadja a tárolási várólista engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="78bc0-126">Specifies permissions for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-127">-Házirend</span><span class="sxs-lookup"><span data-stu-id="78bc0-127">-Policy</span></span>
<span data-ttu-id="78bc0-128">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="78bc0-128">Specifies an Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="78bc0-129">-Protocol</span></span>
<span data-ttu-id="78bc0-130">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="78bc0-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="78bc0-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="78bc0-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="78bc0-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="78bc0-132">HttpsOnly</span></span>
* <span data-ttu-id="78bc0-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="78bc0-133">HttpsOrHttp</span></span>

<span data-ttu-id="78bc0-134">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="78bc0-134">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-135">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="78bc0-135">-StartTime</span></span>
<span data-ttu-id="78bc0-136">Azt adja meg, hogy mikor lesz érvényes a megosztott hozzáférés aláírása.</span><span class="sxs-lookup"><span data-stu-id="78bc0-136">Specifies when the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bc0-137">CommonParameters</span></span>
<span data-ttu-id="78bc0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78bc0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bc0-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78bc0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bc0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78bc0-140">INPUTS</span></span>

## <span data-ttu-id="78bc0-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78bc0-141">OUTPUTS</span></span>

## <span data-ttu-id="78bc0-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78bc0-142">NOTES</span></span>

## <span data-ttu-id="78bc0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78bc0-143">RELATED LINKS</span></span>

