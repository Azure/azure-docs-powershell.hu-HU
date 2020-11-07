---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 5094d350653a766ec5656d1c571f67001821bf5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680424"
---
# <span data-ttu-id="d54fe-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d54fe-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="d54fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d54fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d54fe-103">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="d54fe-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d54fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d54fe-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d54fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d54fe-105">DESCRIPTION</span></span>
<span data-ttu-id="d54fe-106">A **WAIT-AzureRmHDInsightJob** parancsmag várja az Azure HDInsight-feladatok befejezését vagy hibáját.</span><span class="sxs-lookup"><span data-stu-id="d54fe-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="d54fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d54fe-107">EXAMPLES</span></span>

### <span data-ttu-id="d54fe-108">Példa 1: várakozás a feladat befejezésére vagy hibájának megtartására</span><span class="sxs-lookup"><span data-stu-id="d54fe-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="d54fe-109">A parancs megvárja a feladatok befejezését vagy kudarcát.</span><span class="sxs-lookup"><span data-stu-id="d54fe-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="d54fe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d54fe-110">PARAMETERS</span></span>

### <span data-ttu-id="d54fe-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="d54fe-111">-ClusterName</span></span>
<span data-ttu-id="d54fe-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d54fe-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d54fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d54fe-113">-DefaultProfile</span></span>
<span data-ttu-id="d54fe-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d54fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d54fe-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d54fe-115">-HttpCredential</span></span>
<span data-ttu-id="d54fe-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="d54fe-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="d54fe-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d54fe-117">-JobId</span></span>
<span data-ttu-id="d54fe-118">A feladat munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d54fe-118">Specifies the job ID of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d54fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d54fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="d54fe-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d54fe-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d54fe-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d54fe-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="d54fe-122">A munkavégzés befejezéséhez szükséges teljes idő másodpercben.</span><span class="sxs-lookup"><span data-stu-id="d54fe-122">The total time to wait for job completion, in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d54fe-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d54fe-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="d54fe-124">A feladatok állapotának ellenőrzése között eltelt idő másodpercben.</span><span class="sxs-lookup"><span data-stu-id="d54fe-124">The time to wait between job status checks, in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d54fe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d54fe-125">CommonParameters</span></span>
<span data-ttu-id="d54fe-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d54fe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d54fe-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d54fe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d54fe-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d54fe-128">INPUTS</span></span>

### <span data-ttu-id="d54fe-129">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="d54fe-129">String</span></span>
<span data-ttu-id="d54fe-130">A ' JobId ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d54fe-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d54fe-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d54fe-131">OUTPUTS</span></span>

### <span data-ttu-id="d54fe-132">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d54fe-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d54fe-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d54fe-133">NOTES</span></span>

## <span data-ttu-id="d54fe-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d54fe-134">RELATED LINKS</span></span>

[<span data-ttu-id="d54fe-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d54fe-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="d54fe-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d54fe-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="d54fe-137">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d54fe-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


