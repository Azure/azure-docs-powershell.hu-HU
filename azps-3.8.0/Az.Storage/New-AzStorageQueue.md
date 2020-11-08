---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013475"
---
# <span data-ttu-id="ddf7a-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ddf7a-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="ddf7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddf7a-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf7a-103">Tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-103">Creates a storage queue.</span></span>

## <span data-ttu-id="ddf7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddf7a-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddf7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddf7a-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf7a-106">A **New-AzStorageQueue** parancsmag létrehoz egy tárolási várólistát az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="ddf7a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ddf7a-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf7a-108">Példa 1: Azure Storage Queue létrehozása</span><span class="sxs-lookup"><span data-stu-id="ddf7a-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="ddf7a-109">Ez a példa létrehoz egy queueabc nevű tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="ddf7a-110">2. példa: több Azure-tárterületet tároló várólista létrehozása</span><span class="sxs-lookup"><span data-stu-id="ddf7a-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="ddf7a-111">Ez a példa több tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="ddf7a-112">A .NET string osztály felosztott metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="ddf7a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddf7a-113">PARAMETERS</span></span>

### <span data-ttu-id="ddf7a-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ddf7a-114">-Context</span></span>
<span data-ttu-id="ddf7a-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ddf7a-116">A New-AzStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ddf7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf7a-117">-DefaultProfile</span></span>
<span data-ttu-id="ddf7a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf7a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddf7a-119">-Name</span></span>
<span data-ttu-id="ddf7a-120">A várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="ddf7a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf7a-121">CommonParameters</span></span>
<span data-ttu-id="ddf7a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddf7a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf7a-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf7a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf7a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddf7a-124">INPUTS</span></span>

### <span data-ttu-id="ddf7a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ddf7a-125">System.String</span></span>

### <span data-ttu-id="ddf7a-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ddf7a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ddf7a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddf7a-127">OUTPUTS</span></span>

### <span data-ttu-id="ddf7a-128">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ddf7a-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="ddf7a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddf7a-129">NOTES</span></span>

## <span data-ttu-id="ddf7a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddf7a-130">RELATED LINKS</span></span>

[<span data-ttu-id="ddf7a-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ddf7a-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="ddf7a-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ddf7a-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


