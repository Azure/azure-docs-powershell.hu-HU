---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bfc14e0fba2b384766495dde9e3ef11fafd4653c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009045"
---
# <span data-ttu-id="a0375-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0375-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="a0375-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0375-102">SYNOPSIS</span></span>
<span data-ttu-id="a0375-103">Egy nem állandó objektumot hoz létre, amely leírja egy Azure HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a0375-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a0375-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0375-104">SYNTAX</span></span>

### <span data-ttu-id="a0375-105">LoadAutoscaleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0375-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0375-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0375-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0375-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0375-107">DESCRIPTION</span></span>
<span data-ttu-id="a0375-108">A **New-AzHDInsightClusterAutoscaleConfiguration** parancsmag létrehoz egy nem állandó objektumot, amely leírja egy Azure HDInsight-fürt automatikus skálás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a0375-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a0375-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0375-109">EXAMPLES</span></span>

### <span data-ttu-id="a0375-110">1. példa: Betöltésalapú automatikusskála-konfigurációt leíró objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a0375-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="a0375-111">Ez a parancs egy olyan objektumot hoz létre, amely leírja a betöltésalapú automatikusskála-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a0375-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="a0375-112">2. példa: Automatikus méretezés ütemezési konfigurációját leíró objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a0375-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="a0375-113">Ezzel a paranccsal olyan objektumot hoz létre, amely leírja az automatikus méretezés ütemezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a0375-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="a0375-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0375-114">PARAMETERS</span></span>

### <span data-ttu-id="a0375-115">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="a0375-115">-Condition</span></span>
<span data-ttu-id="a0375-116">Beállítja vagy beállítja az ütemezésalapú automatikus skálázás feltételét.</span><span class="sxs-lookup"><span data-stu-id="a0375-116">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="a0375-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0375-117">-DefaultProfile</span></span>
<span data-ttu-id="a0375-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0375-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0375-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="a0375-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="a0375-120">Beállítja vagy beállítja a munkaterhelés-alapú automatikus skálázás maximális számát.</span><span class="sxs-lookup"><span data-stu-id="a0375-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="a0375-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="a0375-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="a0375-122">Beállítja vagy beállítja a munkaterhelés-alapú automatikus skálázás minimális számát.</span><span class="sxs-lookup"><span data-stu-id="a0375-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="a0375-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="a0375-123">-TimeZone</span></span>
<span data-ttu-id="a0375-124">Beállítja vagy beállítja az ütemezésalapú automatikus skálázás időzónát.</span><span class="sxs-lookup"><span data-stu-id="a0375-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="a0375-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0375-125">CommonParameters</span></span>
<span data-ttu-id="a0375-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0375-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0375-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0375-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0375-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0375-128">INPUTS</span></span>

### <span data-ttu-id="a0375-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="a0375-129">None</span></span>

## <span data-ttu-id="a0375-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0375-130">OUTPUTS</span></span>

### <span data-ttu-id="a0375-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="a0375-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="a0375-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0375-132">NOTES</span></span>

## <span data-ttu-id="a0375-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0375-133">RELATED LINKS</span></span>

<span data-ttu-id="a0375-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0375-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
