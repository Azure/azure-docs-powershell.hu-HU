---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 403bcc5a85001b6d98c67f91d995eb05bc948752
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180621"
---
# <span data-ttu-id="068e9-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="068e9-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="068e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="068e9-102">SYNOPSIS</span></span>
<span data-ttu-id="068e9-103">A csomópont-szolgáltatási naplófájlok feltöltése Azure-tárolóba.</span><span class="sxs-lookup"><span data-stu-id="068e9-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="068e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="068e9-104">SYNTAX</span></span>

### <span data-ttu-id="068e9-105">AzureBatchComputeNodeServiceLogUpload (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="068e9-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="068e9-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="068e9-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068e9-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="068e9-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="068e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="068e9-108">DESCRIPTION</span></span>
<span data-ttu-id="068e9-109">Ez a parancsmag az Azure batch Service log-fájljait a kiszámított csomópontokból gyűjti össze, ha hibát tapasztal, és az Azure ügyfélszolgálatát szeretné kibővíteni.</span><span class="sxs-lookup"><span data-stu-id="068e9-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="068e9-110">Az Azure-köteg-szolgáltatási naplófájlokat az Azure ügyfélszolgálatával kell megosztania, hogy segítséget nyújt a kötegelt szolgáltatással kapcsolatos hibák elhárításához.</span><span class="sxs-lookup"><span data-stu-id="068e9-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="068e9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="068e9-111">EXAMPLES</span></span>

### <span data-ttu-id="068e9-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="068e9-112">Example 1</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="068e9-113">A számítási csomópontot az 2018-es verzióban, illetve január 1-jén, az-es éjfél után, a számítási csomóponttól kapott készlet azonosítójának feltöltése után, illetve a csomópont-azonosító kiszámításához adja meg.</span><span class="sxs-lookup"><span data-stu-id="068e9-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="068e9-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="068e9-114">Example 2</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="068e9-115">Töltse fel a számítási csomópontot (a számítási csomópontot) a január 1, 2018 éjfél után és január 10, 2018 éjfél után, amelyet a számítási csomóponttól kapott, a számítási csomópontot tartalmazó készlet azonosítóját adja meg, és számítja ki a csomópont-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="068e9-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="068e9-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="068e9-116">Example 3</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="068e9-117">A számítási csomópontot az 2018-es verzióban, az éjfél után, az 2018 éjfél után, a kiszámított csomópont objektumból kapott.</span><span class="sxs-lookup"><span data-stu-id="068e9-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="068e9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="068e9-118">PARAMETERS</span></span>

### <span data-ttu-id="068e9-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="068e9-119">-BatchContext</span></span>
<span data-ttu-id="068e9-120">A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.</span><span class="sxs-lookup"><span data-stu-id="068e9-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="068e9-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="068e9-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="068e9-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="068e9-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="068e9-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="068e9-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="068e9-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="068e9-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="068e9-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="068e9-125">-ComputeNode</span></span>
<span data-ttu-id="068e9-126">Azt a **PSComputeNode** -objektumot adja meg, amelyből a szolgáltatási naplók beolvashatók.</span><span class="sxs-lookup"><span data-stu-id="068e9-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="068e9-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="068e9-127">-ComputeNodeId</span></span>
<span data-ttu-id="068e9-128">A számítási csomópont azonosítója.</span><span class="sxs-lookup"><span data-stu-id="068e9-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="068e9-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="068e9-129">-ContainerUrl</span></span>
<span data-ttu-id="068e9-130">Az Azure Storage tároló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="068e9-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068e9-131">-DefaultProfile</span></span>
<span data-ttu-id="068e9-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="068e9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="068e9-133">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="068e9-133">-EndTime</span></span>
<span data-ttu-id="068e9-134">A szolgáltatás-napló feltöltésének befejezési időpontja (nem kötelező).</span><span class="sxs-lookup"><span data-stu-id="068e9-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e9-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="068e9-135">-PoolId</span></span>
<span data-ttu-id="068e9-136">A számítási csomópontot tartalmazó készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="068e9-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="068e9-137">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="068e9-137">-StartTime</span></span>
<span data-ttu-id="068e9-138">A szolgáltatás-napló feltöltésének kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="068e9-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e9-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="068e9-139">-Confirm</span></span>
<span data-ttu-id="068e9-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="068e9-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="068e9-141">-WhatIf</span></span>
<span data-ttu-id="068e9-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="068e9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="068e9-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="068e9-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068e9-144">CommonParameters</span></span>
<span data-ttu-id="068e9-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="068e9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068e9-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="068e9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068e9-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="068e9-147">INPUTS</span></span>

### <span data-ttu-id="068e9-148">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="068e9-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="068e9-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="068e9-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="068e9-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="068e9-150">OUTPUTS</span></span>

### <span data-ttu-id="068e9-151">Microsoft.Azure.Commands.BatCH. Modellek. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="068e9-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="068e9-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="068e9-152">NOTES</span></span>

## <span data-ttu-id="068e9-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="068e9-153">RELATED LINKS</span></span>
