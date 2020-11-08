---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024208"
---
# <span data-ttu-id="51175-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="51175-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="51175-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51175-102">SYNOPSIS</span></span>
<span data-ttu-id="51175-103">A megadott számítási csomóponton engedélyezi a tevékenységek ütemezését.</span><span class="sxs-lookup"><span data-stu-id="51175-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="51175-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51175-104">SYNTAX</span></span>

### <span data-ttu-id="51175-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51175-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51175-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="51175-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51175-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="51175-107">DESCRIPTION</span></span>
<span data-ttu-id="51175-108">Az **enable-AzBatchComputeNodeScheduling** parancsmag a megadott számítási csomóponton engedélyezte a tevékenységek ütemezését.</span><span class="sxs-lookup"><span data-stu-id="51175-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="51175-109">A számítási csomópont egy olyan Azure Virtual Machine, amely egy adott alkalmazási munkaterheléshez van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="51175-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="51175-110">Példák</span><span class="sxs-lookup"><span data-stu-id="51175-110">EXAMPLES</span></span>

### <span data-ttu-id="51175-111">1. példa: tevékenység ütemezése engedélyezése számítási csomóponton</span><span class="sxs-lookup"><span data-stu-id="51175-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="51175-112">Ezekkel a parancsokkal a TVM-1783593343_34-20151117t222514z számíthatja ki a tevékenység ütemezését.</span><span class="sxs-lookup"><span data-stu-id="51175-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="51175-113">Ehhez a példa első parancsa létrehoz egy objektumot, amely tartalmazza a kötegelt fiók contosobatchaccount tartozó kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="51175-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="51175-114">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="51175-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="51175-115">A második parancs ekkor az Object Reference ( **enable-AzBatchComputeNodeScheduling** parancsmag) segítségével csatlakozik a Pool myPool, és engedélyezheti a TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="51175-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="51175-116">2. példa: tevékenység ütemezése engedélyezése a kiszámított csomópontokon a készletben</span><span class="sxs-lookup"><span data-stu-id="51175-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="51175-117">Ezekkel a parancsokkal engedélyezheti a tevékenységek ütemezését a Pool Pool06 található összes számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="51175-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="51175-118">A feladat végrehajtásához a példa első parancsa létrehoz egy objektumot, amely tartalmazza a kötegelt fiók contosobatchaccount tartozó kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="51175-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="51175-119">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="51175-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="51175-120">A példában szereplő második parancs az objektum-hivatkozással és a **Get-AzBatchComputeNode** a Pool06 található összes számítási csomópont gyűjteményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="51175-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="51175-121">Ezt követően a program átirányítja a gyűjteményt az **enable-AzBatchComputeNodeScheduling** parancsmagra, amely lehetővé teszi a tevékenység ütemezését a gyűjtemény egyes számítási csomópontjain.</span><span class="sxs-lookup"><span data-stu-id="51175-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="51175-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51175-122">PARAMETERS</span></span>

### <span data-ttu-id="51175-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="51175-123">-BatchContext</span></span>
<span data-ttu-id="51175-124">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="51175-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="51175-125">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="51175-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="51175-126">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="51175-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="51175-127">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="51175-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="51175-128">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="51175-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="51175-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="51175-129">-ComputeNode</span></span>
<span data-ttu-id="51175-130">A számítási csomópontra mutató objektum hivatkozását adja meg, ahol a tevékenység ütemezése engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="51175-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="51175-131">Ez az objektum hivatkozás az Get-AzBatchComputeNode parancsmag használatával jön létre, és a visszaadott számítási csomópont objektumát egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="51175-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="51175-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51175-132">-DefaultProfile</span></span>
<span data-ttu-id="51175-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51175-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51175-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="51175-134">-Id</span></span>
<span data-ttu-id="51175-135">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, ahol a tevékenység ütemezése engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="51175-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="51175-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="51175-136">-PoolId</span></span>
<span data-ttu-id="51175-137">Annak a kötegelt készletnek az AZONOSÍTÓját adja meg, amely a tevékenység ütemezésekor engedélyezett számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="51175-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="51175-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51175-138">CommonParameters</span></span>
<span data-ttu-id="51175-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51175-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51175-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51175-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51175-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51175-141">INPUTS</span></span>

### <span data-ttu-id="51175-142">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="51175-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="51175-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="51175-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="51175-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51175-144">OUTPUTS</span></span>

### <span data-ttu-id="51175-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="51175-145">System.Void</span></span>

## <span data-ttu-id="51175-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51175-146">NOTES</span></span>

## <span data-ttu-id="51175-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51175-147">RELATED LINKS</span></span>

[<span data-ttu-id="51175-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="51175-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


