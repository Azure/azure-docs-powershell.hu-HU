---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187154"
---
# <span data-ttu-id="e498d-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="e498d-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="e498d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e498d-102">SYNOPSIS</span></span>
<span data-ttu-id="e498d-103">Egy Access-aláírási tokent hoz létre egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="e498d-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="e498d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e498d-104">SYNTAX</span></span>

### <span data-ttu-id="e498d-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="e498d-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e498d-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="e498d-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e498d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e498d-107">DESCRIPTION</span></span>
<span data-ttu-id="e498d-108">A **New-AzStorageQueueSASToken** parancsmag egy Azure-tárterület-várólista esetén létrehoz egy megosztott Access-aláírási jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="e498d-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="e498d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e498d-109">EXAMPLES</span></span>

### <span data-ttu-id="e498d-110">1. példa: a várólista-jogkivonat létrehozása teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="e498d-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="e498d-111">Ebben a példában egy biztonsági várólista-tokent hoz létre teljes hozzáféréssel.</span><span class="sxs-lookup"><span data-stu-id="e498d-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="e498d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e498d-112">PARAMETERS</span></span>

### <span data-ttu-id="e498d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e498d-113">-Context</span></span>
<span data-ttu-id="e498d-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e498d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e498d-115">New-AzStorageContext parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="e498d-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e498d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e498d-116">-DefaultProfile</span></span>
<span data-ttu-id="e498d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e498d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e498d-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e498d-118">-ExpiryTime</span></span>
<span data-ttu-id="e498d-119">Azt adja meg, hogy a megosztott hozzáférés aláírása már nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="e498d-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="e498d-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e498d-120">-FullUri</span></span>
<span data-ttu-id="e498d-121">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="e498d-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e498d-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e498d-122">-IPAddressOrRange</span></span>
<span data-ttu-id="e498d-123">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="e498d-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e498d-124">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="e498d-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="e498d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e498d-125">-Name</span></span>
<span data-ttu-id="e498d-126">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e498d-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="e498d-127">– Engedély</span><span class="sxs-lookup"><span data-stu-id="e498d-127">-Permission</span></span>
<span data-ttu-id="e498d-128">Megadja a tárolási várólista engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="e498d-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="e498d-129">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="e498d-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="e498d-130">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e498d-130">-Policy</span></span>
<span data-ttu-id="e498d-131">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e498d-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="e498d-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e498d-132">-Protocol</span></span>
<span data-ttu-id="e498d-133">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e498d-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e498d-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e498d-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e498d-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e498d-135">HttpsOnly</span></span>
* <span data-ttu-id="e498d-136">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e498d-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e498d-137">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="e498d-137">-StartTime</span></span>
<span data-ttu-id="e498d-138">Azt adja meg, hogy mikor lesz érvényes a megosztott hozzáférés aláírása.</span><span class="sxs-lookup"><span data-stu-id="e498d-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e498d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e498d-139">CommonParameters</span></span>
<span data-ttu-id="e498d-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e498d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e498d-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e498d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e498d-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e498d-142">INPUTS</span></span>

### <span data-ttu-id="e498d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e498d-143">System.String</span></span>

### <span data-ttu-id="e498d-144">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e498d-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e498d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e498d-145">OUTPUTS</span></span>

### <span data-ttu-id="e498d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e498d-146">System.String</span></span>

## <span data-ttu-id="e498d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e498d-147">NOTES</span></span>

## <span data-ttu-id="e498d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e498d-148">RELATED LINKS</span></span>
