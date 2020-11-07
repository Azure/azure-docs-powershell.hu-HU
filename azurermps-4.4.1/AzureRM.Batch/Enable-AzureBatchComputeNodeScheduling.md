---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 6c890836d8ca22e617fdc88788a6809cbce8581c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679798"
---
# <span data-ttu-id="1ce47-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="1ce47-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="1ce47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ce47-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce47-103">A megadott számítási csomóponton engedélyezi a tevékenységek ütemezését.</span><span class="sxs-lookup"><span data-stu-id="1ce47-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ce47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ce47-104">SYNTAX</span></span>

### <span data-ttu-id="1ce47-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ce47-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ce47-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1ce47-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ce47-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ce47-107">DESCRIPTION</span></span>
<span data-ttu-id="1ce47-108">Az **enable-AzureBatchComputeNodeScheduling** parancsmag a megadott számítási csomóponton engedélyezte a tevékenységek ütemezését.</span><span class="sxs-lookup"><span data-stu-id="1ce47-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="1ce47-109">A számítási csomópont egy olyan Azure Virtual Machine, amely egy adott alkalmazási munkaterheléshez van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="1ce47-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="1ce47-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ce47-110">EXAMPLES</span></span>

### <span data-ttu-id="1ce47-111">1. példa: tevékenység ütemezése engedélyezése számítási csomóponton</span><span class="sxs-lookup"><span data-stu-id="1ce47-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="1ce47-112">Ezekkel a parancsokkal a TVM-1783593343_34-20151117t222514z számíthatja ki a tevékenység ütemezését.</span><span class="sxs-lookup"><span data-stu-id="1ce47-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="1ce47-113">Ehhez a példa első parancsa létrehoz egy objektumot, amely tartalmazza a kötegelt fiók contosobatchaccount tartozó kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="1ce47-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="1ce47-114">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="1ce47-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="1ce47-115">A második parancs ekkor az Object Reference ( **enable-AzureBatchComputeNodeScheduling** parancsmag) segítségével csatlakozik a Pool myPool, és engedélyezheti a TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="1ce47-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="1ce47-116">2. példa: tevékenység ütemezése engedélyezése a kiszámított csomópontokon a készletben</span><span class="sxs-lookup"><span data-stu-id="1ce47-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="1ce47-117">Ezekkel a parancsokkal engedélyezheti a tevékenységek ütemezését a Pool Pool06 található összes számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="1ce47-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="1ce47-118">A feladat végrehajtásához a példa első parancsa létrehoz egy objektumot, amely tartalmazza a kötegelt fiók contosobatchaccount tartozó kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="1ce47-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="1ce47-119">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="1ce47-119">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="1ce47-120">A példában szereplő második parancs az objektum-hivatkozással és a **Get-AzureBatchComputeNode** a Pool06 található összes számítási csomópont gyűjteményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1ce47-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="1ce47-121">Ezt követően a program átirányítja a gyűjteményt az **enable-AzureBatchComputeNodeScheduling** parancsmagra, amely lehetővé teszi a tevékenység ütemezését a gyűjtemény egyes számítási csomópontjain.</span><span class="sxs-lookup"><span data-stu-id="1ce47-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="1ce47-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ce47-122">PARAMETERS</span></span>

### <span data-ttu-id="1ce47-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1ce47-123">-BatchContext</span></span>
<span data-ttu-id="1ce47-124">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="1ce47-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1ce47-125">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ce47-125">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce47-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="1ce47-126">-ComputeNode</span></span>
<span data-ttu-id="1ce47-127">A számítási csomópontra mutató objektum hivatkozását adja meg, ahol a tevékenység ütemezése engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="1ce47-127">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="1ce47-128">Ez az objektum hivatkozás az Get-AzureBatchComputeNode parancsmag használatával jön létre, és a visszaadott számítási csomópont objektumát egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ce47-128">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce47-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="1ce47-129">-Id</span></span>
<span data-ttu-id="1ce47-130">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, ahol a tevékenység ütemezése engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="1ce47-130">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce47-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1ce47-131">-PoolId</span></span>
<span data-ttu-id="1ce47-132">Annak a kötegelt készletnek az AZONOSÍTÓját adja meg, amely a tevékenység ütemezésekor engedélyezett számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1ce47-132">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce47-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce47-133">-DefaultProfile</span></span>
<span data-ttu-id="1ce47-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ce47-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce47-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce47-135">CommonParameters</span></span>
<span data-ttu-id="1ce47-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ce47-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce47-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce47-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce47-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ce47-138">INPUTS</span></span>

### <span data-ttu-id="1ce47-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1ce47-139">BatchAccountContext</span></span>
<span data-ttu-id="1ce47-140">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ce47-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="1ce47-141">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="1ce47-141">PSComputeNode</span></span>
<span data-ttu-id="1ce47-142">A ' ComputeNode ' paraméter az "PSComputeNode" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ce47-142">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="1ce47-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ce47-143">OUTPUTS</span></span>

## <span data-ttu-id="1ce47-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ce47-144">NOTES</span></span>

## <span data-ttu-id="1ce47-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ce47-145">RELATED LINKS</span></span>

[<span data-ttu-id="1ce47-146">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="1ce47-146">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


