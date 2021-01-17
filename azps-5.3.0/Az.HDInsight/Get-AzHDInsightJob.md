---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: dc7f69ef29d7e5396ad57346380decc672f83db5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469693"
---
# <span data-ttu-id="b7764-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b7764-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="b7764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7764-102">SYNOPSIS</span></span>
<span data-ttu-id="b7764-103">Beolvassa a feladatok listáját egy fürtből, és fordított időrendi sorrendben listázza őket, vagy lekér egy adott feladatot.</span><span class="sxs-lookup"><span data-stu-id="b7764-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="b7764-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7764-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7764-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7764-105">DESCRIPTION</span></span>
<span data-ttu-id="b7764-106">A **Get-AzHDInsight Jobs** parancsmag fordított időrendi sorrendben kapja meg egy adott Azure HDInsight-fürt legutóbbi feladatokat, a lista tetején pedig a legújabb feladat szerepel.</span><span class="sxs-lookup"><span data-stu-id="b7764-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="b7764-107">A JobId paraméter megadva *adott feladatot kap.*</span><span class="sxs-lookup"><span data-stu-id="b7764-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="b7764-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7764-108">EXAMPLES</span></span>

### <span data-ttu-id="b7764-109">1. példa: Legutóbbi feladatok lekérte egy adott Azure HDInsight-fürthöz</span><span class="sxs-lookup"><span data-stu-id="b7764-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b7764-110">Ez a parancs a -hadoop-001 nevű fürt összes legutóbbi munkáját beveszi.</span><span class="sxs-lookup"><span data-stu-id="b7764-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b7764-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7764-111">PARAMETERS</span></span>

### <span data-ttu-id="b7764-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7764-112">-ClusterName</span></span>
<span data-ttu-id="b7764-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7764-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b7764-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7764-114">-DefaultProfile</span></span>
<span data-ttu-id="b7764-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7764-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7764-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b7764-116">-HttpCredential</span></span>
<span data-ttu-id="b7764-117">A fürt bejelentkezési (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="b7764-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="b7764-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="b7764-118">-JobId</span></span>
<span data-ttu-id="b7764-119">A lekért feladat feladatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7764-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="b7764-120">-NumOfFeladats</span><span class="sxs-lookup"><span data-stu-id="b7764-120">-NumOfJobs</span></span>
<span data-ttu-id="b7764-121">A beolvassa a beolvassa feladatok számát.</span><span class="sxs-lookup"><span data-stu-id="b7764-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="b7764-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7764-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7764-123">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7764-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b7764-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7764-124">CommonParameters</span></span>
<span data-ttu-id="b7764-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7764-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7764-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7764-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7764-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7764-127">INPUTS</span></span>

### <span data-ttu-id="b7764-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="b7764-128">None</span></span>

## <span data-ttu-id="b7764-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7764-129">OUTPUTS</span></span>

### <span data-ttu-id="b7764-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b7764-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="b7764-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7764-131">NOTES</span></span>

## <span data-ttu-id="b7764-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7764-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7764-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b7764-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="b7764-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b7764-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="b7764-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b7764-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="b7764-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b7764-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


