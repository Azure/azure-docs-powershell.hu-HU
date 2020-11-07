---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 03c37bb1cf70dfefc5373e9211d6365feb133ad4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847902"
---
# <span data-ttu-id="39f28-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="39f28-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="39f28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39f28-102">SYNOPSIS</span></span>
<span data-ttu-id="39f28-103">A számítási csomópont távoli bejelentkezési beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="39f28-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="39f28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39f28-104">SYNTAX</span></span>

### <span data-ttu-id="39f28-105">Azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39f28-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f28-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="39f28-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39f28-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="39f28-107">DESCRIPTION</span></span>
<span data-ttu-id="39f28-108">A **Get-AzBatchRemoteLoginSetting** parancsmag a virtuális gépek infrastruktúra-alapú készletében a számítási csomópont távoli bejelentkezési beállításait kapja.</span><span class="sxs-lookup"><span data-stu-id="39f28-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="39f28-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39f28-109">EXAMPLES</span></span>

### <span data-ttu-id="39f28-110">Példa 1: távoli bejelentkezési beállítások beszerzése a készlet összes csomópontjára</span><span class="sxs-lookup"><span data-stu-id="39f28-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="39f28-111">Az első parancs a **Get-AzBatchAccountKeys használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="39f28-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="39f28-112">A parancs a következő parancsban a $Context változó környezetét tárolja.</span><span class="sxs-lookup"><span data-stu-id="39f28-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="39f28-113">A második parancs a **Get-AzBatchComputeNode** segítségével az azonosító ContosoPool tartalmazó készlet minden számítási csomópontját bekapja.</span><span class="sxs-lookup"><span data-stu-id="39f28-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="39f28-114">A parancs a csővezeték-kezelő használatával továbbítja az egyes számítógép-csomópontokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="39f28-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="39f28-115">A parancs minden számítási csomóponthoz megkapja a távoli bejelentkezési beállításokat.</span><span class="sxs-lookup"><span data-stu-id="39f28-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="39f28-116">2. példa: egy csomópont távoli bejelentkezési beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="39f28-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="39f28-117">Az első parancs beolvassa az előfizetéshez tartozó hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét, majd a $Context változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="39f28-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="39f28-118">A második parancs beolvassa a számítási csomópont távoli bejelentkezési beállításait, amely az azonosító ContosoPool tartalmazó készletben a megadott azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="39f28-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="39f28-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39f28-119">PARAMETERS</span></span>

### <span data-ttu-id="39f28-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="39f28-120">-BatchContext</span></span>
<span data-ttu-id="39f28-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="39f28-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="39f28-122">Az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** beolvasásához használja az Get-AzBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="39f28-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="39f28-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="39f28-123">-ComputeNode</span></span>
<span data-ttu-id="39f28-124">A számítási csomópontot **PSComputeNode** objektumként adja meg, amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.</span><span class="sxs-lookup"><span data-stu-id="39f28-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="39f28-125">A számítási csomópont objektum beolvasásához használja az Get-AzBatchComputeNode parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="39f28-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="39f28-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="39f28-126">-ComputeNodeId</span></span>
<span data-ttu-id="39f28-127">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyhez a távoli bejelentkezési beállításokat be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="39f28-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="39f28-128">amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.</span><span class="sxs-lookup"><span data-stu-id="39f28-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="39f28-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f28-129">-DefaultProfile</span></span>
<span data-ttu-id="39f28-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39f28-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39f28-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="39f28-131">-PoolId</span></span>
<span data-ttu-id="39f28-132">A virtuális gépet tartalmazó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f28-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="39f28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f28-133">CommonParameters</span></span>
<span data-ttu-id="39f28-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39f28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f28-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f28-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f28-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39f28-136">INPUTS</span></span>

### <span data-ttu-id="39f28-137">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="39f28-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="39f28-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="39f28-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="39f28-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39f28-139">OUTPUTS</span></span>

### <span data-ttu-id="39f28-140">Microsoft.Azure.Commands.BatCH. Modellek. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="39f28-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="39f28-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39f28-141">NOTES</span></span>

## <span data-ttu-id="39f28-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39f28-142">RELATED LINKS</span></span>

[<span data-ttu-id="39f28-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="39f28-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="39f28-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="39f28-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="39f28-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="39f28-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="39f28-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="39f28-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


