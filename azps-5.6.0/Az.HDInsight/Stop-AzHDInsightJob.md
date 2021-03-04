---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: 26572b942671bcfca9fc52d2a93da29d55405b18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931874"
---
# <span data-ttu-id="72f1a-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="72f1a-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="72f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="72f1a-103">Leállít egy megadott futó feladatot egy fürtön.</span><span class="sxs-lookup"><span data-stu-id="72f1a-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="72f1a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72f1a-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72f1a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="72f1a-106">A **Stop-AzHDInsight Job** parancsmag leállít egy megadott futó feladatot egy Azure HDInsight-fürtben.</span><span class="sxs-lookup"><span data-stu-id="72f1a-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="72f1a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="72f1a-108">1. példa: Feladat leállítása a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="72f1a-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="72f1a-109">Ez a parancs leállítja a feladatot a -hadoop-001 nevű fürtben.</span><span class="sxs-lookup"><span data-stu-id="72f1a-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="72f1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="72f1a-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="72f1a-111">-ClusterName</span></span>
<span data-ttu-id="72f1a-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72f1a-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="72f1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f1a-113">-DefaultProfile</span></span>
<span data-ttu-id="72f1a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="72f1a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72f1a-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="72f1a-115">-HttpCredential</span></span>
<span data-ttu-id="72f1a-116">A fürt bejelentkezési (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="72f1a-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="72f1a-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="72f1a-117">-JobId</span></span>
<span data-ttu-id="72f1a-118">A feladat feladatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72f1a-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="72f1a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f1a-119">-ResourceGroupName</span></span>
<span data-ttu-id="72f1a-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72f1a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="72f1a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f1a-121">CommonParameters</span></span>
<span data-ttu-id="72f1a-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f1a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f1a-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72f1a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f1a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72f1a-124">INPUTS</span></span>

### <span data-ttu-id="72f1a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="72f1a-125">System.String</span></span>

## <span data-ttu-id="72f1a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72f1a-126">OUTPUTS</span></span>

### <span data-ttu-id="72f1a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="72f1a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="72f1a-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72f1a-128">NOTES</span></span>

## <span data-ttu-id="72f1a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72f1a-129">RELATED LINKS</span></span>

[<span data-ttu-id="72f1a-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="72f1a-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="72f1a-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="72f1a-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="72f1a-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="72f1a-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


