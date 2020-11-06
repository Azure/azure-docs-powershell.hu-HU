---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496732"
---
# <span data-ttu-id="5780e-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5780e-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="5780e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5780e-102">SYNOPSIS</span></span>
<span data-ttu-id="5780e-103">Tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5780e-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5780e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5780e-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5780e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5780e-105">DESCRIPTION</span></span>
<span data-ttu-id="5780e-106">A **New-AzureStorageQueue** parancsmag létrehoz egy tárolási várólistát az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="5780e-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="5780e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5780e-107">EXAMPLES</span></span>

### <span data-ttu-id="5780e-108">Példa 1: Azure Storage Queue létrehozása</span><span class="sxs-lookup"><span data-stu-id="5780e-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="5780e-109">Ez a példa létrehoz egy queueabc nevű tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="5780e-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="5780e-110">2. példa: több Azure-tárterületet tároló várólista létrehozása</span><span class="sxs-lookup"><span data-stu-id="5780e-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="5780e-111">Ez a példa több tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5780e-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="5780e-112">A .NET string osztály felosztott metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="5780e-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="5780e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5780e-113">PARAMETERS</span></span>

### <span data-ttu-id="5780e-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5780e-114">-Context</span></span>
<span data-ttu-id="5780e-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5780e-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5780e-116">A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="5780e-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5780e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5780e-117">-Name</span></span>
<span data-ttu-id="5780e-118">A várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5780e-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="5780e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5780e-119">CommonParameters</span></span>
<span data-ttu-id="5780e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5780e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5780e-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5780e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5780e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5780e-122">INPUTS</span></span>

### <span data-ttu-id="5780e-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5780e-123">IStorageContext</span></span>

<span data-ttu-id="5780e-124">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5780e-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5780e-125">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="5780e-125">String</span></span>

<span data-ttu-id="5780e-126">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5780e-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5780e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5780e-127">OUTPUTS</span></span>

### <span data-ttu-id="5780e-128">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5780e-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="5780e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5780e-129">NOTES</span></span>

## <span data-ttu-id="5780e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5780e-130">RELATED LINKS</span></span>

[<span data-ttu-id="5780e-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5780e-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="5780e-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5780e-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


