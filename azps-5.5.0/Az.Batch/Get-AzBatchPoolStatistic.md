---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 49aa971dcc9d46f5a063042cbcdf8ca449c41e94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164339"
---
# <span data-ttu-id="96e00-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="96e00-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="96e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96e00-102">SYNOPSIS</span></span>
<span data-ttu-id="96e00-103">Készlet-összegző statisztikákat kap egy Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="96e00-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="96e00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96e00-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96e00-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96e00-105">DESCRIPTION</span></span>
<span data-ttu-id="96e00-106">A **Get-AzBatchPoolStatistic** parancsmag lekérte a megadott fiók összes készletének élettartam-statisztikáját.</span><span class="sxs-lookup"><span data-stu-id="96e00-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="96e00-107">A statisztikák a fiókban már létező összes készlet összesítve létezik, a fiók létrehozásától a statisztika legutóbbi frissítésének időpontig.</span><span class="sxs-lookup"><span data-stu-id="96e00-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="96e00-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96e00-108">EXAMPLES</span></span>

### <span data-ttu-id="96e00-109">1. példa: Egy fiók összes készletének erőforrás-statisztikája</span><span class="sxs-lookup"><span data-stu-id="96e00-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="96e00-110">Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**</span><span class="sxs-lookup"><span data-stu-id="96e00-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="96e00-111">A parancs ezt az objektumhivatkozást a $Context tárolja.</span><span class="sxs-lookup"><span data-stu-id="96e00-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="96e00-112">A második parancs bekérte a megadott fiók összes készletének statisztikáját, majd a $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="96e00-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="96e00-113">Az utolsó parancs  megjeleníti a $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="96e00-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="96e00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96e00-114">PARAMETERS</span></span>

### <span data-ttu-id="96e00-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="96e00-115">-BatchContext</span></span>
<span data-ttu-id="96e00-116">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="96e00-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="96e00-117">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="96e00-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="96e00-118">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="96e00-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="96e00-119">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="96e00-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="96e00-120">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="96e00-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="96e00-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e00-121">-DefaultProfile</span></span>
<span data-ttu-id="96e00-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96e00-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96e00-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e00-123">CommonParameters</span></span>
<span data-ttu-id="96e00-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e00-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e00-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96e00-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e00-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96e00-126">INPUTS</span></span>

### <span data-ttu-id="96e00-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="96e00-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="96e00-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e00-128">OUTPUTS</span></span>

### <span data-ttu-id="96e00-129">Microsoft.Azure.Commands.Bat. Models.PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="96e00-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="96e00-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96e00-130">NOTES</span></span>

## <span data-ttu-id="96e00-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96e00-131">RELATED LINKS</span></span>

[<span data-ttu-id="96e00-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="96e00-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="96e00-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="96e00-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="96e00-134">Get-AzBatchStatistic</span><span class="sxs-lookup"><span data-stu-id="96e00-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)
