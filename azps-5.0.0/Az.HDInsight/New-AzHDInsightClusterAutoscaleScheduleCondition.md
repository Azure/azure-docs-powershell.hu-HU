---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185363"
---
# <span data-ttu-id="e2556-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="e2556-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="e2556-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2556-102">SYNOPSIS</span></span>
<span data-ttu-id="e2556-103">Ütemezési alapú autoscale-feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e2556-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="e2556-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2556-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2556-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2556-105">DESCRIPTION</span></span>
<span data-ttu-id="e2556-106">A **New-AzHDInsightClusterAutoscaleScheduleCondition** parancsmag az ütemezési alapú autoscale feltételt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e2556-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="e2556-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e2556-107">EXAMPLES</span></span>

### <span data-ttu-id="e2556-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2556-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="e2556-109">Ez a parancs olyan feltételt hoz létre, amelyben a cluster autoscale 5 munkacsomópontra, a 09:00 minden hétfőn, szerdán található.</span><span class="sxs-lookup"><span data-stu-id="e2556-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="e2556-110">2. példa: egy fürt ütemterven alapuló automatikus méretezésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="e2556-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="e2556-111">Ez a parancs olyan feltételt hoz létre, amelyben a cluster autoscale 5 munkacsomópontra, a 09:00 minden hétfőn, szerdán található.</span><span class="sxs-lookup"><span data-stu-id="e2556-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="e2556-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2556-112">PARAMETERS</span></span>

### <span data-ttu-id="e2556-113">Napos</span><span class="sxs-lookup"><span data-stu-id="e2556-113">-Day</span></span>
<span data-ttu-id="e2556-114">Az automéretarány ütemezési feltételének a napjait adja meg vagy adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2556-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="e2556-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2556-115">-DefaultProfile</span></span>
<span data-ttu-id="e2556-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2556-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2556-117">-Idő</span><span class="sxs-lookup"><span data-stu-id="e2556-117">-Time</span></span>
<span data-ttu-id="e2556-118">Az automéretarány ütemezési feltételének beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="e2556-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="e2556-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="e2556-119">-WorkerNodeCount</span></span>
<span data-ttu-id="e2556-120">Beilleszti vagy beállítja az ütemezés workernode az automéretarány ütemezési feltételének számát.</span><span class="sxs-lookup"><span data-stu-id="e2556-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="e2556-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2556-121">CommonParameters</span></span>
<span data-ttu-id="e2556-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2556-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2556-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2556-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2556-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2556-124">INPUTS</span></span>

### <span data-ttu-id="e2556-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2556-125">None</span></span>

## <span data-ttu-id="e2556-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2556-126">OUTPUTS</span></span>

### <span data-ttu-id="e2556-127">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="e2556-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="e2556-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2556-128">NOTES</span></span>

## <span data-ttu-id="e2556-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2556-129">RELATED LINKS</span></span>

<span data-ttu-id="e2556-130">[Új – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e2556-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>