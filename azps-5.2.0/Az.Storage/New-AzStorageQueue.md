---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324726"
---
# <span data-ttu-id="a4339-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4339-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="a4339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4339-102">SYNOPSIS</span></span>
<span data-ttu-id="a4339-103">Tárterület-várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4339-103">Creates a storage queue.</span></span>

## <span data-ttu-id="a4339-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4339-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4339-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4339-105">DESCRIPTION</span></span>
<span data-ttu-id="a4339-106">A **New-AzStorageQueue** parancsmag létrehoz egy tár várólistát az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="a4339-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="a4339-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4339-107">EXAMPLES</span></span>

### <span data-ttu-id="a4339-108">1. példa: Azure-tárterület várólistájának létrehozása</span><span class="sxs-lookup"><span data-stu-id="a4339-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="a4339-109">Ez a példa létrehoz egy queueabc nevű tárterület-várólistát.</span><span class="sxs-lookup"><span data-stu-id="a4339-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="a4339-110">2. példa: Több Azure storage queues létrehozása</span><span class="sxs-lookup"><span data-stu-id="a4339-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="a4339-111">Ez a példa több tárterület-várólistát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4339-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="a4339-112">A .NET-karakterláncosztály Felosztás metódusát használja, majd átadja a neveket a folyamatnak.</span><span class="sxs-lookup"><span data-stu-id="a4339-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a4339-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4339-113">PARAMETERS</span></span>

### <span data-ttu-id="a4339-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a4339-114">-Context</span></span>
<span data-ttu-id="a4339-115">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a4339-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a4339-116">A parancsmagot a New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="a4339-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a4339-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4339-117">-DefaultProfile</span></span>
<span data-ttu-id="a4339-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4339-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4339-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a4339-119">-Name</span></span>
<span data-ttu-id="a4339-120">Megadja a várólistának a nevét.</span><span class="sxs-lookup"><span data-stu-id="a4339-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="a4339-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4339-121">CommonParameters</span></span>
<span data-ttu-id="a4339-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4339-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4339-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4339-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4339-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4339-124">INPUTS</span></span>

### <span data-ttu-id="a4339-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a4339-125">System.String</span></span>

### <span data-ttu-id="a4339-126">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a4339-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a4339-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4339-127">OUTPUTS</span></span>

### <span data-ttu-id="a4339-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4339-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="a4339-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4339-129">NOTES</span></span>

## <span data-ttu-id="a4339-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4339-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4339-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4339-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="a4339-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a4339-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


