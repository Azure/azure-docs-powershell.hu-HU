---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: a4e02a10bef16fad21a44ca7952a5f2e429846d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466042"
---
# <span data-ttu-id="346a0-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="346a0-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="346a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="346a0-102">SYNOPSIS</span></span>
<span data-ttu-id="346a0-103">A parancsmaggal együtt használni kívánt Invoke-RmAzureHDInsightHiveJob kijelölése.</span><span class="sxs-lookup"><span data-stu-id="346a0-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="346a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="346a0-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="346a0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="346a0-105">DESCRIPTION</span></span>
<span data-ttu-id="346a0-106">A **Use-AzHDInsightCluster** parancsmag kiválasztja az Azure HDInsight-fürtöt a Invoke-AzHDInsightHiveJob-parancsmag számára a Hive-feladatok beküldése érdekében.</span><span class="sxs-lookup"><span data-stu-id="346a0-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="346a0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="346a0-107">EXAMPLES</span></span>

### <span data-ttu-id="346a0-108">1. példa: Fürt kiválasztása a Hive-lekérdezések beküldéséhez</span><span class="sxs-lookup"><span data-stu-id="346a0-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="346a0-109">Ez a parancs kijelöl egy fürtöt a Hive-lekérdezések beküldéséhez.</span><span class="sxs-lookup"><span data-stu-id="346a0-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="346a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="346a0-110">PARAMETERS</span></span>

### <span data-ttu-id="346a0-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="346a0-111">-ClusterName</span></span>
<span data-ttu-id="346a0-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="346a0-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="346a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346a0-113">-DefaultProfile</span></span>
<span data-ttu-id="346a0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="346a0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="346a0-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="346a0-115">-HttpCredential</span></span>
<span data-ttu-id="346a0-116">A fürt bejelentkezési (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="346a0-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="346a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="346a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="346a0-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="346a0-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="346a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346a0-119">CommonParameters</span></span>
<span data-ttu-id="346a0-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="346a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346a0-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="346a0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346a0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="346a0-122">INPUTS</span></span>

### <span data-ttu-id="346a0-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="346a0-123">None</span></span>

## <span data-ttu-id="346a0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="346a0-124">OUTPUTS</span></span>

### <span data-ttu-id="346a0-125">System.String</span><span class="sxs-lookup"><span data-stu-id="346a0-125">System.String</span></span>

## <span data-ttu-id="346a0-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="346a0-126">NOTES</span></span>

## <span data-ttu-id="346a0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="346a0-127">RELATED LINKS</span></span>

[<span data-ttu-id="346a0-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="346a0-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="346a0-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="346a0-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


