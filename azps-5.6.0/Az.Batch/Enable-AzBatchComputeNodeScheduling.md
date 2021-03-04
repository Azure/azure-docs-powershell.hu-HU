---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941289"
---
# <span data-ttu-id="ab6d9-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="ab6d9-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="ab6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6d9-103">Engedélyezi a tevékenységek ütemezését a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="ab6d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab6d9-104">SYNTAX</span></span>

### <span data-ttu-id="ab6d9-105">Id (Default)</span><span class="sxs-lookup"><span data-stu-id="ab6d9-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6d9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ab6d9-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab6d9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab6d9-107">DESCRIPTION</span></span>
<span data-ttu-id="ab6d9-108">Az **Enable-AzBatchComputeNodeScheduling parancsmag** lehetővé teszi a feladat ütemezését a megadott számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="ab6d9-109">A számítási csomópont egy adott alkalmazásterheléshez dedikált Azure virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="ab6d9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab6d9-110">EXAMPLES</span></span>

### <span data-ttu-id="ab6d9-111">1. példa: Feladatütemezés engedélyezése számítási csomóponton</span><span class="sxs-lookup"><span data-stu-id="ab6d9-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="ab6d9-112">Ezek a parancsok lehetővé teszik a feladatok ütemezését a számítási csomópont tvm-1783593343_34-20151117t22514z.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="ab6d9-113">Ehhez a példában az első parancs létrehoz egy objektumhivatkozást, amely tartalmazza a contosobatchaccount kötegfiók fiókkulcsait.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="ab6d9-114">Ezt az objektumhivatkozást egy $context.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="ab6d9-115">A második parancs ezután ezt az objektumhivatkozást és az **Enable-AzBatchComputeNodeScheduling parancsmagot** használva csatlakozik a sajátPool készlethez, és engedélyezi a feladatok ütemezését a tvm-1783593343_34-20151117t22514z.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="ab6d9-116">2. példa: Tevékenységütemezés engedélyezése egy készlet számítási csomópontjain</span><span class="sxs-lookup"><span data-stu-id="ab6d9-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="ab6d9-117">Ezek a parancsok lehetővé teszik a tevékenység ütemezését a készlet Pool06-ban található összes számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="ab6d9-118">A feladat végrehajtásához a példában az első parancs létrehoz egy objektumhivatkozást, amely tartalmazza a contosobatchaccount kötegfiók fiókkulcsait.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="ab6d9-119">Ezt az objektumhivatkozást egy $context.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="ab6d9-120">A példában a második parancs ezt az objektumhivatkozást és **a Get-AzBatchComputeNode-ot** használva visszaadja a Pool06-ban található összes számítási csomópont gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="ab6d9-121">Ez a gyűjtemény ezután az **Enable-AzBatchComputeNodeScheduling** parancsmagba lesz becsatolt, amely lehetővé teszi a feladat ütemezését a gyűjtemény minden egyes számítási csomópontján.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="ab6d9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab6d9-122">PARAMETERS</span></span>

### <span data-ttu-id="ab6d9-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab6d9-123">-BatchContext</span></span>
<span data-ttu-id="ab6d9-124">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ab6d9-125">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ab6d9-126">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ab6d9-127">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ab6d9-128">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab6d9-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ab6d9-129">-ComputeNode</span></span>
<span data-ttu-id="ab6d9-130">Objektumhivatkozást ad meg arra a számítási csomópontra, ahol engedélyezve van a tevékenységütemezés.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="ab6d9-131">Ez az objektumhivatkozás a Get-AzBatchComputeNode segítségével jön létre, és a visszaadott számítási csomópont-objektumot egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="ab6d9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6d9-132">-DefaultProfile</span></span>
<span data-ttu-id="ab6d9-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab6d9-134">-Id</span><span class="sxs-lookup"><span data-stu-id="ab6d9-134">-Id</span></span>
<span data-ttu-id="ab6d9-135">Annak a számítási csomópontnak az azonosítója, ahol engedélyezve van a feladatütemezés.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="ab6d9-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ab6d9-136">-PoolId</span></span>
<span data-ttu-id="ab6d9-137">Annak a kötegkészletnek az azonosítója, amely azt a számítási csomópontot tartalmazza, ahol a tevékenységütemezés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="ab6d9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6d9-138">CommonParameters</span></span>
<span data-ttu-id="ab6d9-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6d9-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab6d9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6d9-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab6d9-141">INPUTS</span></span>

### <span data-ttu-id="ab6d9-142">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ab6d9-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ab6d9-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab6d9-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ab6d9-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab6d9-144">OUTPUTS</span></span>

### <span data-ttu-id="ab6d9-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="ab6d9-145">System.Void</span></span>

## <span data-ttu-id="ab6d9-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab6d9-146">NOTES</span></span>

## <span data-ttu-id="ab6d9-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab6d9-147">RELATED LINKS</span></span>

[<span data-ttu-id="ab6d9-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="ab6d9-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


