---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 94bd90b644b12723a36266dea34d9b5e9417b45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496144"
---
# <span data-ttu-id="07523-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="07523-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="07523-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07523-102">SYNOPSIS</span></span>
<span data-ttu-id="07523-103">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="07523-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07523-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07523-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07523-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07523-105">DESCRIPTION</span></span>
<span data-ttu-id="07523-106">A **Get-AzureRmHDInsightJobOutput** parancsmag az Azure HDInsight-fürtökhez társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="07523-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="07523-107">Példák</span><span class="sxs-lookup"><span data-stu-id="07523-107">EXAMPLES</span></span>

### <span data-ttu-id="07523-108">Példa 1: a napló kimenetének beolvasása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="07523-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="07523-109">Ez a parancs a Hadoop-001 nevű fürtből kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="07523-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="07523-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07523-110">PARAMETERS</span></span>

### <span data-ttu-id="07523-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="07523-111">-ClusterName</span></span>
<span data-ttu-id="07523-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07523-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="07523-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="07523-113">-DefaultContainer</span></span>
<span data-ttu-id="07523-114">Az alapértelmezett tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07523-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="07523-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07523-115">-DefaultProfile</span></span>
<span data-ttu-id="07523-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="07523-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07523-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="07523-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="07523-118">Az alapértelmezett tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07523-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="07523-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="07523-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="07523-120">Az alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07523-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="07523-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="07523-121">-DisplayOutputType</span></span>
<span data-ttu-id="07523-122">A kért munkahelyi kimeneti típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="07523-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="07523-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="07523-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07523-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="07523-124">StandardOutput</span></span>
- <span data-ttu-id="07523-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="07523-125">StandardError</span></span>

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

### <span data-ttu-id="07523-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="07523-126">-HttpCredential</span></span>
<span data-ttu-id="07523-127">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="07523-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="07523-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="07523-128">-JobId</span></span>
<span data-ttu-id="07523-129">Annak a projektnek az AZONOSÍTÓját adja meg, amelynek a kimenetét le fogja olvasni.</span><span class="sxs-lookup"><span data-stu-id="07523-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="07523-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07523-130">-ResourceGroupName</span></span>
<span data-ttu-id="07523-131">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07523-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="07523-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07523-132">CommonParameters</span></span>
<span data-ttu-id="07523-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07523-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07523-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07523-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07523-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07523-135">INPUTS</span></span>

### <span data-ttu-id="07523-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="07523-136">None</span></span>

## <span data-ttu-id="07523-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07523-137">OUTPUTS</span></span>

### <span data-ttu-id="07523-138">System. String</span><span class="sxs-lookup"><span data-stu-id="07523-138">System.String</span></span>

## <span data-ttu-id="07523-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07523-139">NOTES</span></span>

## <span data-ttu-id="07523-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07523-140">RELATED LINKS</span></span>

[<span data-ttu-id="07523-141">Új – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="07523-141">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="07523-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="07523-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


