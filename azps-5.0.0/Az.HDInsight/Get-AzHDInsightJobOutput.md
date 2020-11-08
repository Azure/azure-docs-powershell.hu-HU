---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 2489da10ebf1d346b147e252d6d347635efb1aff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185367"
---
# <span data-ttu-id="55e0f-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="55e0f-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="55e0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="55e0f-103">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="55e0f-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="55e0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55e0f-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55e0f-105">DESCRIPTION</span></span>
<span data-ttu-id="55e0f-106">A **Get-AzHDInsightJobOutput** parancsmag az Azure HDInsight-fürtökhez társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="55e0f-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="55e0f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55e0f-107">EXAMPLES</span></span>

### <span data-ttu-id="55e0f-108">Példa 1: a napló kimenetének beolvasása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="55e0f-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="55e0f-109">Ez a parancs a Hadoop-001 nevű fürtből kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="55e0f-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="55e0f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55e0f-110">PARAMETERS</span></span>

### <span data-ttu-id="55e0f-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="55e0f-111">-ClusterName</span></span>
<span data-ttu-id="55e0f-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55e0f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="55e0f-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="55e0f-113">-DefaultContainer</span></span>
<span data-ttu-id="55e0f-114">Az alapértelmezett tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55e0f-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="55e0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e0f-115">-DefaultProfile</span></span>
<span data-ttu-id="55e0f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="55e0f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55e0f-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="55e0f-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="55e0f-118">Az alapértelmezett tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="55e0f-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e0f-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="55e0f-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="55e0f-120">Az alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55e0f-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e0f-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="55e0f-121">-DisplayOutputType</span></span>
<span data-ttu-id="55e0f-122">A kért munkahelyi kimeneti típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="55e0f-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="55e0f-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="55e0f-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55e0f-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="55e0f-124">StandardOutput</span></span>
- <span data-ttu-id="55e0f-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="55e0f-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e0f-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="55e0f-126">-HttpCredential</span></span>
<span data-ttu-id="55e0f-127">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="55e0f-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e0f-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="55e0f-128">-JobId</span></span>
<span data-ttu-id="55e0f-129">Annak a projektnek az AZONOSÍTÓját adja meg, amelynek a kimenetét le fogja olvasni.</span><span class="sxs-lookup"><span data-stu-id="55e0f-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e0f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e0f-130">-ResourceGroupName</span></span>
<span data-ttu-id="55e0f-131">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55e0f-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="55e0f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e0f-132">CommonParameters</span></span>
<span data-ttu-id="55e0f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55e0f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e0f-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e0f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e0f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55e0f-135">INPUTS</span></span>

### <span data-ttu-id="55e0f-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="55e0f-136">None</span></span>

## <span data-ttu-id="55e0f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55e0f-137">OUTPUTS</span></span>

### <span data-ttu-id="55e0f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="55e0f-138">System.String</span></span>

## <span data-ttu-id="55e0f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55e0f-139">NOTES</span></span>

## <span data-ttu-id="55e0f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55e0f-140">RELATED LINKS</span></span>

[<span data-ttu-id="55e0f-141">Új – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="55e0f-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="55e0f-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="55e0f-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


