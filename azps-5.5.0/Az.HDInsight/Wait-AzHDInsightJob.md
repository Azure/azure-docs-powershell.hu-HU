---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4c1d991d3236c8e631b2b5c7f0026e91af2f8cf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153082"
---
# <span data-ttu-id="751c9-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="751c9-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="751c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="751c9-102">SYNOPSIS</span></span>
<span data-ttu-id="751c9-103">Megvárja egy adott feladat elvégzését vagy sikertelenségét.</span><span class="sxs-lookup"><span data-stu-id="751c9-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="751c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="751c9-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="751c9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="751c9-105">DESCRIPTION</span></span>
<span data-ttu-id="751c9-106">A **Wait-AzHDInsight Job** parancsmag az Azure HDInsight-feladat befejezésére vagy sikertelenségére vár.</span><span class="sxs-lookup"><span data-stu-id="751c9-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="751c9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="751c9-107">EXAMPLES</span></span>

### <span data-ttu-id="751c9-108">1. példa: Várakozás a feladat elvégzésére vagy sikertelenségére</span><span class="sxs-lookup"><span data-stu-id="751c9-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="751c9-109">Ez a parancs a feladat elvégzésére vagy sikertelenségére vár.</span><span class="sxs-lookup"><span data-stu-id="751c9-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="751c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="751c9-110">PARAMETERS</span></span>

### <span data-ttu-id="751c9-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="751c9-111">-ClusterName</span></span>
<span data-ttu-id="751c9-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="751c9-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="751c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751c9-113">-DefaultProfile</span></span>
<span data-ttu-id="751c9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="751c9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="751c9-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="751c9-115">-HttpCredential</span></span>
<span data-ttu-id="751c9-116">A fürt bejelentkezési (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="751c9-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="751c9-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="751c9-117">-JobId</span></span>
<span data-ttu-id="751c9-118">A feladat feladatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="751c9-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="751c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="751c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="751c9-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="751c9-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="751c9-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="751c9-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="751c9-122">A munkára való várakozás teljes ideje másodpercben.</span><span class="sxs-lookup"><span data-stu-id="751c9-122">The total time to wait for job completion, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751c9-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="751c9-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="751c9-124">A feladatállapot-ellenőrzések közötti várakozási idő másodpercben.</span><span class="sxs-lookup"><span data-stu-id="751c9-124">The time to wait between job status checks, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751c9-125">CommonParameters</span></span>
<span data-ttu-id="751c9-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="751c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="751c9-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="751c9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751c9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="751c9-128">INPUTS</span></span>

### <span data-ttu-id="751c9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="751c9-129">System.String</span></span>

## <span data-ttu-id="751c9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="751c9-130">OUTPUTS</span></span>

### <span data-ttu-id="751c9-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="751c9-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="751c9-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="751c9-132">NOTES</span></span>

## <span data-ttu-id="751c9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="751c9-133">RELATED LINKS</span></span>

[<span data-ttu-id="751c9-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="751c9-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="751c9-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="751c9-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="751c9-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="751c9-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


