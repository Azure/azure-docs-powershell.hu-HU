---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 545979c621a807c2a866fc5cf1d29aa0b659dc82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205367"
---
# <span data-ttu-id="da98a-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="da98a-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="da98a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da98a-102">SYNOPSIS</span></span>
<span data-ttu-id="da98a-103">Engedélyezi a köteget.</span><span class="sxs-lookup"><span data-stu-id="da98a-103">Enables a Batch job.</span></span>

## <span data-ttu-id="da98a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da98a-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da98a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da98a-105">DESCRIPTION</span></span>
<span data-ttu-id="da98a-106">Az **Enable-AzBatch Job parancsmag** engedélyezi az Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="da98a-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="da98a-107">A feladat engedélyezése után az új feladatok futtathatók.</span><span class="sxs-lookup"><span data-stu-id="da98a-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="da98a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da98a-108">EXAMPLES</span></span>

### <span data-ttu-id="da98a-109">1. példa: Kötegelt feladat engedélyezése</span><span class="sxs-lookup"><span data-stu-id="da98a-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="da98a-110">Ez a parancs engedélyezi a 000001 azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="da98a-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="da98a-111">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="da98a-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="da98a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da98a-112">PARAMETERS</span></span>

### <span data-ttu-id="da98a-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da98a-113">-BatchContext</span></span>
<span data-ttu-id="da98a-114">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="da98a-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da98a-115">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="da98a-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="da98a-116">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="da98a-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="da98a-117">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="da98a-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="da98a-118">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="da98a-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="da98a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da98a-119">-DefaultProfile</span></span>
<span data-ttu-id="da98a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da98a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da98a-121">-Id</span><span class="sxs-lookup"><span data-stu-id="da98a-121">-Id</span></span>
<span data-ttu-id="da98a-122">A parancsmag által lehetővé tesz feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da98a-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="da98a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da98a-123">CommonParameters</span></span>
<span data-ttu-id="da98a-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da98a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da98a-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da98a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da98a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da98a-126">INPUTS</span></span>

### <span data-ttu-id="da98a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="da98a-127">System.String</span></span>

### <span data-ttu-id="da98a-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da98a-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="da98a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da98a-129">OUTPUTS</span></span>

### <span data-ttu-id="da98a-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="da98a-130">System.Void</span></span>

## <span data-ttu-id="da98a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da98a-131">NOTES</span></span>

## <span data-ttu-id="da98a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da98a-132">RELATED LINKS</span></span>

[<span data-ttu-id="da98a-133">Disable-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="da98a-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="da98a-134">Get-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="da98a-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="da98a-135">New-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="da98a-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="da98a-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="da98a-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="da98a-137">Stop-AzBatchUpp</span><span class="sxs-lookup"><span data-stu-id="da98a-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="da98a-138">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="da98a-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
