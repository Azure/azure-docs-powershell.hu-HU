---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1919c773eb51f5e2d57333f42cbcc0793d4dad63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001541"
---
# <span data-ttu-id="7fa44-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fa44-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="7fa44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fa44-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa44-103">Beállítja egy Azure HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7fa44-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7fa44-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fa44-104">SYNTAX</span></span>

### <span data-ttu-id="7fa44-105">LoadAutoscaleByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fa44-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa44-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa44-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa44-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fa44-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa44-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa44-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa44-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa44-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fa44-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fa44-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fa44-114">DESCRIPTION</span></span>
<span data-ttu-id="7fa44-115">Ez a **Set-AzHDInsightClusterAutoscaleConfiguration** parancsmag beállítja egy Azure HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7fa44-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7fa44-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fa44-116">EXAMPLES</span></span>

### <span data-ttu-id="7fa44-117">1. példa: A HDInsight-fürt betöltésalapú automatikusskála-konfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="7fa44-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="7fa44-118">Ez a parancs beállítja egy Azure HDInsight-fürt betöltésalapú automatikusskála-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7fa44-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="7fa44-119">2. példa: A HDInsight-fürt ütemezésalapú automatikus skálázásának beállítása</span><span class="sxs-lookup"><span data-stu-id="7fa44-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="7fa44-120">Ez a parancs beállítja a HDInsight-fürt ütemezésalapú automatikusskála-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7fa44-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="7fa44-121">3. példa: A HDInsight-fürt automatikus skálázási konfigurációjának beállítása egy másik fürt alapján, amely beállította az automatikus skálázást</span><span class="sxs-lookup"><span data-stu-id="7fa44-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="7fa44-122">Ez a parancs beállítja a HDInsight-fürt automatikus skálázási konfigurációját egy másik fürt alapján.</span><span class="sxs-lookup"><span data-stu-id="7fa44-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="7fa44-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fa44-123">PARAMETERS</span></span>

### <span data-ttu-id="7fa44-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fa44-124">-AsJob</span></span>
<span data-ttu-id="7fa44-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7fa44-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fa44-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="7fa44-127">Beállítja vagy beállítja az automatikus skálázás konfigurációját</span><span class="sxs-lookup"><span data-stu-id="7fa44-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7fa44-128">-ClusterName</span></span>
<span data-ttu-id="7fa44-129">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="7fa44-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-130">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="7fa44-130">-Condition</span></span>
<span data-ttu-id="7fa44-131">Beállítja vagy beállítja az ütemezésalapú automatikus skálázás feltételét.</span><span class="sxs-lookup"><span data-stu-id="7fa44-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa44-132">-DefaultProfile</span></span>
<span data-ttu-id="7fa44-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fa44-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fa44-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fa44-134">-InputObject</span></span>
<span data-ttu-id="7fa44-135">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="7fa44-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="7fa44-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="7fa44-137">Beállítja vagy beállítja a munkaterhelés-alapú automatikus skálázás maximális számát.</span><span class="sxs-lookup"><span data-stu-id="7fa44-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="7fa44-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="7fa44-139">Beállítja vagy beállítja a munkaterhelés-alapú automatikus skálázás minimális számát.</span><span class="sxs-lookup"><span data-stu-id="7fa44-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa44-140">-ResourceGroupName</span></span>
<span data-ttu-id="7fa44-141">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="7fa44-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fa44-142">-ResourceId</span></span>
<span data-ttu-id="7fa44-143">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="7fa44-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-144">-Schedule</span><span class="sxs-lookup"><span data-stu-id="7fa44-144">-Schedule</span></span>
<span data-ttu-id="7fa44-145">Ütemezésen alapuló paraméterek beállítása</span><span class="sxs-lookup"><span data-stu-id="7fa44-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="7fa44-146">-TimeZone</span></span>
<span data-ttu-id="7fa44-147">Beállítja vagy beállítja az ütemezésalapú automatikus skálázás időzónát.</span><span class="sxs-lookup"><span data-stu-id="7fa44-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fa44-148">-Confirm</span></span>
<span data-ttu-id="7fa44-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7fa44-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fa44-150">-WhatIf</span></span>
<span data-ttu-id="7fa44-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7fa44-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fa44-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7fa44-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa44-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa44-153">CommonParameters</span></span>
<span data-ttu-id="7fa44-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa44-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa44-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fa44-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa44-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fa44-156">INPUTS</span></span>

### <span data-ttu-id="7fa44-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7fa44-157">System.String</span></span>

### <span data-ttu-id="7fa44-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7fa44-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="7fa44-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fa44-159">OUTPUTS</span></span>

### <span data-ttu-id="7fa44-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="7fa44-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="7fa44-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fa44-161">NOTES</span></span>

## <span data-ttu-id="7fa44-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fa44-162">RELATED LINKS</span></span>

<span data-ttu-id="7fa44-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7fa44-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
