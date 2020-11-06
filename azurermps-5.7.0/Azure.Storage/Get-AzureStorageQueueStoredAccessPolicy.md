---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ebf5596ba63a86e3865c5a6dc05bdea648dc18c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496767"
---
# <span data-ttu-id="8ecaf-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecaf-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="8ecaf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ecaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecaf-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ecaf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ecaf-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ecaf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ecaf-105">DESCRIPTION</span></span>
<span data-ttu-id="8ecaf-106">A **Get-AzureStorageQueueStoredAccessPolicy** parancsmag felsorolja az Azure-tárterületek várólistájának tárolt elérési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="8ecaf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8ecaf-107">EXAMPLES</span></span>

### <span data-ttu-id="8ecaf-108">1. példa: tárolt hozzáférési házirend beszerzése a várólistában</span><span class="sxs-lookup"><span data-stu-id="8ecaf-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="8ecaf-109">Ez a parancs a Policy12 nevű Access-házirendet a MyQueue nevű tárolási várólistában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="8ecaf-110">2. példa: az összes tárolt Access-házirend beolvasása a várólistán</span><span class="sxs-lookup"><span data-stu-id="8ecaf-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="8ecaf-111">Ez a parancs a MyQueue nevű várólistában minden tárolt Access-házirendet beolvas.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="8ecaf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ecaf-112">PARAMETERS</span></span>

### <span data-ttu-id="8ecaf-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8ecaf-113">-Context</span></span>
<span data-ttu-id="8ecaf-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8ecaf-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8ecaf-116">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8ecaf-116">-Policy</span></span>
<span data-ttu-id="8ecaf-117">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecaf-118">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="8ecaf-118">-Queue</span></span>
<span data-ttu-id="8ecaf-119">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecaf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecaf-120">CommonParameters</span></span>
<span data-ttu-id="8ecaf-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ecaf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecaf-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecaf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecaf-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ecaf-123">INPUTS</span></span>

### <span data-ttu-id="8ecaf-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ecaf-124">IStorageContext</span></span>

<span data-ttu-id="8ecaf-125">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8ecaf-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8ecaf-126">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8ecaf-126">String</span></span>

<span data-ttu-id="8ecaf-127">A "várólista" paraméter a folyamat "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="8ecaf-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8ecaf-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ecaf-128">OUTPUTS</span></span>

### <span data-ttu-id="8ecaf-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="8ecaf-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="8ecaf-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ecaf-130">NOTES</span></span>

## <span data-ttu-id="8ecaf-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ecaf-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ecaf-132">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecaf-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8ecaf-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecaf-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8ecaf-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecaf-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8ecaf-135">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ecaf-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


