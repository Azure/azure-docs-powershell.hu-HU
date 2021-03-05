---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: c89293ee071aba3fcec2d58d071714193cc44a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010485"
---
# <span data-ttu-id="86e89-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="86e89-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="86e89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e89-102">SYNOPSIS</span></span>
<span data-ttu-id="86e89-103">Beolvassa és felsorolja az aktuális előfizetéshez vagy adott erőforráscsoporthoz társított Összes Azure HDInsight-fürtöt, illetve lekér egy adott fürtöt.</span><span class="sxs-lookup"><span data-stu-id="86e89-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="86e89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86e89-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86e89-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86e89-105">DESCRIPTION</span></span>
<span data-ttu-id="86e89-106">A **Get-AzHDInsightCluster** parancsmag felsorolja az aktuális előfizetés Azure HDInsight szolgáltatáscsoportját.</span><span class="sxs-lookup"><span data-stu-id="86e89-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="86e89-107">Egy adott *fürt részleteinek* lekérdezéséhez használja a ClusterName paramétert.</span><span class="sxs-lookup"><span data-stu-id="86e89-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="86e89-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86e89-108">EXAMPLES</span></span>

### <span data-ttu-id="86e89-109">1. példa: Az összes Azure HDInsight-fürt felsorolása</span><span class="sxs-lookup"><span data-stu-id="86e89-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="86e89-110">Ez a parancs felsorolja az összes Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="86e89-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="86e89-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86e89-111">PARAMETERS</span></span>

### <span data-ttu-id="86e89-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="86e89-112">-ClusterName</span></span>
<span data-ttu-id="86e89-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86e89-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e89-114">-DefaultProfile</span></span>
<span data-ttu-id="86e89-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86e89-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86e89-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e89-116">-ResourceGroupName</span></span>
<span data-ttu-id="86e89-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86e89-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e89-118">CommonParameters</span></span>
<span data-ttu-id="86e89-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e89-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e89-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86e89-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e89-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86e89-121">INPUTS</span></span>

### <span data-ttu-id="86e89-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="86e89-122">None</span></span>

## <span data-ttu-id="86e89-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e89-123">OUTPUTS</span></span>

### <span data-ttu-id="86e89-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="86e89-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="86e89-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86e89-125">NOTES</span></span>

## <span data-ttu-id="86e89-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86e89-126">RELATED LINKS</span></span>

[<span data-ttu-id="86e89-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="86e89-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="86e89-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="86e89-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


