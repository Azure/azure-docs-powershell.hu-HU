---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296291"
---
# <span data-ttu-id="4ccf5-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4ccf5-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="4ccf5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ccf5-102">SYNOPSIS</span></span>
<span data-ttu-id="4ccf5-103">Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="4ccf5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ccf5-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ccf5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ccf5-105">DESCRIPTION</span></span>
<span data-ttu-id="4ccf5-106">A **Start-AzHDInsightJob** parancsmag egy meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="4ccf5-107">Ez lehet egy MapReduce-feladat, egy adatfolyam-MapReduce feladat, egy kaptár vagy egy sertés-feladat.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="4ccf5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4ccf5-108">EXAMPLES</span></span>

### <span data-ttu-id="4ccf5-109">Példa 1: feladat indítása a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="4ccf5-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="4ccf5-110">Ez a parancs elindítja a feladatot a Hadoop-001 nevű fürtben.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4ccf5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ccf5-111">PARAMETERS</span></span>

### <span data-ttu-id="4ccf5-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="4ccf5-112">-ClusterName</span></span>
<span data-ttu-id="4ccf5-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4ccf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ccf5-114">-DefaultProfile</span></span>
<span data-ttu-id="4ccf5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ccf5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ccf5-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4ccf5-116">-HttpCredential</span></span>
<span data-ttu-id="4ccf5-117">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4ccf5-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="4ccf5-118">-JobDefinition</span></span>
<span data-ttu-id="4ccf5-119">Itt adhatja meg az Azure HDInsight-fürtben való indulási feladatot.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="4ccf5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ccf5-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ccf5-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4ccf5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ccf5-122">CommonParameters</span></span>
<span data-ttu-id="4ccf5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ccf5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ccf5-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ccf5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ccf5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ccf5-125">INPUTS</span></span>

### <span data-ttu-id="4ccf5-126">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4ccf5-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="4ccf5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ccf5-127">OUTPUTS</span></span>

### <span data-ttu-id="4ccf5-128">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4ccf5-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="4ccf5-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ccf5-129">NOTES</span></span>

## <span data-ttu-id="4ccf5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ccf5-130">RELATED LINKS</span></span>

[<span data-ttu-id="4ccf5-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4ccf5-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="4ccf5-132">Új – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4ccf5-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="4ccf5-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4ccf5-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="4ccf5-134">Várjon-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4ccf5-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


