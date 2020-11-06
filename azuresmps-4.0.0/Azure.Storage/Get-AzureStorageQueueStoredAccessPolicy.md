---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491728"
---
# <span data-ttu-id="ef1ed-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef1ed-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ef1ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1ed-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ef1ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef1ed-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef1ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef1ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ef1ed-106">A **Get-AzureStorageQueueStoredAccessPolicy** parancsmag felsorolja az Azure-tárterületek várólistájának tárolt elérési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ef1ed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef1ed-107">EXAMPLES</span></span>

### <span data-ttu-id="ef1ed-108">1. példa: tárolt hozzáférési házirend beszerzése a várólistában</span><span class="sxs-lookup"><span data-stu-id="ef1ed-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="ef1ed-109">Ez a parancs a Policy12 nevű Access-házirendet a MyQueue nevű tárolási várólistában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="ef1ed-110">2. példa: az összes tárolt Access-házirend beolvasása a várólistán</span><span class="sxs-lookup"><span data-stu-id="ef1ed-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="ef1ed-111">Ez a parancs a MyQueue nevű várólistában minden tárolt Access-házirendet beolvas.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="ef1ed-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef1ed-112">PARAMETERS</span></span>

### <span data-ttu-id="ef1ed-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ef1ed-113">-Context</span></span>
<span data-ttu-id="ef1ed-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ef1ed-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ef1ed-116">-Házirend</span><span class="sxs-lookup"><span data-stu-id="ef1ed-116">-Policy</span></span>
<span data-ttu-id="ef1ed-117">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="ef1ed-118">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="ef1ed-118">-Queue</span></span>
<span data-ttu-id="ef1ed-119">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef1ed-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ef1ed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1ed-120">CommonParameters</span></span>
<span data-ttu-id="ef1ed-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef1ed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1ed-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1ed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1ed-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1ed-123">INPUTS</span></span>

## <span data-ttu-id="ef1ed-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1ed-124">OUTPUTS</span></span>

## <span data-ttu-id="ef1ed-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef1ed-125">NOTES</span></span>

## <span data-ttu-id="ef1ed-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef1ed-126">RELATED LINKS</span></span>

[<span data-ttu-id="ef1ed-127">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef1ed-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ef1ed-128">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef1ed-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ef1ed-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef1ed-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ef1ed-130">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef1ed-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


