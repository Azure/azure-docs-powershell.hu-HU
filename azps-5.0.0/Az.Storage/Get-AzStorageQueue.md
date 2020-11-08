---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186345"
---
# <span data-ttu-id="5ceee-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5ceee-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="5ceee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ceee-102">SYNOPSIS</span></span>
<span data-ttu-id="5ceee-103">A tárolási várólisták listája.</span><span class="sxs-lookup"><span data-stu-id="5ceee-103">Lists storage queues.</span></span>

## <span data-ttu-id="5ceee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ceee-104">SYNTAX</span></span>

### <span data-ttu-id="5ceee-105">QueueName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ceee-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ceee-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="5ceee-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ceee-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ceee-107">DESCRIPTION</span></span>
<span data-ttu-id="5ceee-108">A **Get-AzStorageQueue** parancsmag az Azure tárterület-fiókjához társított tárolási várólistákat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="5ceee-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="5ceee-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5ceee-109">EXAMPLES</span></span>

### <span data-ttu-id="5ceee-110">1. példa: az összes Azure-tároló várólistájának listázása</span><span class="sxs-lookup"><span data-stu-id="5ceee-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="5ceee-111">Ez a parancs felsorolja az aktuális tárterület-fiók tárolási várólistáit.</span><span class="sxs-lookup"><span data-stu-id="5ceee-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="5ceee-112">2. példa: az Azure tárolási várólistái a helyettesítő karakterekkel jelennek meg</span><span class="sxs-lookup"><span data-stu-id="5ceee-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="5ceee-113">A parancs egy helyettesítő karaktert használ a tárolási várólisták listájának megjelenítéséhez, amelynek a neve a várólistával fog kezdődni.</span><span class="sxs-lookup"><span data-stu-id="5ceee-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="5ceee-114">3. példa: az Azure tárolási várólistái a várólista neve előtag használatával</span><span class="sxs-lookup"><span data-stu-id="5ceee-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="5ceee-115">Ebben a példában az *előtag* paraméterrel kilistázhatja azokat a tárolási várólistákat, amelyeknek a neve a várólistával fog kezdődni.</span><span class="sxs-lookup"><span data-stu-id="5ceee-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="5ceee-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ceee-116">PARAMETERS</span></span>

### <span data-ttu-id="5ceee-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5ceee-117">-Context</span></span>
<span data-ttu-id="5ceee-118">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ceee-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5ceee-119">Ezt a **New-AzStorageContext** parancsmag segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="5ceee-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="5ceee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ceee-120">-DefaultProfile</span></span>
<span data-ttu-id="5ceee-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ceee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ceee-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ceee-122">-Name</span></span>
<span data-ttu-id="5ceee-123">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="5ceee-123">Specifies a name.</span></span>
<span data-ttu-id="5ceee-124">Ha nincs megadva név, a parancsmag felsorolja az összes várólistát.</span><span class="sxs-lookup"><span data-stu-id="5ceee-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="5ceee-125">Ha meg van adva egy teljes vagy részleges név, a parancsmag minden olyan várólistát kap, amely megfelel a név mintának.</span><span class="sxs-lookup"><span data-stu-id="5ceee-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ceee-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5ceee-126">-Prefix</span></span>
<span data-ttu-id="5ceee-127">A bekapni kívánt várólisták nevében használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ceee-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ceee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ceee-128">CommonParameters</span></span>
<span data-ttu-id="5ceee-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ceee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ceee-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ceee-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ceee-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ceee-131">INPUTS</span></span>

### <span data-ttu-id="5ceee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5ceee-132">System.String</span></span>

### <span data-ttu-id="5ceee-133">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ceee-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5ceee-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ceee-134">OUTPUTS</span></span>

### <span data-ttu-id="5ceee-135">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5ceee-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="5ceee-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ceee-136">NOTES</span></span>

## <span data-ttu-id="5ceee-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ceee-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ceee-138">Új – AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5ceee-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="5ceee-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5ceee-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


