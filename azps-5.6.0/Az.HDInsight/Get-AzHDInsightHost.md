---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 5b58e535acae8d6d0845b6be8c838f8372af9c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012117"
---
# <span data-ttu-id="5b36f-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="5b36f-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="5b36f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b36f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b36f-103">A HDInsight-fürt állomáslistái.</span><span class="sxs-lookup"><span data-stu-id="5b36f-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="5b36f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b36f-104">SYNTAX</span></span>

### <span data-ttu-id="5b36f-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b36f-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b36f-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b36f-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b36f-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b36f-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b36f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b36f-108">DESCRIPTION</span></span>
<span data-ttu-id="5b36f-109">A **Get-AzHDInsightHost** parancsmag felsorolja a HDInsight-fürt állomásokat.</span><span class="sxs-lookup"><span data-stu-id="5b36f-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="5b36f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b36f-110">EXAMPLES</span></span>

### <span data-ttu-id="5b36f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5b36f-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="5b36f-112">Ez a parancslista a fürt állomáscsoportnevét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5b36f-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="5b36f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5b36f-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="5b36f-114">Ez a parancslisták a folyamatban futó fürt állomásokat sorolják fel.</span><span class="sxs-lookup"><span data-stu-id="5b36f-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="5b36f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b36f-115">PARAMETERS</span></span>

### <span data-ttu-id="5b36f-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5b36f-116">-ClusterName</span></span>
<span data-ttu-id="5b36f-117">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="5b36f-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b36f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b36f-118">-DefaultProfile</span></span>
<span data-ttu-id="5b36f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b36f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b36f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b36f-120">-InputObject</span></span>
<span data-ttu-id="5b36f-121">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="5b36f-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b36f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b36f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b36f-123">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="5b36f-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b36f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b36f-124">-ResourceId</span></span>
<span data-ttu-id="5b36f-125">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="5b36f-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b36f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b36f-126">CommonParameters</span></span>
<span data-ttu-id="5b36f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b36f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b36f-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b36f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b36f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b36f-129">INPUTS</span></span>

### <span data-ttu-id="5b36f-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5b36f-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="5b36f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b36f-131">OUTPUTS</span></span>

### <span data-ttu-id="5b36f-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="5b36f-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="5b36f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b36f-133">NOTES</span></span>

## <span data-ttu-id="5b36f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b36f-134">RELATED LINKS</span></span>
