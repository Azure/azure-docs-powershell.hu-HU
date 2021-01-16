---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357054"
---
# <span data-ttu-id="9a4b9-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4b9-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9a4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4b9-103">Leállítja a köteg feladatütemtervét.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="9a4b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a4b9-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a4b9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="9a4b9-106">A **Stop-AzBatch JobSchedule** parancsmag leállít egy Azure Batch-feladatütemtervet.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="9a4b9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a4b9-107">EXAMPLES</span></span>

### <span data-ttu-id="9a4b9-108">1. példa: Munkabeosztás leállítása</span><span class="sxs-lookup"><span data-stu-id="9a4b9-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="9a4b9-109">Ez a parancs leállítja azt a munkabeosztást, amely a Feladatütemező17 azonosítót állítja le.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9a4b9-110">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9a4b9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a4b9-111">PARAMETERS</span></span>

### <span data-ttu-id="9a4b9-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9a4b9-112">-BatchContext</span></span>
<span data-ttu-id="9a4b9-113">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9a4b9-114">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9a4b9-115">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9a4b9-116">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9a4b9-117">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9a4b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4b9-118">-DefaultProfile</span></span>
<span data-ttu-id="9a4b9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a4b9-120">-Id</span><span class="sxs-lookup"><span data-stu-id="9a4b9-120">-Id</span></span>
<span data-ttu-id="9a4b9-121">A parancsmag által leállítható feladatütemterv azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="9a4b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4b9-122">CommonParameters</span></span>
<span data-ttu-id="9a4b9-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4b9-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a4b9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4b9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a4b9-125">INPUTS</span></span>

### <span data-ttu-id="9a4b9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9a4b9-126">System.String</span></span>

### <span data-ttu-id="9a4b9-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9a4b9-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9a4b9-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a4b9-128">OUTPUTS</span></span>

### <span data-ttu-id="9a4b9-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="9a4b9-129">System.Void</span></span>

## <span data-ttu-id="9a4b9-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a4b9-130">NOTES</span></span>

## <span data-ttu-id="9a4b9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a4b9-131">RELATED LINKS</span></span>

[<span data-ttu-id="9a4b9-132">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4b9-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="9a4b9-133">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4b9-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9a4b9-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9a4b9-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9a4b9-135">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4b9-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9a4b9-136">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4b9-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9a4b9-137">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4b9-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="9a4b9-138">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9a4b9-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
