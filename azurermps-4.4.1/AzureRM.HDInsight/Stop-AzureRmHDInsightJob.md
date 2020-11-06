---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 674c8f1cb5fdf8d8c76da36a7bb6d8df06e29c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504968"
---
# <span data-ttu-id="ab15d-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ab15d-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="ab15d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab15d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab15d-103">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="ab15d-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab15d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab15d-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab15d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab15d-105">DESCRIPTION</span></span>
<span data-ttu-id="ab15d-106">A **stop-AzureRmHDInsightJob** parancsmag az Azure HDInsight-fürtökben meghatározott futási feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="ab15d-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ab15d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ab15d-107">EXAMPLES</span></span>

### <span data-ttu-id="ab15d-108">Példa 1: feladat leállítása a megadott fürtön</span><span class="sxs-lookup"><span data-stu-id="ab15d-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="ab15d-109">Ez a parancs a Hadoop-001 nevű fürtben leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="ab15d-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ab15d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab15d-110">PARAMETERS</span></span>

### <span data-ttu-id="ab15d-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="ab15d-111">-ClusterName</span></span>
<span data-ttu-id="ab15d-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab15d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ab15d-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ab15d-113">-HttpCredential</span></span>
<span data-ttu-id="ab15d-114">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="ab15d-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ab15d-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="ab15d-115">-JobId</span></span>
<span data-ttu-id="ab15d-116">A feladat munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab15d-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="ab15d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab15d-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab15d-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab15d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ab15d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab15d-119">-DefaultProfile</span></span>
<span data-ttu-id="ab15d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab15d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab15d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab15d-121">CommonParameters</span></span>
<span data-ttu-id="ab15d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab15d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab15d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab15d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab15d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab15d-124">INPUTS</span></span>

### <span data-ttu-id="ab15d-125">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="ab15d-125">String</span></span>
<span data-ttu-id="ab15d-126">A ' JobId ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ab15d-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ab15d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab15d-127">OUTPUTS</span></span>

### <span data-ttu-id="ab15d-128">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ab15d-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="ab15d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab15d-129">NOTES</span></span>

## <span data-ttu-id="ab15d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab15d-130">RELATED LINKS</span></span>

[<span data-ttu-id="ab15d-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ab15d-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="ab15d-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ab15d-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="ab15d-133">Várjon-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ab15d-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


