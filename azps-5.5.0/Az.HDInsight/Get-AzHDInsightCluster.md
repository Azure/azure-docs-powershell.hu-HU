---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155587"
---
# <span data-ttu-id="fc861-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fc861-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="fc861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc861-102">SYNOPSIS</span></span>
<span data-ttu-id="fc861-103">Beolvassa és felsorolja az aktuális előfizetéshez vagy adott erőforráscsoporthoz társított Összes Azure HDInsight-fürtöt, illetve lekér egy adott fürtöt.</span><span class="sxs-lookup"><span data-stu-id="fc861-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="fc861-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc861-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc861-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc861-105">DESCRIPTION</span></span>
<span data-ttu-id="fc861-106">A **Get-AzHDInsightCluster** parancsmag felsorolja az aktuális előfizetés Azure HDInsight szolgáltatáscsoportját.</span><span class="sxs-lookup"><span data-stu-id="fc861-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="fc861-107">Egy adott *fürt részleteinek* lekérdezéséhez használja a ClusterName paramétert.</span><span class="sxs-lookup"><span data-stu-id="fc861-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="fc861-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc861-108">EXAMPLES</span></span>

### <span data-ttu-id="fc861-109">1. példa: Az összes Azure HDInsight-fürt felsorolása</span><span class="sxs-lookup"><span data-stu-id="fc861-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="fc861-110">Ez a parancs felsorolja az összes Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="fc861-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="fc861-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc861-111">PARAMETERS</span></span>

### <span data-ttu-id="fc861-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fc861-112">-ClusterName</span></span>
<span data-ttu-id="fc861-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc861-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="fc861-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc861-114">-DefaultProfile</span></span>
<span data-ttu-id="fc861-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fc861-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc861-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc861-116">-ResourceGroupName</span></span>
<span data-ttu-id="fc861-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc861-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fc861-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc861-118">CommonParameters</span></span>
<span data-ttu-id="fc861-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc861-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc861-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc861-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc861-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc861-121">INPUTS</span></span>

### <span data-ttu-id="fc861-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="fc861-122">None</span></span>

## <span data-ttu-id="fc861-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc861-123">OUTPUTS</span></span>

### <span data-ttu-id="fc861-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fc861-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="fc861-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc861-125">NOTES</span></span>

## <span data-ttu-id="fc861-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc861-126">RELATED LINKS</span></span>

[<span data-ttu-id="fc861-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fc861-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="fc861-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fc861-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


