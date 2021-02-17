---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205262"
---
# <span data-ttu-id="3e15b-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="3e15b-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="3e15b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e15b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e15b-103">A Köteg csomópontok száma csomópontonként, készletazonosító szerint csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="3e15b-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="3e15b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e15b-104">SYNTAX</span></span>

### <span data-ttu-id="3e15b-105">AzureBatchPoolNodeCounts (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e15b-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e15b-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="3e15b-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e15b-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="3e15b-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e15b-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="3e15b-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e15b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e15b-109">DESCRIPTION</span></span>
<span data-ttu-id="3e15b-110">A Get-AzBatchPoolNodeCount parancsmag lehetővé teszi az ügyfeleknek, hogy készlet szerint csoportosítva visszaszámolják a csomópontok számát csomópontonként.</span><span class="sxs-lookup"><span data-stu-id="3e15b-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="3e15b-111">A csomópontok lehetséges állapotok létrehozása, üresjárata, aPool elhagyása, offline, előre elindított, újraindítás, újraképezés, futás, indítás, indítás, ismeretlen, használhatatlan és aStartTask várakozása.</span><span class="sxs-lookup"><span data-stu-id="3e15b-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="3e15b-112">A parancsmag a PoolId vagy a Pool paramétert használva csak a készlet megadott készletazonosítóját szűri.</span><span class="sxs-lookup"><span data-stu-id="3e15b-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="3e15b-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e15b-113">EXAMPLES</span></span>

### <span data-ttu-id="3e15b-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="3e15b-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="3e15b-115">Az aktuális kötegfiók környezetében lévő készletek csomópontonkénti száma.</span><span class="sxs-lookup"><span data-stu-id="3e15b-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="3e15b-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="3e15b-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="3e15b-117">Csomópontok száma csomópontonként egy adott készletazonosítóhoz</span><span class="sxs-lookup"><span data-stu-id="3e15b-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="3e15b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e15b-118">PARAMETERS</span></span>

### <span data-ttu-id="3e15b-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3e15b-119">-BatchContext</span></span>
<span data-ttu-id="3e15b-120">A BatchAccountContext példány, amely a Batch szolgáltatás használata során használható.</span><span class="sxs-lookup"><span data-stu-id="3e15b-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="3e15b-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="3e15b-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="3e15b-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="3e15b-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="3e15b-123">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="3e15b-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="3e15b-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="3e15b-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3e15b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e15b-125">-DefaultProfile</span></span>
<span data-ttu-id="3e15b-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e15b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e15b-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3e15b-127">-MaxCount</span></span>
<span data-ttu-id="3e15b-128">Azt adja meg, hogy legfeljebb hány készletet kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="3e15b-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="3e15b-129">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="3e15b-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e15b-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="3e15b-130">-Pool</span></span>
<span data-ttu-id="3e15b-131">Azt a **PSCloudPoolt adja** meg, amelynek a csomópontszámát meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="3e15b-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e15b-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3e15b-132">-PoolId</span></span>
<span data-ttu-id="3e15b-133">Annak a készletnek az azonosítója, amelynek a csomópontszámát le kell számítani.</span><span class="sxs-lookup"><span data-stu-id="3e15b-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e15b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e15b-134">CommonParameters</span></span>
<span data-ttu-id="3e15b-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e15b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e15b-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e15b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e15b-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e15b-137">INPUTS</span></span>

### <span data-ttu-id="3e15b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3e15b-138">System.String</span></span>

### <span data-ttu-id="3e15b-139">Microsoft.Azure.Commands.Bat. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="3e15b-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="3e15b-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e15b-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3e15b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e15b-141">OUTPUTS</span></span>

### <span data-ttu-id="3e15b-142">Microsoft.Azure.Commands.Bat. Models.PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="3e15b-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="3e15b-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e15b-143">NOTES</span></span>

## <span data-ttu-id="3e15b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e15b-144">RELATED LINKS</span></span>

[<span data-ttu-id="3e15b-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e15b-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="3e15b-146">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="3e15b-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="3e15b-147">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3e15b-147">Azure Batch Cmdlets</span></span>]()

