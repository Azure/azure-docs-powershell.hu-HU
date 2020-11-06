---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: de7df9417e617f88c61e75c64dd42f32b83fc66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497464"
---
# <span data-ttu-id="81215-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81215-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="81215-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81215-102">SYNOPSIS</span></span>
<span data-ttu-id="81215-103">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="81215-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81215-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81215-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81215-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81215-105">DESCRIPTION</span></span>
<span data-ttu-id="81215-106">A **WAIT-AzureRmHDInsightJob** parancsmag várja az Azure HDInsight-feladatok befejezését vagy hibáját.</span><span class="sxs-lookup"><span data-stu-id="81215-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="81215-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81215-107">EXAMPLES</span></span>

### <span data-ttu-id="81215-108">Példa 1: várakozás a feladat befejezésére vagy hibájának megtartására</span><span class="sxs-lookup"><span data-stu-id="81215-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="81215-109">A parancs megvárja a feladatok befejezését vagy kudarcát.</span><span class="sxs-lookup"><span data-stu-id="81215-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="81215-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81215-110">PARAMETERS</span></span>

### <span data-ttu-id="81215-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="81215-111">-ClusterName</span></span>
<span data-ttu-id="81215-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81215-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="81215-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81215-113">-DefaultProfile</span></span>
<span data-ttu-id="81215-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="81215-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81215-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="81215-115">-HttpCredential</span></span>
<span data-ttu-id="81215-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="81215-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="81215-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="81215-117">-JobId</span></span>
<span data-ttu-id="81215-118">A feladat munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="81215-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="81215-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81215-119">-ResourceGroupName</span></span>
<span data-ttu-id="81215-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81215-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="81215-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="81215-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="81215-122">A munkavégzés befejezéséhez szükséges teljes idő másodpercben.</span><span class="sxs-lookup"><span data-stu-id="81215-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="81215-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="81215-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="81215-124">A feladatok állapotának ellenőrzése között eltelt idő másodpercben.</span><span class="sxs-lookup"><span data-stu-id="81215-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="81215-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81215-125">CommonParameters</span></span>
<span data-ttu-id="81215-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81215-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81215-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81215-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81215-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81215-128">INPUTS</span></span>

### <span data-ttu-id="81215-129">System. String</span><span class="sxs-lookup"><span data-stu-id="81215-129">System.String</span></span>
<span data-ttu-id="81215-130">Paraméterek: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="81215-130">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="81215-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81215-131">OUTPUTS</span></span>

### <span data-ttu-id="81215-132">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81215-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="81215-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81215-133">NOTES</span></span>

## <span data-ttu-id="81215-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81215-134">RELATED LINKS</span></span>

[<span data-ttu-id="81215-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81215-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="81215-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81215-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="81215-137">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81215-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


