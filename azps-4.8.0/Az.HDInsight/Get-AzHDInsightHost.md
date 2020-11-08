---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94023965"
---
# <span data-ttu-id="f3988-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="f3988-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="f3988-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3988-102">SYNOPSIS</span></span>
<span data-ttu-id="f3988-103">Felsorolja a HDInsight-fürt állomásait.</span><span class="sxs-lookup"><span data-stu-id="f3988-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="f3988-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3988-104">SYNTAX</span></span>

### <span data-ttu-id="f3988-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3988-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3988-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3988-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3988-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3988-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3988-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3988-108">DESCRIPTION</span></span>
<span data-ttu-id="f3988-109">A **Get-AzHDInsightHost** parancsmag felsorolja a HDInsight-fürt állomásait.</span><span class="sxs-lookup"><span data-stu-id="f3988-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="f3988-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f3988-110">EXAMPLES</span></span>

### <span data-ttu-id="f3988-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3988-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="f3988-112">Ez a parancs a fürtöket tároló állomásokat tároló fürtöket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f3988-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="f3988-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f3988-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="f3988-114">Ez a parancs a fürtöket tároló állomásokat tartalmazó listákat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f3988-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="f3988-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3988-115">PARAMETERS</span></span>

### <span data-ttu-id="f3988-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="f3988-116">-ClusterName</span></span>
<span data-ttu-id="f3988-117">A fürt nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="f3988-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="f3988-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3988-118">-DefaultProfile</span></span>
<span data-ttu-id="f3988-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3988-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3988-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3988-120">-InputObject</span></span>
<span data-ttu-id="f3988-121">A beviteli objektum beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="f3988-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="f3988-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3988-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3988-123">Az erőforráscsoport nevének beolvasása vagy megadására szolgáló parancs.</span><span class="sxs-lookup"><span data-stu-id="f3988-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="f3988-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3988-124">-ResourceId</span></span>
<span data-ttu-id="f3988-125">Az erőforrás azonosítóját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="f3988-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="f3988-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3988-126">CommonParameters</span></span>
<span data-ttu-id="f3988-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3988-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3988-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3988-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3988-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3988-129">INPUTS</span></span>

### <span data-ttu-id="f3988-130">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f3988-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f3988-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3988-131">OUTPUTS</span></span>

### <span data-ttu-id="f3988-132">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="f3988-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="f3988-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3988-133">NOTES</span></span>

## <span data-ttu-id="f3988-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3988-134">RELATED LINKS</span></span>
