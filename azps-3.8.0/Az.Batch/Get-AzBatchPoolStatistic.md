---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 650d5fdd615ad44c30417eb0927e4c946e6a92d5
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017180"
---
# <span data-ttu-id="c4607-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="c4607-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="c4607-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4607-102">SYNOPSIS</span></span>
<span data-ttu-id="c4607-103">A kötegelt fiókokat összegző statisztikaként kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c4607-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="c4607-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4607-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4607-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4607-105">DESCRIPTION</span></span>
<span data-ttu-id="c4607-106">A **Get-AzBatchPoolStatistic** parancsmag a megadott fiók összes készletének élettartam statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="c4607-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="c4607-107">A statisztika összesítve van a fiókban valaha létező összes készleten, a fiók létrehozása és a statisztika utolsó frissítési időpontja között.</span><span class="sxs-lookup"><span data-stu-id="c4607-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="c4607-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c4607-108">EXAMPLES</span></span>

### <span data-ttu-id="c4607-109">Példa 1: erőforrás-statisztika beszerzése az összes készletről egy fiókban</span><span class="sxs-lookup"><span data-stu-id="c4607-109">Example 1: Get resource statistics of all pools in an account</span></span>
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

<span data-ttu-id="c4607-110">Az első parancs a **Get-AzBatchAccountKey** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="c4607-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="c4607-111">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="c4607-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="c4607-112">A második parancs a megadott fiók összes készletének statisztikáját kapja, majd a $PoolStatistics tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="c4607-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="c4607-113">A végleges parancs megjeleníti az $PoolStatistics **ResourceStatistics** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c4607-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="c4607-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4607-114">PARAMETERS</span></span>

### <span data-ttu-id="c4607-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c4607-115">-BatchContext</span></span>
<span data-ttu-id="c4607-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="c4607-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c4607-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="c4607-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c4607-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="c4607-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c4607-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="c4607-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c4607-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="c4607-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c4607-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4607-121">-DefaultProfile</span></span>
<span data-ttu-id="c4607-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4607-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4607-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4607-123">CommonParameters</span></span>
<span data-ttu-id="c4607-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4607-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4607-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c4607-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4607-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4607-126">INPUTS</span></span>

### <span data-ttu-id="c4607-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c4607-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c4607-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4607-128">OUTPUTS</span></span>

### <span data-ttu-id="c4607-129">Microsoft.Azure.Commands.BatCH. Modellek. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="c4607-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="c4607-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4607-130">NOTES</span></span>

## <span data-ttu-id="c4607-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4607-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4607-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4607-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c4607-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="c4607-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="c4607-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="c4607-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)


