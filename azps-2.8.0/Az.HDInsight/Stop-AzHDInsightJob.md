---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: f2c162427abc1a05c7680e0fc19e0d2406c3e4a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666325"
---
# <span data-ttu-id="2d61d-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2d61d-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="2d61d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d61d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d61d-103">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="2d61d-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="2d61d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d61d-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d61d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d61d-105">DESCRIPTION</span></span>
<span data-ttu-id="2d61d-106">A **stop-AzHDInsightJob** parancsmag az Azure HDInsight-fürtökben meghatározott futási feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="2d61d-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2d61d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d61d-107">EXAMPLES</span></span>

### <span data-ttu-id="2d61d-108">Példa 1: feladat leállítása a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="2d61d-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="2d61d-109">Ez a parancs a Hadoop-001 nevű fürtben leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="2d61d-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2d61d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d61d-110">PARAMETERS</span></span>

### <span data-ttu-id="2d61d-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="2d61d-111">-ClusterName</span></span>
<span data-ttu-id="2d61d-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d61d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2d61d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d61d-113">-DefaultProfile</span></span>
<span data-ttu-id="2d61d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d61d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d61d-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2d61d-115">-HttpCredential</span></span>
<span data-ttu-id="2d61d-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="2d61d-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2d61d-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2d61d-117">-JobId</span></span>
<span data-ttu-id="2d61d-118">A feladat munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d61d-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d61d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d61d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d61d-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d61d-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2d61d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d61d-121">CommonParameters</span></span>
<span data-ttu-id="2d61d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d61d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d61d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d61d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d61d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d61d-124">INPUTS</span></span>

### <span data-ttu-id="2d61d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2d61d-125">System.String</span></span>

## <span data-ttu-id="2d61d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d61d-126">OUTPUTS</span></span>

### <span data-ttu-id="2d61d-127">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2d61d-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2d61d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d61d-128">NOTES</span></span>

## <span data-ttu-id="2d61d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d61d-129">RELATED LINKS</span></span>

[<span data-ttu-id="2d61d-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2d61d-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="2d61d-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2d61d-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="2d61d-132">Várjon-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2d61d-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


