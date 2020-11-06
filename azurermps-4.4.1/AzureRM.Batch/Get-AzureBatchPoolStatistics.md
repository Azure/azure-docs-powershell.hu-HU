---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: 25fe1f4e89b7ea569899fc980a55c3a30acbf77a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505239"
---
# <span data-ttu-id="9ddd3-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="9ddd3-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="9ddd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ddd3-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddd3-103">A kötegelt fiókokat összegző statisztikaként kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ddd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ddd3-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ddd3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ddd3-105">DESCRIPTION</span></span>
<span data-ttu-id="9ddd3-106">A **Get-AzureBatchPoolStatistics** parancsmag a megadott fiók összes készletének élettartam statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="9ddd3-107">A statisztika összesítve van a fiókban valaha létező összes készleten, a fiók létrehozása és a statisztika utolsó frissítési időpontja között.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="9ddd3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9ddd3-108">EXAMPLES</span></span>

### <span data-ttu-id="9ddd3-109">Példa 1: erőforrás-statisztika beszerzése az összes készletről egy fiókban</span><span class="sxs-lookup"><span data-stu-id="9ddd3-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
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

<span data-ttu-id="9ddd3-110">Az első parancs a **Get-AzureRmBatchAccountKeys** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="9ddd3-111">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="9ddd3-112">A második parancs a megadott fiók összes készletének statisztikáját kapja, majd a $PoolStatistics tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>

<span data-ttu-id="9ddd3-113">A végleges parancs megjeleníti az $PoolStatistics **ResourceStatistics** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="9ddd3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ddd3-114">PARAMETERS</span></span>

### <span data-ttu-id="9ddd3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9ddd3-115">-BatchContext</span></span>
<span data-ttu-id="9ddd3-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9ddd3-117">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9ddd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddd3-118">-DefaultProfile</span></span>
<span data-ttu-id="9ddd3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ddd3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ddd3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddd3-120">CommonParameters</span></span>
<span data-ttu-id="9ddd3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ddd3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddd3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddd3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddd3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ddd3-123">INPUTS</span></span>

### <span data-ttu-id="9ddd3-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9ddd3-124">BatchAccountContext</span></span>
<span data-ttu-id="9ddd3-125">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9ddd3-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9ddd3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ddd3-126">OUTPUTS</span></span>

### <span data-ttu-id="9ddd3-127">PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="9ddd3-127">PSPoolStatistics</span></span>

## <span data-ttu-id="9ddd3-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ddd3-128">NOTES</span></span>

## <span data-ttu-id="9ddd3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ddd3-129">RELATED LINKS</span></span>

[<span data-ttu-id="9ddd3-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9ddd3-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9ddd3-131">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="9ddd3-131">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="9ddd3-132">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="9ddd3-132">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


