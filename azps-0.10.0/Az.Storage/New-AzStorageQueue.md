---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1ce3615d7eeef4986f1fefd20ec5be2ea1aaac7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842990"
---
# <span data-ttu-id="2c431-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2c431-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="2c431-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c431-102">SYNOPSIS</span></span>
<span data-ttu-id="2c431-103">Tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2c431-103">Creates a storage queue.</span></span>

## <span data-ttu-id="2c431-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c431-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c431-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c431-105">DESCRIPTION</span></span>
<span data-ttu-id="2c431-106">A **New-AzStorageQueue** parancsmag létrehoz egy tárolási várólistát az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2c431-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="2c431-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2c431-107">EXAMPLES</span></span>

### <span data-ttu-id="2c431-108">Példa 1: Azure Storage Queue létrehozása</span><span class="sxs-lookup"><span data-stu-id="2c431-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="2c431-109">Ez a példa létrehoz egy queueabc nevű tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="2c431-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="2c431-110">2. példa: több Azure-tárterületet tároló várólista létrehozása</span><span class="sxs-lookup"><span data-stu-id="2c431-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="2c431-111">Ez a példa több tárolási várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2c431-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="2c431-112">A .NET string osztály felosztott metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="2c431-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="2c431-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c431-113">PARAMETERS</span></span>

### <span data-ttu-id="2c431-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2c431-114">-Context</span></span>
<span data-ttu-id="2c431-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c431-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2c431-116">A New-AzStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="2c431-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2c431-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c431-117">-DefaultProfile</span></span>
<span data-ttu-id="2c431-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c431-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c431-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c431-119">-Name</span></span>
<span data-ttu-id="2c431-120">A várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c431-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="2c431-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c431-121">CommonParameters</span></span>
<span data-ttu-id="2c431-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c431-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c431-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c431-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c431-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c431-124">INPUTS</span></span>

### <span data-ttu-id="2c431-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2c431-125">System.String</span></span>

### <span data-ttu-id="2c431-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c431-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2c431-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c431-127">OUTPUTS</span></span>

### <span data-ttu-id="2c431-128">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2c431-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="2c431-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c431-129">NOTES</span></span>

## <span data-ttu-id="2c431-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c431-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c431-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2c431-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="2c431-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2c431-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


