---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: eebbe6fb233b0d6117411973e841cf39f2ae377d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500020"
---
# <span data-ttu-id="de70c-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="de70c-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="de70c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de70c-102">SYNOPSIS</span></span>
<span data-ttu-id="de70c-103">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="de70c-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de70c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de70c-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de70c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de70c-105">DESCRIPTION</span></span>
<span data-ttu-id="de70c-106">A **Get-AzureRmHDInsightJobOutput** parancsmag az Azure HDInsight-fürtökhez társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="de70c-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="de70c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de70c-107">EXAMPLES</span></span>

### <span data-ttu-id="de70c-108">Példa 1: a napló kimenetének beolvasása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="de70c-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="de70c-109">Ez a parancs a Hadoop-001 nevű fürtből kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="de70c-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="de70c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de70c-110">PARAMETERS</span></span>

### <span data-ttu-id="de70c-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="de70c-111">-ClusterName</span></span>
<span data-ttu-id="de70c-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de70c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="de70c-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="de70c-113">-DefaultContainer</span></span>
<span data-ttu-id="de70c-114">Az alapértelmezett tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de70c-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="de70c-115">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="de70c-115">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="de70c-116">Az alapértelmezett tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="de70c-116">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="de70c-117">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="de70c-117">-DefaultStorageAccountName</span></span>
<span data-ttu-id="de70c-118">Az alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de70c-118">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="de70c-119">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="de70c-119">-DisplayOutputType</span></span>
<span data-ttu-id="de70c-120">A kért munkahelyi kimeneti típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="de70c-120">Specifies the job output type being requested.</span></span>
<span data-ttu-id="de70c-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="de70c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de70c-122">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="de70c-122">StandardOutput</span></span>
- <span data-ttu-id="de70c-123">StandardError</span><span class="sxs-lookup"><span data-stu-id="de70c-123">StandardError</span></span>

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

### <span data-ttu-id="de70c-124">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="de70c-124">-HttpCredential</span></span>
<span data-ttu-id="de70c-125">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="de70c-125">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="de70c-126">-JobId</span><span class="sxs-lookup"><span data-stu-id="de70c-126">-JobId</span></span>
<span data-ttu-id="de70c-127">Annak a projektnek az AZONOSÍTÓját adja meg, amelynek a kimenetét le fogja olvasni.</span><span class="sxs-lookup"><span data-stu-id="de70c-127">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="de70c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de70c-128">-ResourceGroupName</span></span>
<span data-ttu-id="de70c-129">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de70c-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="de70c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de70c-130">-DefaultProfile</span></span>
<span data-ttu-id="de70c-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de70c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de70c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de70c-132">CommonParameters</span></span>
<span data-ttu-id="de70c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de70c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de70c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de70c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de70c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de70c-135">INPUTS</span></span>

## <span data-ttu-id="de70c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de70c-136">OUTPUTS</span></span>

### <span data-ttu-id="de70c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="de70c-137">System.String</span></span>

## <span data-ttu-id="de70c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de70c-138">NOTES</span></span>

## <span data-ttu-id="de70c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de70c-139">RELATED LINKS</span></span>

[<span data-ttu-id="de70c-140">Új – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="de70c-140">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="de70c-141">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="de70c-141">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


