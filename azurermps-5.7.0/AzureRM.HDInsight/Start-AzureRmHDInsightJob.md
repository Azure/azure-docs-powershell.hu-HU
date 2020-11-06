---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504571"
---
# <span data-ttu-id="0be5d-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0be5d-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="0be5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0be5d-102">SYNOPSIS</span></span>
<span data-ttu-id="0be5d-103">Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="0be5d-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0be5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0be5d-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0be5d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0be5d-105">DESCRIPTION</span></span>
<span data-ttu-id="0be5d-106">A **Start-AzureRMHDInsightJob** parancsmag egy meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="0be5d-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="0be5d-107">Ez lehet egy MapReduce-feladat, egy adatfolyam-MapReduce feladat, egy kaptár vagy egy sertés-feladat.</span><span class="sxs-lookup"><span data-stu-id="0be5d-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="0be5d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0be5d-108">EXAMPLES</span></span>

### <span data-ttu-id="0be5d-109">Példa 1: feladat indítása a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="0be5d-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0be5d-110">Ez a parancs elindítja a feladatot a Hadoop-001 nevű fürtben.</span><span class="sxs-lookup"><span data-stu-id="0be5d-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0be5d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0be5d-111">PARAMETERS</span></span>

### <span data-ttu-id="0be5d-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="0be5d-112">-ClusterName</span></span>
<span data-ttu-id="0be5d-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0be5d-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be5d-114">-DefaultProfile</span></span>
<span data-ttu-id="0be5d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0be5d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be5d-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0be5d-116">-HttpCredential</span></span>
<span data-ttu-id="0be5d-117">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="0be5d-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be5d-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="0be5d-118">-JobDefinition</span></span>
<span data-ttu-id="0be5d-119">Itt adhatja meg az Azure HDInsight-fürtben való indulási feladatot.</span><span class="sxs-lookup"><span data-stu-id="0be5d-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0be5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0be5d-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0be5d-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be5d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be5d-122">CommonParameters</span></span>
<span data-ttu-id="0be5d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0be5d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be5d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0be5d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be5d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0be5d-125">INPUTS</span></span>

### <span data-ttu-id="0be5d-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0be5d-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="0be5d-127">A ' JobDefinition ' paraméter az "AzureHDInsightJobDefinition" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0be5d-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="0be5d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0be5d-128">OUTPUTS</span></span>

### <span data-ttu-id="0be5d-129">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0be5d-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="0be5d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0be5d-130">NOTES</span></span>

## <span data-ttu-id="0be5d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0be5d-131">RELATED LINKS</span></span>

[<span data-ttu-id="0be5d-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0be5d-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="0be5d-133">Új – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0be5d-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="0be5d-134">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0be5d-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="0be5d-135">Várjon-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0be5d-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


