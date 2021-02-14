---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167435"
---
# <span data-ttu-id="ac8e3-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac8e3-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="ac8e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac8e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8e3-103">A HDInsight-fürt automatikus skálázási konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="ac8e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac8e3-104">SYNTAX</span></span>

### <span data-ttu-id="ac8e3-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac8e3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac8e3-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8e3-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac8e3-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8e3-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac8e3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac8e3-108">DESCRIPTION</span></span>
<span data-ttu-id="ac8e3-109">A **Remove-AzHDInsightClusterAutoscaleConfiguration parancsmag** eltávolítja a HDInsight-fürt automatikus skálás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="ac8e3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac8e3-110">EXAMPLES</span></span>

### <span data-ttu-id="ac8e3-111">1. példa: Távolítsa el a HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="ac8e3-112">Ez a parancs eltávolítja a HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="ac8e3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac8e3-113">PARAMETERS</span></span>

### <span data-ttu-id="ac8e3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac8e3-114">-AsJob</span></span>
<span data-ttu-id="ac8e3-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ac8e3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac8e3-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ac8e3-116">-ClusterName</span></span>
<span data-ttu-id="ac8e3-117">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8e3-118">-DefaultProfile</span></span>
<span data-ttu-id="ac8e3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac8e3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac8e3-120">-InputObject</span></span>
<span data-ttu-id="ac8e3-121">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac8e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac8e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="ac8e3-123">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8e3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac8e3-124">-ResourceId</span></span>
<span data-ttu-id="ac8e3-125">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac8e3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac8e3-126">-Confirm</span></span>
<span data-ttu-id="ac8e3-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac8e3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac8e3-128">-WhatIf</span></span>
<span data-ttu-id="ac8e3-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac8e3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac8e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8e3-131">CommonParameters</span></span>
<span data-ttu-id="ac8e3-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8e3-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac8e3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8e3-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac8e3-134">INPUTS</span></span>

### <span data-ttu-id="ac8e3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ac8e3-135">System.String</span></span>

### <span data-ttu-id="ac8e3-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ac8e3-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="ac8e3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac8e3-137">OUTPUTS</span></span>

### <span data-ttu-id="ac8e3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac8e3-138">System.Boolean</span></span>

## <span data-ttu-id="ac8e3-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac8e3-139">NOTES</span></span>

## <span data-ttu-id="ac8e3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac8e3-140">RELATED LINKS</span></span>

<span data-ttu-id="ac8e3-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ac8e3-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
