---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491435"
---
# <span data-ttu-id="8c3d9-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8c3d9-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="8c3d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3d9-103">Tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-103">Creates a storage queue.</span></span>

## <span data-ttu-id="8c3d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c3d9-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="8c3d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c3d9-105">DESCRIPTION</span></span>
<span data-ttu-id="8c3d9-106">A **New-AzureStorageQueue** parancsmag létrehoz egy tárolási várólistát az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="8c3d9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c3d9-107">EXAMPLES</span></span>

### <span data-ttu-id="8c3d9-108">Példa 1: Azure Storage Queue létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c3d9-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="8c3d9-109">Ez a példa létrehoz egy queueabc nevű tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="8c3d9-110">2. példa: több Azure-tárterületet tároló várólista létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c3d9-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="8c3d9-111">Ez a példa több tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="8c3d9-112">A .NET string osztály felosztott metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="8c3d9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c3d9-113">PARAMETERS</span></span>

### <span data-ttu-id="8c3d9-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8c3d9-114">-Context</span></span>
<span data-ttu-id="8c3d9-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8c3d9-116">A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8c3d9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c3d9-117">-Name</span></span>
<span data-ttu-id="8c3d9-118">A várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="8c3d9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3d9-119">CommonParameters</span></span>
<span data-ttu-id="8c3d9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c3d9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3d9-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c3d9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3d9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c3d9-122">INPUTS</span></span>

## <span data-ttu-id="8c3d9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c3d9-123">OUTPUTS</span></span>

## <span data-ttu-id="8c3d9-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c3d9-124">NOTES</span></span>

## <span data-ttu-id="8c3d9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c3d9-125">RELATED LINKS</span></span>

[<span data-ttu-id="8c3d9-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8c3d9-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="8c3d9-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8c3d9-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


