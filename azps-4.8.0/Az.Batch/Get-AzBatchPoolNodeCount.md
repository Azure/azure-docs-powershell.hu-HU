---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182616"
---
# <span data-ttu-id="07d74-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="07d74-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="07d74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07d74-102">SYNOPSIS</span></span>
<span data-ttu-id="07d74-103">A köteg-csomópontok száma egy csomópontos államban, a Pool ID szerint csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="07d74-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="07d74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07d74-104">SYNTAX</span></span>

### <span data-ttu-id="07d74-105">AzureBatchPoolNodeCounts (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07d74-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07d74-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="07d74-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d74-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="07d74-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d74-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="07d74-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d74-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="07d74-109">DESCRIPTION</span></span>
<span data-ttu-id="07d74-110">Az Get-AzBatchPoolNodeCount parancsmag lehetővé teszi, hogy az ügyfelek a csomópontokat a csomópontok szerint csoportosítva, a csomópontok száma szerint csoportosítsák.</span><span class="sxs-lookup"><span data-stu-id="07d74-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="07d74-111">A lehetséges csomópont-Államok létrehozása, üresjárata, leavingPool, offline, preempted, újraindítás, újraképkezelés, futás, indítás, startTaskFailed, ismeretlen, használhatatlan és waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="07d74-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="07d74-112">A parancsmag a PoolId vagy a Pool paraméterrel csak a megadott készlet-azonosítóval rendelkező készletet szűri.</span><span class="sxs-lookup"><span data-stu-id="07d74-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="07d74-113">Példák</span><span class="sxs-lookup"><span data-stu-id="07d74-113">EXAMPLES</span></span>

### <span data-ttu-id="07d74-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07d74-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="07d74-115">A lista csomópont az aktuális kötegelt fiók környezetében a medencék esetén a csomópontok állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="07d74-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="07d74-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="07d74-116">Example 2</span></span>

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

<span data-ttu-id="07d74-117">A csomópontok megjelenítése: a csomópontok száma a Pool-azonosítók esetében.</span><span class="sxs-lookup"><span data-stu-id="07d74-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="07d74-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07d74-118">PARAMETERS</span></span>

### <span data-ttu-id="07d74-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="07d74-119">-BatchContext</span></span>
<span data-ttu-id="07d74-120">A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.</span><span class="sxs-lookup"><span data-stu-id="07d74-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="07d74-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="07d74-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="07d74-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="07d74-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="07d74-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="07d74-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="07d74-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="07d74-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="07d74-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d74-125">-DefaultProfile</span></span>
<span data-ttu-id="07d74-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07d74-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07d74-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="07d74-127">-MaxCount</span></span>
<span data-ttu-id="07d74-128">A visszaadható készletek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07d74-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="07d74-129">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="07d74-129">The default value is 10.</span></span>

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

### <span data-ttu-id="07d74-130">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="07d74-130">-Pool</span></span>
<span data-ttu-id="07d74-131">Annak a **PSCloudPool** a megadása, amelyhez csomópontot szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="07d74-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="07d74-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="07d74-132">-PoolId</span></span>
<span data-ttu-id="07d74-133">Annak a készletnek az azonosítója, amelyhez csomópontot szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="07d74-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="07d74-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d74-134">CommonParameters</span></span>
<span data-ttu-id="07d74-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07d74-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d74-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07d74-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d74-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07d74-137">INPUTS</span></span>

### <span data-ttu-id="07d74-138">System. String</span><span class="sxs-lookup"><span data-stu-id="07d74-138">System.String</span></span>

### <span data-ttu-id="07d74-139">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="07d74-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="07d74-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="07d74-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="07d74-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07d74-141">OUTPUTS</span></span>

### <span data-ttu-id="07d74-142">Microsoft.Azure.Commands.BatCH. Modellek. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="07d74-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="07d74-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07d74-143">NOTES</span></span>

## <span data-ttu-id="07d74-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07d74-144">RELATED LINKS</span></span>

[<span data-ttu-id="07d74-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="07d74-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="07d74-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="07d74-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="07d74-147">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="07d74-147">Azure Batch Cmdlets</span></span>]()

