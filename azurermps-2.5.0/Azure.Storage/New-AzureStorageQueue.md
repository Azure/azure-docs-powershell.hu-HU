---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849818"
---
# <span data-ttu-id="401a9-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="401a9-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="401a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="401a9-102">SYNOPSIS</span></span>
<span data-ttu-id="401a9-103">Tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="401a9-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="401a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="401a9-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="401a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="401a9-105">DESCRIPTION</span></span>
<span data-ttu-id="401a9-106">A **New-AzureStorageQueue** parancsmag létrehoz egy tárolási várólistát az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="401a9-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="401a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="401a9-107">EXAMPLES</span></span>

### <span data-ttu-id="401a9-108">Példa 1: Azure Storage Queue létrehozása</span><span class="sxs-lookup"><span data-stu-id="401a9-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="401a9-109">Ez a példa létrehoz egy queueabc nevű tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="401a9-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="401a9-110">2. példa: több Azure-tárterületet tároló várólista létrehozása</span><span class="sxs-lookup"><span data-stu-id="401a9-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="401a9-111">Ez a példa több tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="401a9-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="401a9-112">A .NET string osztály felosztott metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="401a9-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="401a9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="401a9-113">PARAMETERS</span></span>

### <span data-ttu-id="401a9-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="401a9-114">-Context</span></span>
<span data-ttu-id="401a9-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="401a9-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="401a9-116">A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="401a9-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="401a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401a9-117">-DefaultProfile</span></span>
<span data-ttu-id="401a9-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="401a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="401a9-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="401a9-119">-Name</span></span>
<span data-ttu-id="401a9-120">A várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="401a9-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="401a9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401a9-121">CommonParameters</span></span>
<span data-ttu-id="401a9-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="401a9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401a9-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="401a9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401a9-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="401a9-124">INPUTS</span></span>

### <span data-ttu-id="401a9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="401a9-125">System.String</span></span>

### <span data-ttu-id="401a9-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="401a9-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="401a9-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="401a9-127">OUTPUTS</span></span>

### <span data-ttu-id="401a9-128">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="401a9-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="401a9-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="401a9-129">NOTES</span></span>

## <span data-ttu-id="401a9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="401a9-130">RELATED LINKS</span></span>

[<span data-ttu-id="401a9-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="401a9-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="401a9-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="401a9-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


