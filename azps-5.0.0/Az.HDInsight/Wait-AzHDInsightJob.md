---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187824"
---
# <span data-ttu-id="ea233-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea233-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="ea233-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea233-102">SYNOPSIS</span></span>
<span data-ttu-id="ea233-103">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="ea233-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="ea233-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea233-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea233-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea233-105">DESCRIPTION</span></span>
<span data-ttu-id="ea233-106">A **WAIT-AzHDInsightJob** parancsmag várja az Azure HDInsight-feladatok befejezését vagy hibáját.</span><span class="sxs-lookup"><span data-stu-id="ea233-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="ea233-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ea233-107">EXAMPLES</span></span>

### <span data-ttu-id="ea233-108">Példa 1: várakozás a feladat befejezésére vagy hibájának megtartására</span><span class="sxs-lookup"><span data-stu-id="ea233-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="ea233-109">A parancs megvárja a feladatok befejezését vagy kudarcát.</span><span class="sxs-lookup"><span data-stu-id="ea233-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="ea233-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea233-110">PARAMETERS</span></span>

### <span data-ttu-id="ea233-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="ea233-111">-ClusterName</span></span>
<span data-ttu-id="ea233-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea233-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ea233-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea233-113">-DefaultProfile</span></span>
<span data-ttu-id="ea233-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ea233-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea233-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ea233-115">-HttpCredential</span></span>
<span data-ttu-id="ea233-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="ea233-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ea233-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="ea233-117">-JobId</span></span>
<span data-ttu-id="ea233-118">A feladat munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea233-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="ea233-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea233-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea233-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea233-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ea233-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="ea233-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="ea233-122">A munkavégzés befejezéséhez szükséges teljes idő másodpercben.</span><span class="sxs-lookup"><span data-stu-id="ea233-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="ea233-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ea233-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="ea233-124">A feladatok állapotának ellenőrzése között eltelt idő másodpercben.</span><span class="sxs-lookup"><span data-stu-id="ea233-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="ea233-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea233-125">CommonParameters</span></span>
<span data-ttu-id="ea233-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea233-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea233-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea233-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea233-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea233-128">INPUTS</span></span>

### <span data-ttu-id="ea233-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ea233-129">System.String</span></span>

## <span data-ttu-id="ea233-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea233-130">OUTPUTS</span></span>

### <span data-ttu-id="ea233-131">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea233-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="ea233-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea233-132">NOTES</span></span>

## <span data-ttu-id="ea233-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea233-133">RELATED LINKS</span></span>

[<span data-ttu-id="ea233-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea233-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="ea233-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea233-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="ea233-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea233-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

