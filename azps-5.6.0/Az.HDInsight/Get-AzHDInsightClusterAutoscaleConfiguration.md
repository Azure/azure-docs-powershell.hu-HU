---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 4f60445dc22c2e2b0f8c0c5291691f4d7456db2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012118"
---
# <span data-ttu-id="59be3-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="59be3-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="59be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59be3-102">SYNOPSIS</span></span>
<span data-ttu-id="59be3-103">A HDInsight-fürt automatikus skálázási konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59be3-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="59be3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59be3-104">SYNTAX</span></span>

### <span data-ttu-id="59be3-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59be3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59be3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59be3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59be3-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59be3-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59be3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59be3-108">DESCRIPTION</span></span>
<span data-ttu-id="59be3-109">A **Get-AzHDInsightClusterAutoscaleConfiguration parancsmag** megkapja a HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="59be3-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="59be3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59be3-110">EXAMPLES</span></span>

### <span data-ttu-id="59be3-111">1. példa: A HDInsight-fürt automatikus skálázási konfigurációjának lekérte.</span><span class="sxs-lookup"><span data-stu-id="59be3-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="59be3-112">Ez a parancs a HDInsight-fürt automatikus skálázási konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59be3-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="59be3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59be3-113">PARAMETERS</span></span>

### <span data-ttu-id="59be3-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="59be3-114">-ClusterName</span></span>
<span data-ttu-id="59be3-115">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="59be3-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59be3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59be3-116">-DefaultProfile</span></span>
<span data-ttu-id="59be3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59be3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59be3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59be3-118">-InputObject</span></span>
<span data-ttu-id="59be3-119">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="59be3-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59be3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59be3-120">-ResourceGroupName</span></span>
<span data-ttu-id="59be3-121">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="59be3-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59be3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59be3-122">-ResourceId</span></span>
<span data-ttu-id="59be3-123">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="59be3-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59be3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59be3-124">CommonParameters</span></span>
<span data-ttu-id="59be3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59be3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59be3-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59be3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59be3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59be3-127">INPUTS</span></span>

### <span data-ttu-id="59be3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="59be3-128">System.String</span></span>

### <span data-ttu-id="59be3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59be3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="59be3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59be3-130">OUTPUTS</span></span>

### <span data-ttu-id="59be3-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="59be3-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="59be3-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59be3-132">NOTES</span></span>

## <span data-ttu-id="59be3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59be3-133">RELATED LINKS</span></span>

<span data-ttu-id="59be3-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="59be3-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
