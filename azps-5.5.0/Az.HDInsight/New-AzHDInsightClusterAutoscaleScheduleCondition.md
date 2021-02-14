---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167506"
---
# <span data-ttu-id="f736c-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="f736c-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="f736c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f736c-102">SYNOPSIS</span></span>
<span data-ttu-id="f736c-103">Automatikus ütemezési feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f736c-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="f736c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f736c-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f736c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f736c-105">DESCRIPTION</span></span>
<span data-ttu-id="f736c-106">A **New-AzHDInsightClusterAutoscaleScheduleCondition** parancsmag ütemezés-alapú automatikus skálázási feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f736c-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="f736c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f736c-107">EXAMPLES</span></span>

### <span data-ttu-id="f736c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f736c-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="f736c-109">Ez a parancs olyan feltételt hoz létre, amely esetén a fürt automatikus méretezése 5 munkavégző csomópontra 9:00-kor, minden hétfőn, szerdán.</span><span class="sxs-lookup"><span data-stu-id="f736c-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="f736c-110">2. példa: Az automatikus skálázási feltételt is megszabaduló fürt automatikus skálázásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="f736c-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="f736c-111">Ez a parancs egy olyan feltételt hoz létre, amelyben a fürt automatikus méretezése 5 dolgozói csomópontra 09:00 órakor minden hétfőn, szerdán.</span><span class="sxs-lookup"><span data-stu-id="f736c-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="f736c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f736c-112">PARAMETERS</span></span>

### <span data-ttu-id="f736c-113">-Day</span><span class="sxs-lookup"><span data-stu-id="f736c-113">-Day</span></span>
<span data-ttu-id="f736c-114">Beállítja vagy beállítja az automatikus méretezés ütemezési feltételének napjait.</span><span class="sxs-lookup"><span data-stu-id="f736c-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="f736c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f736c-115">-DefaultProfile</span></span>
<span data-ttu-id="f736c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f736c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f736c-117">-Time</span><span class="sxs-lookup"><span data-stu-id="f736c-117">-Time</span></span>
<span data-ttu-id="f736c-118">Beállítja vagy beállítja az automatikus méretezés ütemezési feltételének idejét.</span><span class="sxs-lookup"><span data-stu-id="f736c-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="f736c-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="f736c-119">-WorkerNodeCount</span></span>
<span data-ttu-id="f736c-120">Beállítja vagy beállítja az automatikus beosztás ütemezési feltételének ütemezési számát.</span><span class="sxs-lookup"><span data-stu-id="f736c-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="f736c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f736c-121">CommonParameters</span></span>
<span data-ttu-id="f736c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f736c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f736c-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f736c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f736c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f736c-124">INPUTS</span></span>

### <span data-ttu-id="f736c-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="f736c-125">None</span></span>

## <span data-ttu-id="f736c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f736c-126">OUTPUTS</span></span>

### <span data-ttu-id="f736c-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="f736c-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="f736c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f736c-128">NOTES</span></span>

## <span data-ttu-id="f736c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f736c-129">RELATED LINKS</span></span>

<span data-ttu-id="f736c-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f736c-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
