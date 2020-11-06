---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: d25e9aeb75c58bcce560043d87f5ce9eef065b97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500276"
---
# <span data-ttu-id="6f09f-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="6f09f-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="6f09f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f09f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f09f-103">A számítási csomópont távoli bejelentkezési beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6f09f-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f09f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f09f-104">SYNTAX</span></span>

### <span data-ttu-id="6f09f-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f09f-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f09f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6f09f-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f09f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f09f-107">DESCRIPTION</span></span>
<span data-ttu-id="6f09f-108">A **Get-AzureBatchRemoteLoginSettings** parancsmag a virtuális gépek infrastruktúra-alapú készletében a számítási csomópont távoli bejelentkezési beállításait kapja.</span><span class="sxs-lookup"><span data-stu-id="6f09f-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="6f09f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6f09f-109">EXAMPLES</span></span>

### <span data-ttu-id="6f09f-110">Példa 1: távoli bejelentkezési beállítások beszerzése a készlet összes csomópontjára</span><span class="sxs-lookup"><span data-stu-id="6f09f-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="6f09f-111">Az első parancs a **Get-AzureRmBatchAccountKeys használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="6f09f-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="6f09f-112">A parancs a következő parancsban a $Context változó környezetét tárolja.</span><span class="sxs-lookup"><span data-stu-id="6f09f-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="6f09f-113">A második parancs a **Get-AzureBatchComputeNode** segítségével az azonosító ContosoPool tartalmazó készlet minden számítási csomópontját bekapja.</span><span class="sxs-lookup"><span data-stu-id="6f09f-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="6f09f-114">A parancs a csővezeték-kezelő használatával továbbítja az egyes számítógép-csomópontokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6f09f-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6f09f-115">A parancs minden számítási csomóponthoz megkapja a távoli bejelentkezési beállításokat.</span><span class="sxs-lookup"><span data-stu-id="6f09f-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="6f09f-116">2. példa: egy csomópont távoli bejelentkezési beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="6f09f-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="6f09f-117">Az első parancs beolvassa az előfizetéshez tartozó hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét, majd a $Context változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6f09f-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="6f09f-118">A második parancs beolvassa a számítási csomópont távoli bejelentkezési beállításait, amely az azonosító ContosoPool tartalmazó készletben a megadott azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6f09f-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="6f09f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f09f-119">PARAMETERS</span></span>

### <span data-ttu-id="6f09f-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6f09f-120">-BatchContext</span></span>
<span data-ttu-id="6f09f-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="6f09f-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f09f-122">Az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** beolvasásához használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6f09f-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6f09f-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="6f09f-123">-ComputeNode</span></span>
<span data-ttu-id="6f09f-124">A számítási csomópontot **PSComputeNode** objektumként adja meg, amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.</span><span class="sxs-lookup"><span data-stu-id="6f09f-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="6f09f-125">A számítási csomópont objektum beolvasásához használja az Get-AzureBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6f09f-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="6f09f-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="6f09f-126">-ComputeNodeId</span></span>
<span data-ttu-id="6f09f-127">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyhez a távoli bejelentkezési beállításokat be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="6f09f-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="6f09f-128">amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.</span><span class="sxs-lookup"><span data-stu-id="6f09f-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="6f09f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f09f-129">-DefaultProfile</span></span>
<span data-ttu-id="6f09f-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f09f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f09f-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6f09f-131">-PoolId</span></span>
<span data-ttu-id="6f09f-132">A virtuális gépet tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f09f-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="6f09f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f09f-133">CommonParameters</span></span>
<span data-ttu-id="6f09f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f09f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f09f-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f09f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f09f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f09f-136">INPUTS</span></span>

### <span data-ttu-id="6f09f-137">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="6f09f-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="6f09f-138">Paraméterek: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6f09f-138">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="6f09f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6f09f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6f09f-140">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6f09f-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6f09f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f09f-141">OUTPUTS</span></span>

### <span data-ttu-id="6f09f-142">Microsoft.Azure.Commands.BatCH. Modellek. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="6f09f-142">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="6f09f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f09f-143">NOTES</span></span>

## <span data-ttu-id="6f09f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f09f-144">RELATED LINKS</span></span>

[<span data-ttu-id="6f09f-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6f09f-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6f09f-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6f09f-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="6f09f-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="6f09f-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="6f09f-148">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6f09f-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


