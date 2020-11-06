---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: e00a1a923afdd8a851416e872028a30ce1e04a55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498448"
---
# <span data-ttu-id="c566c-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="c566c-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="c566c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c566c-102">SYNOPSIS</span></span>
<span data-ttu-id="c566c-103">A megadott számítási csomóponton engedélyezi a tevékenységek ütemezését.</span><span class="sxs-lookup"><span data-stu-id="c566c-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c566c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c566c-104">SYNTAX</span></span>

### <span data-ttu-id="c566c-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c566c-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c566c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c566c-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c566c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c566c-107">DESCRIPTION</span></span>
<span data-ttu-id="c566c-108">Az **enable-AzureBatchComputeNodeScheduling** parancsmag a megadott számítási csomóponton engedélyezte a tevékenységek ütemezését.</span><span class="sxs-lookup"><span data-stu-id="c566c-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="c566c-109">A számítási csomópont egy olyan Azure Virtual Machine, amely egy adott alkalmazási munkaterheléshez van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="c566c-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="c566c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c566c-110">EXAMPLES</span></span>

### <span data-ttu-id="c566c-111">1. példa: tevékenység ütemezése engedélyezése számítási csomóponton</span><span class="sxs-lookup"><span data-stu-id="c566c-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="c566c-112">Ezekkel a parancsokkal a TVM-1783593343_34-20151117t222514z számíthatja ki a tevékenység ütemezését.</span><span class="sxs-lookup"><span data-stu-id="c566c-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="c566c-113">Ehhez a példa első parancsa létrehoz egy objektumot, amely tartalmazza a kötegelt fiók contosobatchaccount tartozó kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="c566c-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="c566c-114">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="c566c-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="c566c-115">A második parancs ekkor az Object Reference ( **enable-AzureBatchComputeNodeScheduling** parancsmag) segítségével csatlakozik a Pool myPool, és engedélyezheti a TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="c566c-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="c566c-116">2. példa: tevékenység ütemezése engedélyezése a kiszámított csomópontokon a készletben</span><span class="sxs-lookup"><span data-stu-id="c566c-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="c566c-117">Ezekkel a parancsokkal engedélyezheti a tevékenységek ütemezését a Pool Pool06 található összes számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="c566c-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="c566c-118">A feladat végrehajtásához a példa első parancsa létrehoz egy objektumot, amely tartalmazza a kötegelt fiók contosobatchaccount tartozó kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="c566c-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="c566c-119">Ez az objektum hivatkozás a $context nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="c566c-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="c566c-120">A példában szereplő második parancs az objektum-hivatkozással és a **Get-AzureBatchComputeNode** a Pool06 található összes számítási csomópont gyűjteményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c566c-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="c566c-121">Ezt követően a program átirányítja a gyűjteményt az **enable-AzureBatchComputeNodeScheduling** parancsmagra, amely lehetővé teszi a tevékenység ütemezését a gyűjtemény egyes számítási csomópontjain.</span><span class="sxs-lookup"><span data-stu-id="c566c-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="c566c-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c566c-122">PARAMETERS</span></span>

### <span data-ttu-id="c566c-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c566c-123">-BatchContext</span></span>
<span data-ttu-id="c566c-124">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="c566c-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c566c-125">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="c566c-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c566c-126">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="c566c-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c566c-127">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="c566c-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c566c-128">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="c566c-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c566c-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c566c-129">-ComputeNode</span></span>
<span data-ttu-id="c566c-130">A számítási csomópontra mutató objektum hivatkozását adja meg, ahol a tevékenység ütemezése engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="c566c-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="c566c-131">Ez az objektum hivatkozás az Get-AzureBatchComputeNode parancsmag használatával jön létre, és a visszaadott számítási csomópont objektumát egy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c566c-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="c566c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c566c-132">-DefaultProfile</span></span>
<span data-ttu-id="c566c-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c566c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c566c-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c566c-134">-Id</span></span>
<span data-ttu-id="c566c-135">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, ahol a tevékenység ütemezése engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="c566c-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="c566c-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c566c-136">-PoolId</span></span>
<span data-ttu-id="c566c-137">Annak a kötegelt készletnek az AZONOSÍTÓját adja meg, amely a tevékenység ütemezésekor engedélyezett számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c566c-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="c566c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c566c-138">CommonParameters</span></span>
<span data-ttu-id="c566c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c566c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c566c-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c566c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c566c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c566c-141">INPUTS</span></span>

### <span data-ttu-id="c566c-142">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c566c-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="c566c-143">Paraméterek: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c566c-143">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="c566c-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c566c-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c566c-145">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c566c-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c566c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c566c-146">OUTPUTS</span></span>

### <span data-ttu-id="c566c-147">System. Void</span><span class="sxs-lookup"><span data-stu-id="c566c-147">System.Void</span></span>

## <span data-ttu-id="c566c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c566c-148">NOTES</span></span>

## <span data-ttu-id="c566c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c566c-149">RELATED LINKS</span></span>

[<span data-ttu-id="c566c-150">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="c566c-150">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


