---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: d5e38cf3edb89801b630735dee1ce0dbd1d62d41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846270"
---
# <span data-ttu-id="89529-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89529-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="89529-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89529-102">SYNOPSIS</span></span>
<span data-ttu-id="89529-103">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="89529-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="89529-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89529-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89529-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89529-105">DESCRIPTION</span></span>
<span data-ttu-id="89529-106">A **stop-AzHDInsightJob** parancsmag az Azure HDInsight-fürtökben meghatározott futási feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="89529-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="89529-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89529-107">EXAMPLES</span></span>

### <span data-ttu-id="89529-108">Példa 1: feladat leállítása a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="89529-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="89529-109">Ez a parancs a Hadoop-001 nevű fürtben leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="89529-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="89529-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89529-110">PARAMETERS</span></span>

### <span data-ttu-id="89529-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="89529-111">-ClusterName</span></span>
<span data-ttu-id="89529-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89529-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="89529-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89529-113">-DefaultProfile</span></span>
<span data-ttu-id="89529-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="89529-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89529-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="89529-115">-HttpCredential</span></span>
<span data-ttu-id="89529-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="89529-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="89529-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="89529-117">-JobId</span></span>
<span data-ttu-id="89529-118">A feladat munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="89529-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="89529-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89529-119">-ResourceGroupName</span></span>
<span data-ttu-id="89529-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89529-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="89529-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89529-121">CommonParameters</span></span>
<span data-ttu-id="89529-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89529-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89529-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89529-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89529-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89529-124">INPUTS</span></span>

### <span data-ttu-id="89529-125">System. String</span><span class="sxs-lookup"><span data-stu-id="89529-125">System.String</span></span>

## <span data-ttu-id="89529-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89529-126">OUTPUTS</span></span>

### <span data-ttu-id="89529-127">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89529-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="89529-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89529-128">NOTES</span></span>

## <span data-ttu-id="89529-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89529-129">RELATED LINKS</span></span>

[<span data-ttu-id="89529-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89529-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="89529-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89529-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="89529-132">Várjon-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89529-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


