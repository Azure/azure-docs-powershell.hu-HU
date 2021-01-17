---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: ad2060a399b5781e18c9d8b7fc1c8a37b5d467b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469649"
---
# <span data-ttu-id="b1696-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b1696-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="b1696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1696-102">SYNOPSIS</span></span>
<span data-ttu-id="b1696-103">Egy megadott Azure HDInsight-feladatot kezd egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="b1696-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="b1696-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1696-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1696-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1696-105">DESCRIPTION</span></span>
<span data-ttu-id="b1696-106">A **Start-AzHDInsight Job** parancsmag elindít egy definiált Azure HDInsight-feladatot egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="b1696-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="b1696-107">Ez lehet MapReduce-feladat, Streaming MapReduce-feladat, Kaptár- vagy Vírusfólejátszási feladat.</span><span class="sxs-lookup"><span data-stu-id="b1696-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="b1696-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1696-108">EXAMPLES</span></span>

### <span data-ttu-id="b1696-109">1. példa: Feladat kezdése a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="b1696-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b1696-110">Ez a parancs elindít egy feladatot a "-hadoop-001" nevű fürtben.</span><span class="sxs-lookup"><span data-stu-id="b1696-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b1696-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1696-111">PARAMETERS</span></span>

### <span data-ttu-id="b1696-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b1696-112">-ClusterName</span></span>
<span data-ttu-id="b1696-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1696-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b1696-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1696-114">-DefaultProfile</span></span>
<span data-ttu-id="b1696-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b1696-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1696-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b1696-116">-HttpCredential</span></span>
<span data-ttu-id="b1696-117">A fürt bejelentkezési (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="b1696-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1696-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="b1696-118">-JobDefinition</span></span>
<span data-ttu-id="b1696-119">Az Azure HDInsight-fürt indítási feladatának megadása.</span><span class="sxs-lookup"><span data-stu-id="b1696-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1696-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1696-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1696-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1696-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b1696-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1696-122">CommonParameters</span></span>
<span data-ttu-id="b1696-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1696-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1696-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1696-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1696-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1696-125">INPUTS</span></span>

### <span data-ttu-id="b1696-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b1696-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="b1696-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1696-127">OUTPUTS</span></span>

### <span data-ttu-id="b1696-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b1696-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="b1696-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1696-129">NOTES</span></span>

## <span data-ttu-id="b1696-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1696-130">RELATED LINKS</span></span>

[<span data-ttu-id="b1696-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b1696-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="b1696-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b1696-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="b1696-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b1696-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="b1696-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b1696-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


