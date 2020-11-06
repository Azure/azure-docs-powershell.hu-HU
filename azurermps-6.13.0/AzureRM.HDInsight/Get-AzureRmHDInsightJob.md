---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: 1fb2ee80a6dafb005509265e6012380eebf5abd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496147"
---
# <span data-ttu-id="a0176-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a0176-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="a0176-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0176-102">SYNOPSIS</span></span>
<span data-ttu-id="a0176-103">Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.</span><span class="sxs-lookup"><span data-stu-id="a0176-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0176-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0176-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0176-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0176-105">DESCRIPTION</span></span>
<span data-ttu-id="a0176-106">A **Get-AzureRmHDInsightJob** parancsmag a kijelölt Azure HDInsight-fürtök legutóbbi feladatait fordított időrendi sorrendben kapja meg, a lista tetején lévő legutóbbi munkával.</span><span class="sxs-lookup"><span data-stu-id="a0176-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="a0176-107">Adjon meg egy konkrét feladatot a *JobId* paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="a0176-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="a0176-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a0176-108">EXAMPLES</span></span>

### <span data-ttu-id="a0176-109">1. példa: a legutóbbi feladatok beszerzése egy megadott Azure HDInsight-fürthöz</span><span class="sxs-lookup"><span data-stu-id="a0176-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="a0176-110">Ez a parancs a-Hadoop-001 nevű fürt legutóbbi feladatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0176-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a0176-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0176-111">PARAMETERS</span></span>

### <span data-ttu-id="a0176-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="a0176-112">-ClusterName</span></span>
<span data-ttu-id="a0176-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0176-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a0176-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0176-114">-DefaultProfile</span></span>
<span data-ttu-id="a0176-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0176-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0176-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a0176-116">-HttpCredential</span></span>
<span data-ttu-id="a0176-117">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="a0176-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="a0176-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="a0176-118">-JobId</span></span>
<span data-ttu-id="a0176-119">A felvenni kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0176-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0176-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="a0176-120">-NumOfJobs</span></span>
<span data-ttu-id="a0176-121">A lekérdezni kívánt feladatok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0176-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="a0176-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0176-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0176-123">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0176-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a0176-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0176-124">CommonParameters</span></span>
<span data-ttu-id="a0176-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0176-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0176-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0176-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0176-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0176-127">INPUTS</span></span>

### <span data-ttu-id="a0176-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="a0176-128">None</span></span>

## <span data-ttu-id="a0176-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0176-129">OUTPUTS</span></span>

### <span data-ttu-id="a0176-130">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a0176-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="a0176-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0176-131">NOTES</span></span>

## <span data-ttu-id="a0176-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0176-132">RELATED LINKS</span></span>

[<span data-ttu-id="a0176-133">Új – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0176-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="a0176-134">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a0176-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="a0176-135">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a0176-135">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="a0176-136">Várjon-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a0176-136">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


