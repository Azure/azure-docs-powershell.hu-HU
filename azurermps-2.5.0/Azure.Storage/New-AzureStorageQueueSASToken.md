---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
ms.openlocfilehash: b002f518d63fb3ed4ed34d007f72b57e4db41ae5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849814"
---
# <span data-ttu-id="8f80c-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="8f80c-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="8f80c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f80c-102">SYNOPSIS</span></span>
<span data-ttu-id="8f80c-103">Egy Access-aláírási tokent hoz létre egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="8f80c-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f80c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f80c-104">SYNTAX</span></span>

### <span data-ttu-id="8f80c-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="8f80c-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f80c-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="8f80c-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f80c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f80c-107">DESCRIPTION</span></span>
<span data-ttu-id="8f80c-108">A **New-AzureStorageQueueSASToken** parancsmag egy Azure-tárterület-várólista esetén létrehoz egy megosztott Access-aláírási jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="8f80c-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="8f80c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8f80c-109">EXAMPLES</span></span>

### <span data-ttu-id="8f80c-110">1. példa: a várólista-jogkivonat létrehozása teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="8f80c-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="8f80c-111">Ebben a példában egy biztonsági várólista-tokent hoz létre teljes hozzáféréssel.</span><span class="sxs-lookup"><span data-stu-id="8f80c-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="8f80c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f80c-112">PARAMETERS</span></span>

### <span data-ttu-id="8f80c-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8f80c-113">-Context</span></span>
<span data-ttu-id="8f80c-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f80c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8f80c-115">New-AzureStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="8f80c-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8f80c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f80c-116">-DefaultProfile</span></span>
<span data-ttu-id="8f80c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f80c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f80c-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8f80c-118">-ExpiryTime</span></span>
<span data-ttu-id="8f80c-119">Azt adja meg, hogy a megosztott hozzáférés aláírása már nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="8f80c-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="8f80c-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8f80c-120">-FullUri</span></span>
<span data-ttu-id="8f80c-121">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8f80c-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f80c-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8f80c-122">-IPAddressOrRange</span></span>
<span data-ttu-id="8f80c-123">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="8f80c-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8f80c-124">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="8f80c-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="8f80c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f80c-125">-Name</span></span>
<span data-ttu-id="8f80c-126">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f80c-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f80c-127">– Engedély</span><span class="sxs-lookup"><span data-stu-id="8f80c-127">-Permission</span></span>
<span data-ttu-id="8f80c-128">Megadja a tárolási várólista engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="8f80c-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="8f80c-129">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="8f80c-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f80c-130">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8f80c-130">-Policy</span></span>
<span data-ttu-id="8f80c-131">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f80c-131">Specifies an Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f80c-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8f80c-132">-Protocol</span></span>
<span data-ttu-id="8f80c-133">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f80c-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8f80c-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8f80c-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8f80c-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8f80c-135">HttpsOnly</span></span>
* <span data-ttu-id="8f80c-136">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8f80c-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f80c-137">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="8f80c-137">-StartTime</span></span>
<span data-ttu-id="8f80c-138">Azt adja meg, hogy mikor lesz érvényes a megosztott hozzáférés aláírása.</span><span class="sxs-lookup"><span data-stu-id="8f80c-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="8f80c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f80c-139">CommonParameters</span></span>
<span data-ttu-id="8f80c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f80c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f80c-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f80c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f80c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f80c-142">INPUTS</span></span>

### <span data-ttu-id="8f80c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8f80c-143">System.String</span></span>

### <span data-ttu-id="8f80c-144">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f80c-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8f80c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f80c-145">OUTPUTS</span></span>

### <span data-ttu-id="8f80c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8f80c-146">System.String</span></span>

## <span data-ttu-id="8f80c-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f80c-147">NOTES</span></span>

## <span data-ttu-id="8f80c-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f80c-148">RELATED LINKS</span></span>
