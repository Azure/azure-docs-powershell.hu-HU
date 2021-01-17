---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478353"
---
# <span data-ttu-id="67e0e-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="67e0e-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="67e0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="67e0e-103">Egy Batch-fiókra vonatkozó összefoglaló statisztikákat kap.</span><span class="sxs-lookup"><span data-stu-id="67e0e-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="67e0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="67e0e-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67e0e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="67e0e-105">DESCRIPTION</span></span>
<span data-ttu-id="67e0e-106">A **Get-AzBatchStatistic parancsmag** az Azure Batch-fiók összes feladatának összesítő statisztikáját leküldi.</span><span class="sxs-lookup"><span data-stu-id="67e0e-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="67e0e-107">A statisztikák összesítve vannak minden olyan munkakörben, amely valaha is létezik a fiókban, a fiók létrehozásától a statisztika legutóbbi frissítésének időpontig.</span><span class="sxs-lookup"><span data-stu-id="67e0e-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="67e0e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="67e0e-108">EXAMPLES</span></span>

### <span data-ttu-id="67e0e-109">1. példa: Összesítő statisztika megjelenítése az összes álláshoz</span><span class="sxs-lookup"><span data-stu-id="67e0e-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="67e0e-110">Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**</span><span class="sxs-lookup"><span data-stu-id="67e0e-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="67e0e-111">A parancs ezt az objektumhivatkozást a $Context tárolja.</span><span class="sxs-lookup"><span data-stu-id="67e0e-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="67e0e-112">A második parancs az összes feladat összesített statisztikáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="67e0e-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="67e0e-113">A parancs az $Context első parancsból származó értéket használja.</span><span class="sxs-lookup"><span data-stu-id="67e0e-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="67e0e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67e0e-114">PARAMETERS</span></span>

### <span data-ttu-id="67e0e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="67e0e-115">-BatchContext</span></span>
<span data-ttu-id="67e0e-116">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="67e0e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="67e0e-117">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="67e0e-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="67e0e-118">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="67e0e-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="67e0e-119">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="67e0e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="67e0e-120">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="67e0e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="67e0e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e0e-121">-DefaultProfile</span></span>
<span data-ttu-id="67e0e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67e0e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e0e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e0e-123">CommonParameters</span></span>
<span data-ttu-id="67e0e-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e0e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e0e-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67e0e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e0e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67e0e-126">INPUTS</span></span>

### <span data-ttu-id="67e0e-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="67e0e-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="67e0e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67e0e-128">OUTPUTS</span></span>

### <span data-ttu-id="67e0e-129">Microsoft.Azure.Commands.Bat. Models.PSStatistics</span><span class="sxs-lookup"><span data-stu-id="67e0e-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="67e0e-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="67e0e-130">NOTES</span></span>

## <span data-ttu-id="67e0e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67e0e-131">RELATED LINKS</span></span>

[<span data-ttu-id="67e0e-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="67e0e-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="67e0e-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="67e0e-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="67e0e-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="67e0e-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
