---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 7247a4f5e23bc4f0f3c520f909cec221ee03e1ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495117"
---
# <span data-ttu-id="041f0-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="041f0-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="041f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="041f0-102">SYNOPSIS</span></span>
<span data-ttu-id="041f0-103">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="041f0-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="041f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="041f0-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="041f0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="041f0-105">DESCRIPTION</span></span>
<span data-ttu-id="041f0-106">A **stop-AzureRmHDInsightJob** parancsmag az Azure HDInsight-fürtökben meghatározott futási feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="041f0-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="041f0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="041f0-107">EXAMPLES</span></span>

### <span data-ttu-id="041f0-108">Példa 1: feladat leállítása a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="041f0-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="041f0-109">Ez a parancs a Hadoop-001 nevű fürtben leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="041f0-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="041f0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="041f0-110">PARAMETERS</span></span>

### <span data-ttu-id="041f0-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="041f0-111">-ClusterName</span></span>
<span data-ttu-id="041f0-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="041f0-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="041f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="041f0-113">-DefaultProfile</span></span>
<span data-ttu-id="041f0-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="041f0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="041f0-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="041f0-115">-HttpCredential</span></span>
<span data-ttu-id="041f0-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="041f0-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="041f0-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="041f0-117">-JobId</span></span>
<span data-ttu-id="041f0-118">A feladat munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="041f0-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="041f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="041f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="041f0-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="041f0-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="041f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="041f0-121">CommonParameters</span></span>
<span data-ttu-id="041f0-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="041f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="041f0-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="041f0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="041f0-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="041f0-124">INPUTS</span></span>

### <span data-ttu-id="041f0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="041f0-125">System.String</span></span>
<span data-ttu-id="041f0-126">Paraméterek: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="041f0-126">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="041f0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="041f0-127">OUTPUTS</span></span>

### <span data-ttu-id="041f0-128">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="041f0-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="041f0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="041f0-129">NOTES</span></span>

## <span data-ttu-id="041f0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="041f0-130">RELATED LINKS</span></span>

[<span data-ttu-id="041f0-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="041f0-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="041f0-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="041f0-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="041f0-133">Várjon-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="041f0-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


