---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: c560964308fe3bb2195f601f2e4138e022aa41e0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847881"
---
# <span data-ttu-id="b7cf7-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b7cf7-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="b7cf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cf7-103">Letiltja a kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-103">Disables a Batch job.</span></span>

## <span data-ttu-id="b7cf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7cf7-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7cf7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="b7cf7-106">A **disable-AzBatchJob** parancsmag letiltja az Azure-kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="b7cf7-107">Miután engedélyezte a feladatot, az új feladatok futhatnak.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="b7cf7-108">A letiltott feladatok nem futtathatnak új feladatokat.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="b7cf7-109">A letiltott feladatok később is engedélyezhetők.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="b7cf7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b7cf7-110">EXAMPLES</span></span>

### <span data-ttu-id="b7cf7-111">Példa 1: kötegelt feladat letiltása</span><span class="sxs-lookup"><span data-stu-id="b7cf7-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="b7cf7-112">Ez a parancs letiltja azt a feladatot, amely az ID Job-000001 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b7cf7-113">A parancs befejezi a feladat aktív tevékenységeit.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="b7cf7-114">A **Get-AzBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b7cf7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7cf7-115">PARAMETERS</span></span>

### <span data-ttu-id="b7cf7-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b7cf7-116">-BatchContext</span></span>
<span data-ttu-id="b7cf7-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b7cf7-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b7cf7-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b7cf7-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b7cf7-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b7cf7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cf7-122">-DefaultProfile</span></span>
<span data-ttu-id="b7cf7-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7cf7-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="b7cf7-124">-DisableJobOption</span></span>
<span data-ttu-id="b7cf7-125">Itt adhatja meg, hogy mi történjen a parancsmag által kikapcsolt tevékenységhez társított aktív feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="b7cf7-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b7cf7-126">Valid values are:</span></span> 
- <span data-ttu-id="b7cf7-127">Újravárólista</span><span class="sxs-lookup"><span data-stu-id="b7cf7-127">Requeue</span></span> 
- <span data-ttu-id="b7cf7-128">Lezáró</span><span class="sxs-lookup"><span data-stu-id="b7cf7-128">Terminate</span></span> 
- <span data-ttu-id="b7cf7-129">várj</span><span class="sxs-lookup"><span data-stu-id="b7cf7-129">Wait</span></span>

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

### <span data-ttu-id="b7cf7-130">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b7cf7-130">-Id</span></span>
<span data-ttu-id="b7cf7-131">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="b7cf7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cf7-132">CommonParameters</span></span>
<span data-ttu-id="b7cf7-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7cf7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cf7-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7cf7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cf7-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7cf7-135">INPUTS</span></span>

### <span data-ttu-id="b7cf7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b7cf7-136">System.String</span></span>

### <span data-ttu-id="b7cf7-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b7cf7-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b7cf7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7cf7-138">OUTPUTS</span></span>

### <span data-ttu-id="b7cf7-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="b7cf7-139">System.Void</span></span>

## <span data-ttu-id="b7cf7-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7cf7-140">NOTES</span></span>

## <span data-ttu-id="b7cf7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7cf7-141">RELATED LINKS</span></span>

[<span data-ttu-id="b7cf7-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b7cf7-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="b7cf7-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b7cf7-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b7cf7-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b7cf7-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b7cf7-145">Új – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b7cf7-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="b7cf7-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b7cf7-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="b7cf7-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b7cf7-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="b7cf7-148">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b7cf7-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


