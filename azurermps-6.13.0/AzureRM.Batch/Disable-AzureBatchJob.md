---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 141702ec7c60dcdb2dd94d5e259b2f14c8475316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672806"
---
# <span data-ttu-id="bf5e6-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bf5e6-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="bf5e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5e6-103">Letiltja a kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf5e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf5e6-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf5e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf5e6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf5e6-106">A **disable-AzureBatchJob** parancsmag letiltja az Azure-kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="bf5e6-107">Miután engedélyezte a feladatot, az új feladatok futhatnak.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="bf5e6-108">A letiltott feladatok nem futtathatnak új feladatokat.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="bf5e6-109">A letiltott feladatok később is engedélyezhetők.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="bf5e6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf5e6-110">EXAMPLES</span></span>

### <span data-ttu-id="bf5e6-111">Példa 1: kötegelt feladat letiltása</span><span class="sxs-lookup"><span data-stu-id="bf5e6-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="bf5e6-112">Ez a parancs letiltja azt a feladatot, amely az ID Job-000001 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="bf5e6-113">A parancs befejezi a feladat aktív tevékenységeit.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="bf5e6-114">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="bf5e6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf5e6-115">PARAMETERS</span></span>

### <span data-ttu-id="bf5e6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf5e6-116">-BatchContext</span></span>
<span data-ttu-id="bf5e6-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf5e6-118">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bf5e6-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bf5e6-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bf5e6-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bf5e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5e6-122">-DefaultProfile</span></span>
<span data-ttu-id="bf5e6-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf5e6-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="bf5e6-124">-DisableJobOption</span></span>
<span data-ttu-id="bf5e6-125">Itt adhatja meg, hogy mi történjen a parancsmag által kikapcsolt tevékenységhez társított aktív feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="bf5e6-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bf5e6-126">Valid values are:</span></span> 
- <span data-ttu-id="bf5e6-127">Újravárólista</span><span class="sxs-lookup"><span data-stu-id="bf5e6-127">Requeue</span></span> 
- <span data-ttu-id="bf5e6-128">Lezáró</span><span class="sxs-lookup"><span data-stu-id="bf5e6-128">Terminate</span></span> 
- <span data-ttu-id="bf5e6-129">várj</span><span class="sxs-lookup"><span data-stu-id="bf5e6-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5e6-130">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bf5e6-130">-Id</span></span>
<span data-ttu-id="bf5e6-131">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5e6-132">CommonParameters</span></span>
<span data-ttu-id="bf5e6-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf5e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5e6-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5e6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5e6-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf5e6-135">INPUTS</span></span>

### <span data-ttu-id="bf5e6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bf5e6-136">System.String</span></span>

### <span data-ttu-id="bf5e6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf5e6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="bf5e6-138">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf5e6-138">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="bf5e6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf5e6-139">OUTPUTS</span></span>

### <span data-ttu-id="bf5e6-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="bf5e6-140">System.Void</span></span>

## <span data-ttu-id="bf5e6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf5e6-141">NOTES</span></span>

## <span data-ttu-id="bf5e6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf5e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="bf5e6-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bf5e6-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="bf5e6-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bf5e6-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bf5e6-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bf5e6-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="bf5e6-146">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bf5e6-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="bf5e6-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bf5e6-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="bf5e6-148">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bf5e6-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="bf5e6-149">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf5e6-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


