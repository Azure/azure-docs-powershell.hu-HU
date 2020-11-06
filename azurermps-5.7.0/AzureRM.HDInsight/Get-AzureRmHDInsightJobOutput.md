---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 2f63ba552931f70b745816a1d1b892977b6626e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505523"
---
# <span data-ttu-id="906f0-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="906f0-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="906f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="906f0-102">SYNOPSIS</span></span>
<span data-ttu-id="906f0-103">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="906f0-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="906f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="906f0-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="906f0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="906f0-105">DESCRIPTION</span></span>
<span data-ttu-id="906f0-106">A **Get-AzureRmHDInsightJobOutput** parancsmag az Azure HDInsight-fürtökhez társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="906f0-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="906f0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="906f0-107">EXAMPLES</span></span>

### <span data-ttu-id="906f0-108">Példa 1: a napló kimenetének beolvasása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="906f0-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="906f0-109">Ez a parancs a Hadoop-001 nevű fürtből kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="906f0-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="906f0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="906f0-110">PARAMETERS</span></span>

### <span data-ttu-id="906f0-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="906f0-111">-ClusterName</span></span>
<span data-ttu-id="906f0-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="906f0-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="906f0-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="906f0-113">-DefaultContainer</span></span>
<span data-ttu-id="906f0-114">Az alapértelmezett tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="906f0-114">Specifies the default container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906f0-115">-DefaultProfile</span></span>
<span data-ttu-id="906f0-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="906f0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="906f0-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="906f0-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="906f0-118">Az alapértelmezett tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="906f0-118">Specifies the default Storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f0-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="906f0-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="906f0-120">Az alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="906f0-120">Specifies the default Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f0-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="906f0-121">-DisplayOutputType</span></span>
<span data-ttu-id="906f0-122">A kért munkahelyi kimeneti típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="906f0-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="906f0-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="906f0-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="906f0-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="906f0-124">StandardOutput</span></span>
- <span data-ttu-id="906f0-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="906f0-125">StandardError</span></span>

```yaml
Type: JobDisplayOutputType
Parameter Sets: (All)
Aliases: 
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f0-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="906f0-126">-HttpCredential</span></span>
<span data-ttu-id="906f0-127">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="906f0-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f0-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="906f0-128">-JobId</span></span>
<span data-ttu-id="906f0-129">Annak a projektnek az AZONOSÍTÓját adja meg, amelynek a kimenetét le fogja olvasni.</span><span class="sxs-lookup"><span data-stu-id="906f0-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="906f0-130">-ResourceGroupName</span></span>
<span data-ttu-id="906f0-131">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="906f0-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="906f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906f0-132">CommonParameters</span></span>
<span data-ttu-id="906f0-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="906f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906f0-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="906f0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906f0-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="906f0-135">INPUTS</span></span>

### <span data-ttu-id="906f0-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="906f0-136">None</span></span>
<span data-ttu-id="906f0-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="906f0-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="906f0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="906f0-138">OUTPUTS</span></span>

### <span data-ttu-id="906f0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="906f0-139">System.String</span></span>

## <span data-ttu-id="906f0-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="906f0-140">NOTES</span></span>

## <span data-ttu-id="906f0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="906f0-141">RELATED LINKS</span></span>

[<span data-ttu-id="906f0-142">Új – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="906f0-142">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="906f0-143">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="906f0-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


