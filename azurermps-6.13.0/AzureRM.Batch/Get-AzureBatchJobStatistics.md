---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 0a43f98a926da76f2127589477e8c9f771a032cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492013"
---
# <span data-ttu-id="aa819-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="aa819-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="aa819-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa819-102">SYNOPSIS</span></span>
<span data-ttu-id="aa819-103">A kötegelt fiókok összefoglaló statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="aa819-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa819-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa819-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa819-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa819-105">DESCRIPTION</span></span>
<span data-ttu-id="aa819-106">A **Get-AzureBatchJobStatistics** parancsmag az Azure-alapú köteg-fiók összes feladatához megkapja az életprevalencia összesített statisztikáját.</span><span class="sxs-lookup"><span data-stu-id="aa819-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="aa819-107">A statisztika összesítve van a fiókban valaha létező összes feladatban, a fiók létrehozása és a statisztika utolsó frissítési időpontja között.</span><span class="sxs-lookup"><span data-stu-id="aa819-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="aa819-108">Példák</span><span class="sxs-lookup"><span data-stu-id="aa819-108">EXAMPLES</span></span>

### <span data-ttu-id="aa819-109">Példa 1: Összefoglaló statisztika beszerzése az összes feladathoz</span><span class="sxs-lookup"><span data-stu-id="aa819-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
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

<span data-ttu-id="aa819-110">Az első parancs a **Get-AzureRmBatchAccountKeys** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="aa819-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="aa819-111">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="aa819-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="aa819-112">A második parancs az összes projekt összefoglaló statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="aa819-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="aa819-113">A parancs az első parancs $Context értékét használja.</span><span class="sxs-lookup"><span data-stu-id="aa819-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="aa819-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa819-114">PARAMETERS</span></span>

### <span data-ttu-id="aa819-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aa819-115">-BatchContext</span></span>
<span data-ttu-id="aa819-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="aa819-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aa819-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="aa819-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="aa819-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="aa819-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="aa819-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="aa819-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="aa819-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="aa819-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="aa819-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa819-121">-DefaultProfile</span></span>
<span data-ttu-id="aa819-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa819-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa819-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa819-123">CommonParameters</span></span>
<span data-ttu-id="aa819-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa819-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa819-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa819-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa819-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa819-126">INPUTS</span></span>

### <span data-ttu-id="aa819-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aa819-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="aa819-128">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aa819-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="aa819-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa819-129">OUTPUTS</span></span>

### <span data-ttu-id="aa819-130">Microsoft.Azure.Commands.BatCH. Modellek. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="aa819-130">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="aa819-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa819-131">NOTES</span></span>

## <span data-ttu-id="aa819-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa819-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa819-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aa819-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="aa819-134">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="aa819-134">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="aa819-135">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="aa819-135">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


