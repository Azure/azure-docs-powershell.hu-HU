---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328366"
---
# <span data-ttu-id="de99a-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="de99a-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="de99a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de99a-102">SYNOPSIS</span></span>
<span data-ttu-id="de99a-103">Automatikus ütemezési feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="de99a-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="de99a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de99a-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de99a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de99a-105">DESCRIPTION</span></span>
<span data-ttu-id="de99a-106">A **New-AzHDInsightClusterAutoscaleScheduleCondition** parancsmag ütemezés-alapú automatikus skálázási feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="de99a-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="de99a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de99a-107">EXAMPLES</span></span>

### <span data-ttu-id="de99a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="de99a-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="de99a-109">Ez a parancs olyan feltételt hoz létre, amely esetén a fürt automatikus méretezése 5 munkavégző csomópontra 9:00-kor, minden hétfőn, szerdán.</span><span class="sxs-lookup"><span data-stu-id="de99a-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="de99a-110">2. példa: Az automatikus skálázási feltételt is megszabaduló fürt automatikus skálázásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="de99a-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="de99a-111">Ez a parancs olyan feltételt hoz létre, amely esetén a fürt automatikus méretezése 5 munkavégző csomópontra 9:00-kor, minden hétfőn, szerdán.</span><span class="sxs-lookup"><span data-stu-id="de99a-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="de99a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de99a-112">PARAMETERS</span></span>

### <span data-ttu-id="de99a-113">-Day</span><span class="sxs-lookup"><span data-stu-id="de99a-113">-Day</span></span>
<span data-ttu-id="de99a-114">Beállítja vagy beállítja az automatikus méretezés ütemezési feltételének napjait.</span><span class="sxs-lookup"><span data-stu-id="de99a-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de99a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de99a-115">-DefaultProfile</span></span>
<span data-ttu-id="de99a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de99a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de99a-117">-Time</span><span class="sxs-lookup"><span data-stu-id="de99a-117">-Time</span></span>
<span data-ttu-id="de99a-118">Beállítja vagy beállítja az automatikus méretezés ütemezési feltételének idejét.</span><span class="sxs-lookup"><span data-stu-id="de99a-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de99a-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="de99a-119">-WorkerNodeCount</span></span>
<span data-ttu-id="de99a-120">Beállítja vagy beállítja az automatikus beosztás ütemezési feltételének ütemezési számát a munkabeosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="de99a-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de99a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de99a-121">CommonParameters</span></span>
<span data-ttu-id="de99a-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de99a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de99a-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de99a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de99a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de99a-124">INPUTS</span></span>

### <span data-ttu-id="de99a-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="de99a-125">None</span></span>

## <span data-ttu-id="de99a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de99a-126">OUTPUTS</span></span>

### <span data-ttu-id="de99a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="de99a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="de99a-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de99a-128">NOTES</span></span>

## <span data-ttu-id="de99a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de99a-129">RELATED LINKS</span></span>

<span data-ttu-id="de99a-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="de99a-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
