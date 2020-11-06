---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: f8c419f59c05b2160ef02fbf239ecc2815bf1109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496780"
---
# <span data-ttu-id="f58d1-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f58d1-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="f58d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f58d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f58d1-103">A tárolási várólisták listája.</span><span class="sxs-lookup"><span data-stu-id="f58d1-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f58d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f58d1-104">SYNTAX</span></span>

### <span data-ttu-id="f58d1-105">QueueName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f58d1-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="f58d1-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="f58d1-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f58d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f58d1-107">DESCRIPTION</span></span>
<span data-ttu-id="f58d1-108">A **Get-AzureStorageQueue** parancsmag az Azure tárterület-fiókjához társított tárolási várólistákat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="f58d1-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="f58d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f58d1-109">EXAMPLES</span></span>

### <span data-ttu-id="f58d1-110">1. példa: az összes Azure-tároló várólistájának listázása</span><span class="sxs-lookup"><span data-stu-id="f58d1-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="f58d1-111">Ez a parancs felsorolja az aktuális tárterület-fiók tárolási várólistáit.</span><span class="sxs-lookup"><span data-stu-id="f58d1-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="f58d1-112">2. példa: az Azure tárolási várólistái a helyettesítő karakterekkel jelennek meg</span><span class="sxs-lookup"><span data-stu-id="f58d1-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="f58d1-113">A parancs egy helyettesítő karaktert használ a tárolási várólisták listájának megjelenítéséhez, amelynek a neve a várólistával fog kezdődni.</span><span class="sxs-lookup"><span data-stu-id="f58d1-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="f58d1-114">3. példa: az Azure tárolási várólistái a várólista neve előtag használatával</span><span class="sxs-lookup"><span data-stu-id="f58d1-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="f58d1-115">Ebben a példában az *előtag* paraméterrel kilistázhatja azokat a tárolási várólistákat, amelyeknek a neve a várólistával fog kezdődni.</span><span class="sxs-lookup"><span data-stu-id="f58d1-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="f58d1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f58d1-116">PARAMETERS</span></span>

### <span data-ttu-id="f58d1-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f58d1-117">-Context</span></span>
<span data-ttu-id="f58d1-118">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f58d1-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f58d1-119">Ezt a **New-AzureStorageContext** parancsmag segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="f58d1-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="f58d1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f58d1-120">-Name</span></span>
<span data-ttu-id="f58d1-121">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="f58d1-121">Specifies a name.</span></span>
<span data-ttu-id="f58d1-122">Ha nincs megadva név, a parancsmag felsorolja az összes várólistát.</span><span class="sxs-lookup"><span data-stu-id="f58d1-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="f58d1-123">Ha meg van adva egy teljes vagy részleges név, a parancsmag minden olyan várólistát kap, amely megfelel a név mintának.</span><span class="sxs-lookup"><span data-stu-id="f58d1-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="f58d1-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="f58d1-124">-Prefix</span></span>
<span data-ttu-id="f58d1-125">A bekapni kívánt várólisták nevében használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f58d1-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f58d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58d1-126">CommonParameters</span></span>
<span data-ttu-id="f58d1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f58d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58d1-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f58d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58d1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f58d1-129">INPUTS</span></span>

### <span data-ttu-id="f58d1-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f58d1-130">IStorageContext</span></span>

<span data-ttu-id="f58d1-131">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f58d1-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="f58d1-132">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f58d1-132">String</span></span>

<span data-ttu-id="f58d1-133">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f58d1-133">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f58d1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f58d1-134">OUTPUTS</span></span>

### <span data-ttu-id="f58d1-135">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f58d1-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="f58d1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f58d1-136">NOTES</span></span>

## <span data-ttu-id="f58d1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f58d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="f58d1-138">Új – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f58d1-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="f58d1-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f58d1-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


