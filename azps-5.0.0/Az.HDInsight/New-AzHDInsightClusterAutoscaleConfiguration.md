---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185364"
---
# <span data-ttu-id="4bc84-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bc84-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="4bc84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bc84-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc84-103">Olyan nem állandó objektumot hoz létre, amely leírja az Azure HDInsight-fürtök automatikus méretarányos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4bc84-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4bc84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bc84-104">SYNTAX</span></span>

### <span data-ttu-id="4bc84-105">LoadAutoscaleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bc84-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc84-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bc84-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bc84-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bc84-107">DESCRIPTION</span></span>
<span data-ttu-id="4bc84-108">A **New-AzHDInsightClusterAutoscaleConfiguration** parancsmag létrehoz egy nem állandó objektumot, amely leírja az Azure HDInsight-fürtök automatikus méretezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4bc84-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4bc84-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4bc84-109">EXAMPLES</span></span>

### <span data-ttu-id="4bc84-110">Példa 1: a betöltött automatikus méretezés konfigurációját leíró objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="4bc84-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="4bc84-111">Ezzel a paranccsal létrehoz egy olyan objektumot, amely a berakási automatikus méretezés konfigurációját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="4bc84-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="4bc84-112">2. példa: objektum létrehozása, amely leírja az ütemezési alapú automatikus méretezés konfigurációját</span><span class="sxs-lookup"><span data-stu-id="4bc84-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="4bc84-113">Ez a parancs létrehoz egy olyan objektumot, amely leírja az ütemezési alapú automatikus méretezés konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4bc84-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="4bc84-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bc84-114">PARAMETERS</span></span>

### <span data-ttu-id="4bc84-115">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="4bc84-115">-Condition</span></span>
<span data-ttu-id="4bc84-116">Beilleszti vagy beállítja az ütemterven alapuló autoskála állapotát.</span><span class="sxs-lookup"><span data-stu-id="4bc84-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc84-117">-DefaultProfile</span></span>
<span data-ttu-id="4bc84-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bc84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc84-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="4bc84-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="4bc84-120">Beolvassa vagy beállítja a betöltött számlálók maximális számát a workernode.</span><span class="sxs-lookup"><span data-stu-id="4bc84-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc84-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="4bc84-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="4bc84-122">Beilleszti vagy beállítja a berakási workernode minimális számát.</span><span class="sxs-lookup"><span data-stu-id="4bc84-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc84-123">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="4bc84-123">-TimeZone</span></span>
<span data-ttu-id="4bc84-124">Beilleszti vagy beállítja az ütemezési alapú autoscale időzónáját.</span><span class="sxs-lookup"><span data-stu-id="4bc84-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc84-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc84-125">CommonParameters</span></span>
<span data-ttu-id="4bc84-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bc84-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc84-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4bc84-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc84-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bc84-128">INPUTS</span></span>

### <span data-ttu-id="4bc84-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="4bc84-129">None</span></span>

## <span data-ttu-id="4bc84-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bc84-130">OUTPUTS</span></span>

### <span data-ttu-id="4bc84-131">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="4bc84-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="4bc84-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bc84-132">NOTES</span></span>

## <span data-ttu-id="4bc84-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bc84-133">RELATED LINKS</span></span>

<span data-ttu-id="4bc84-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4bc84-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
