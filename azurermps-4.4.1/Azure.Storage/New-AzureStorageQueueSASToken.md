---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 904305e383803e8ef672a82689794296f7c9b84d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505711"
---
# <span data-ttu-id="3b174-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="3b174-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="3b174-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b174-102">SYNOPSIS</span></span>
<span data-ttu-id="3b174-103">Egy Access-aláírási tokent hoz létre egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="3b174-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b174-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b174-104">SYNTAX</span></span>

### <span data-ttu-id="3b174-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="3b174-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="3b174-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="3b174-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="3b174-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b174-107">DESCRIPTION</span></span>
<span data-ttu-id="3b174-108">A **New-AzureStorageQueueSASToken** parancsmag egy Azure-tárterület-várólista esetén létrehoz egy megosztott Access-aláírási jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="3b174-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="3b174-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3b174-109">EXAMPLES</span></span>

### <span data-ttu-id="3b174-110">1. példa: a várólista-jogkivonat létrehozása teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="3b174-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="3b174-111">Ebben a példában egy biztonsági várólista-tokent hoz létre teljes hozzáféréssel.</span><span class="sxs-lookup"><span data-stu-id="3b174-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="3b174-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b174-112">PARAMETERS</span></span>

### <span data-ttu-id="3b174-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3b174-113">-Context</span></span>
<span data-ttu-id="3b174-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b174-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3b174-115">New-AzureStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="3b174-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3b174-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3b174-116">-ExpiryTime</span></span>
<span data-ttu-id="3b174-117">Azt adja meg, hogy a megosztott hozzáférés aláírása már nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="3b174-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="3b174-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3b174-118">-FullUri</span></span>
<span data-ttu-id="3b174-119">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3b174-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="3b174-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3b174-120">-IPAddressOrRange</span></span>
<span data-ttu-id="3b174-121">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3b174-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3b174-122">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="3b174-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="3b174-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b174-123">-Name</span></span>
<span data-ttu-id="3b174-124">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b174-124">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="3b174-125">– Engedély</span><span class="sxs-lookup"><span data-stu-id="3b174-125">-Permission</span></span>
<span data-ttu-id="3b174-126">Megadja a tárolási várólista engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="3b174-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="3b174-127">-Házirend</span><span class="sxs-lookup"><span data-stu-id="3b174-127">-Policy</span></span>
<span data-ttu-id="3b174-128">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b174-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="3b174-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3b174-129">-Protocol</span></span>
<span data-ttu-id="3b174-130">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b174-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3b174-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3b174-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3b174-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3b174-132">HttpsOnly</span></span>
* <span data-ttu-id="3b174-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="3b174-133">HttpsOrHttp</span></span>

<span data-ttu-id="3b174-134">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3b174-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3b174-135">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="3b174-135">-StartTime</span></span>
<span data-ttu-id="3b174-136">Azt adja meg, hogy mikor lesz érvényes a megosztott hozzáférés aláírása.</span><span class="sxs-lookup"><span data-stu-id="3b174-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="3b174-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b174-137">CommonParameters</span></span>
<span data-ttu-id="3b174-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b174-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b174-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b174-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b174-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b174-140">INPUTS</span></span>

### <span data-ttu-id="3b174-141">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b174-141">IStorageContext</span></span>

<span data-ttu-id="3b174-142">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3b174-142">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3b174-143">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="3b174-143">String</span></span>

<span data-ttu-id="3b174-144">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3b174-144">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3b174-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b174-145">OUTPUTS</span></span>

### <span data-ttu-id="3b174-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3b174-146">System.String</span></span>

## <span data-ttu-id="3b174-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b174-147">NOTES</span></span>

## <span data-ttu-id="3b174-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b174-148">RELATED LINKS</span></span>

