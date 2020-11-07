---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolnodecounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
ms.openlocfilehash: 6cd15b6a8ee59982bf328f751a20807835f54513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673180"
---
# <span data-ttu-id="84017-101">Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="84017-101">Get-AzureBatchPoolNodeCounts</span></span>

## <span data-ttu-id="84017-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84017-102">SYNOPSIS</span></span>
<span data-ttu-id="84017-103">A köteg-csomópontok száma egy csomópontos államban, a Pool ID szerint csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="84017-103">Gets Batch node counts per node state grouped by pool id.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84017-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84017-104">SYNTAX</span></span>

### <span data-ttu-id="84017-105">AzureBatchPoolNodeCounts (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84017-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzureBatchPoolNodeCounts -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84017-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="84017-106">PoolId</span></span>
```
Get-AzureBatchPoolNodeCounts [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84017-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="84017-107">ParentObject</span></span>
```
Get-AzureBatchPoolNodeCounts [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84017-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="84017-108">ODataFilter</span></span>
```
Get-AzureBatchPoolNodeCounts [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84017-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="84017-109">DESCRIPTION</span></span>
<span data-ttu-id="84017-110">Az Get-AzureBatchPoolNodeCounts parancsmag lehetővé teszi, hogy az ügyfelek a csomópontokat a csomópontok szerint csoportosítva, a csomópontok száma szerint csoportosítsák.</span><span class="sxs-lookup"><span data-stu-id="84017-110">The Get-AzureBatchPoolNodeCounts cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="84017-111">A lehetséges csomópont-Államok létrehozása, üresjárata, leavingPool, offline, preempted, újraindítás, újraképkezelés, futás, indítás, startTaskFailed, ismeretlen, használhatatlan és waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="84017-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="84017-112">A parancsmag a PoolId vagy a Pool paraméterrel csak a megadott készlet-azonosítóval rendelkező készletet szűri.</span><span class="sxs-lookup"><span data-stu-id="84017-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="84017-113">Példák</span><span class="sxs-lookup"><span data-stu-id="84017-113">EXAMPLES</span></span>

### <span data-ttu-id="84017-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="84017-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="84017-115">A lista csomópont az aktuális kötegelt fiók környezetében a medencék esetén a csomópontok állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="84017-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="84017-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="84017-116">Example 2</span></span>

```powershell
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"
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

PS C:\> Get-AzureBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="84017-117">A csomópontok megjelenítése: a csomópontok száma a Pool-azonosítók esetében.</span><span class="sxs-lookup"><span data-stu-id="84017-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="84017-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84017-118">PARAMETERS</span></span>

### <span data-ttu-id="84017-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84017-119">-BatchContext</span></span>
<span data-ttu-id="84017-120">A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.</span><span class="sxs-lookup"><span data-stu-id="84017-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="84017-121">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="84017-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="84017-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="84017-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="84017-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="84017-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="84017-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="84017-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="84017-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84017-125">-DefaultProfile</span></span>
<span data-ttu-id="84017-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84017-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84017-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="84017-127">-MaxCount</span></span>
<span data-ttu-id="84017-128">A visszaadható készletek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84017-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="84017-129">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="84017-129">The default value is 10.</span></span>

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

### <span data-ttu-id="84017-130">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="84017-130">-Pool</span></span>
<span data-ttu-id="84017-131">Annak a **PSCloudPool** a megadása, amelyhez csomópontot szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="84017-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="84017-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="84017-132">-PoolId</span></span>
<span data-ttu-id="84017-133">Annak a készletnek az azonosítója, amelyhez csomópontot szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="84017-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="84017-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84017-134">CommonParameters</span></span>
<span data-ttu-id="84017-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84017-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84017-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84017-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84017-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84017-137">INPUTS</span></span>

### <span data-ttu-id="84017-138">System. String</span><span class="sxs-lookup"><span data-stu-id="84017-138">System.String</span></span>

### <span data-ttu-id="84017-139">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="84017-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="84017-140">Paraméterek: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84017-140">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="84017-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84017-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="84017-142">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84017-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="84017-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84017-143">OUTPUTS</span></span>

### <span data-ttu-id="84017-144">Microsoft.Azure.Commands.BatCH. Modellek. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="84017-144">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="84017-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84017-145">NOTES</span></span>

## <span data-ttu-id="84017-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84017-146">RELATED LINKS</span></span>

[<span data-ttu-id="84017-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="84017-147">Get-AzureRmBatchAccountKeys</span></span>]()

[<span data-ttu-id="84017-148">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="84017-148">Get-AzureBatchJob</span></span>]()

[<span data-ttu-id="84017-149">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="84017-149">Azure Batch Cmdlets</span></span>]()

