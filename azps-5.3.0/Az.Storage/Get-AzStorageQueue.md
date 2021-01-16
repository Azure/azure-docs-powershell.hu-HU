---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479462"
---
# <span data-ttu-id="a868d-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a868d-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="a868d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a868d-102">SYNOPSIS</span></span>
<span data-ttu-id="a868d-103">A tárterület-várólisták listája.</span><span class="sxs-lookup"><span data-stu-id="a868d-103">Lists storage queues.</span></span>

## <span data-ttu-id="a868d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a868d-104">SYNTAX</span></span>

### <span data-ttu-id="a868d-105">QueueName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a868d-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a868d-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="a868d-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a868d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a868d-107">DESCRIPTION</span></span>
<span data-ttu-id="a868d-108">A **Get-AzStorageQueue** parancsmag felsorolja az Azure Storage-fiókhoz társított társorokat.</span><span class="sxs-lookup"><span data-stu-id="a868d-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="a868d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a868d-109">EXAMPLES</span></span>

### <span data-ttu-id="a868d-110">1. példa: Az összes Azure Storage-várólisták felsorolása</span><span class="sxs-lookup"><span data-stu-id="a868d-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="a868d-111">Ez a parancs az aktuális tárfiók összes tár várólistájának listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a868d-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="a868d-112">2. példa: Azure Storage-várólisták felsorolása helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="a868d-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="a868d-113">Ez a parancs egy helyettesítő karaktert használva lekérte a várólistával kezdődik nevű tárolósorok listáját.</span><span class="sxs-lookup"><span data-stu-id="a868d-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="a868d-114">3. példa: Azure Storage-várólisták felsorolása a várólistán lévő név előtaggal</span><span class="sxs-lookup"><span data-stu-id="a868d-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="a868d-115">Ebben a példában az *Előtag* paramétert használva megjelenik a várólistával kezdődik nevű tárterület-várólisták listája.</span><span class="sxs-lookup"><span data-stu-id="a868d-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="a868d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a868d-116">PARAMETERS</span></span>

### <span data-ttu-id="a868d-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a868d-117">-Context</span></span>
<span data-ttu-id="a868d-118">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a868d-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a868d-119">A **New-AzStorageContext** parancsmag használatával hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="a868d-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="a868d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a868d-120">-DefaultProfile</span></span>
<span data-ttu-id="a868d-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a868d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a868d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a868d-122">-Name</span></span>
<span data-ttu-id="a868d-123">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="a868d-123">Specifies a name.</span></span>
<span data-ttu-id="a868d-124">Ha nincs megadva név, a parancsmag az összes várólistát felsorolja.</span><span class="sxs-lookup"><span data-stu-id="a868d-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="a868d-125">Ha teljes vagy részleges nevet ad meg, a parancsmag az összes olyan várólistát megkapja, amely megfelel a névmintának.</span><span class="sxs-lookup"><span data-stu-id="a868d-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="a868d-126">-Előtag</span><span class="sxs-lookup"><span data-stu-id="a868d-126">-Prefix</span></span>
<span data-ttu-id="a868d-127">Megadja a lekért várólisták nevében használt előtagot.</span><span class="sxs-lookup"><span data-stu-id="a868d-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="a868d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a868d-128">CommonParameters</span></span>
<span data-ttu-id="a868d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a868d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a868d-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a868d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a868d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a868d-131">INPUTS</span></span>

### <span data-ttu-id="a868d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a868d-132">System.String</span></span>

### <span data-ttu-id="a868d-133">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a868d-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a868d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a868d-134">OUTPUTS</span></span>

### <span data-ttu-id="a868d-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a868d-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="a868d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a868d-136">NOTES</span></span>

## <span data-ttu-id="a868d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a868d-137">RELATED LINKS</span></span>

[<span data-ttu-id="a868d-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a868d-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="a868d-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a868d-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


