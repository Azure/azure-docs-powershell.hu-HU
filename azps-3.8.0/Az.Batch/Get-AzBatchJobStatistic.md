---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: e93cbe2cb23545788330c79a2b02ff5f6db9f243
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017302"
---
# <span data-ttu-id="e1a05-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="e1a05-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="e1a05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1a05-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a05-103">A kötegelt fiókok összefoglaló statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="e1a05-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="e1a05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1a05-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1a05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1a05-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a05-106">A **Get-AzBatchJobStatistic** parancsmag az Azure-alapú köteg-fiók összes feladatához megkapja az életprevalencia összesített statisztikáját.</span><span class="sxs-lookup"><span data-stu-id="e1a05-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="e1a05-107">A statisztika összesítve van a fiókban valaha létező összes feladatban, a fiók létrehozása és a statisztika utolsó frissítési időpontja között.</span><span class="sxs-lookup"><span data-stu-id="e1a05-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="e1a05-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e1a05-108">EXAMPLES</span></span>

### <span data-ttu-id="e1a05-109">Példa 1: Összefoglaló statisztika beszerzése az összes feladathoz</span><span class="sxs-lookup"><span data-stu-id="e1a05-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="e1a05-110">Az első parancs a **Get-AzBatchAccountKey** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="e1a05-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="e1a05-111">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="e1a05-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="e1a05-112">A második parancs az összes projekt összefoglaló statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="e1a05-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="e1a05-113">A parancs az első parancs $Context értékét használja.</span><span class="sxs-lookup"><span data-stu-id="e1a05-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="e1a05-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1a05-114">PARAMETERS</span></span>

### <span data-ttu-id="e1a05-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e1a05-115">-BatchContext</span></span>
<span data-ttu-id="e1a05-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="e1a05-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e1a05-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e1a05-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e1a05-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="e1a05-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e1a05-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="e1a05-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e1a05-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="e1a05-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e1a05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a05-121">-DefaultProfile</span></span>
<span data-ttu-id="e1a05-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1a05-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1a05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a05-123">CommonParameters</span></span>
<span data-ttu-id="e1a05-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1a05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a05-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1a05-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a05-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a05-126">INPUTS</span></span>

### <span data-ttu-id="e1a05-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e1a05-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e1a05-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a05-128">OUTPUTS</span></span>

### <span data-ttu-id="e1a05-129">Microsoft.Azure.Commands.BatCH. Modellek. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="e1a05-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="e1a05-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1a05-130">NOTES</span></span>

## <span data-ttu-id="e1a05-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1a05-131">RELATED LINKS</span></span>

[<span data-ttu-id="e1a05-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e1a05-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e1a05-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="e1a05-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="e1a05-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="e1a05-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)


