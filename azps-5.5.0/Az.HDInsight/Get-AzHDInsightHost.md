---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 430c2aa7f38e6246c13ef6045f52346b580d20fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161579"
---
# <span data-ttu-id="0decd-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="0decd-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="0decd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0decd-102">SYNOPSIS</span></span>
<span data-ttu-id="0decd-103">A HDInsight-fürt állomáslistái.</span><span class="sxs-lookup"><span data-stu-id="0decd-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="0decd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0decd-104">SYNTAX</span></span>

### <span data-ttu-id="0decd-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0decd-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0decd-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0decd-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0decd-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0decd-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0decd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0decd-108">DESCRIPTION</span></span>
<span data-ttu-id="0decd-109">A **Get-AzHDInsightHost** parancsmag felsorolja a HDInsight-fürt állomásokat.</span><span class="sxs-lookup"><span data-stu-id="0decd-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="0decd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0decd-110">EXAMPLES</span></span>

### <span data-ttu-id="0decd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0decd-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="0decd-112">Ez a parancslista a fürt állomáscsoportnevét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0decd-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="0decd-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0decd-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="0decd-114">Ez a parancslisták a folyamatban futó fürt állomásokat sorolják fel.</span><span class="sxs-lookup"><span data-stu-id="0decd-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="0decd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0decd-115">PARAMETERS</span></span>

### <span data-ttu-id="0decd-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0decd-116">-ClusterName</span></span>
<span data-ttu-id="0decd-117">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="0decd-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="0decd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0decd-118">-DefaultProfile</span></span>
<span data-ttu-id="0decd-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0decd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0decd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0decd-120">-InputObject</span></span>
<span data-ttu-id="0decd-121">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="0decd-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="0decd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0decd-122">-ResourceGroupName</span></span>
<span data-ttu-id="0decd-123">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="0decd-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="0decd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0decd-124">-ResourceId</span></span>
<span data-ttu-id="0decd-125">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="0decd-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="0decd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0decd-126">CommonParameters</span></span>
<span data-ttu-id="0decd-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0decd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0decd-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0decd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0decd-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0decd-129">INPUTS</span></span>

### <span data-ttu-id="0decd-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0decd-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="0decd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0decd-131">OUTPUTS</span></span>

### <span data-ttu-id="0decd-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="0decd-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="0decd-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0decd-133">NOTES</span></span>

## <span data-ttu-id="0decd-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0decd-134">RELATED LINKS</span></span>
