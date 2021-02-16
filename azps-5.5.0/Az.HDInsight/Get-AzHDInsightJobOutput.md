---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 400153558dffc619e8e567b292ad402a42ce9359
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155586"
---
# <span data-ttu-id="5b653-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="5b653-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="5b653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b653-102">SYNOPSIS</span></span>
<span data-ttu-id="5b653-103">Egy feladat naplókimenetét egy adott fürthöz társított tárfiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5b653-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="5b653-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b653-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b653-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b653-105">DESCRIPTION</span></span>
<span data-ttu-id="5b653-106">A **Get-AzHDInsight JobOutput** parancsmag egy Azure HDInsight-fürthöz társított tárfiókból kapja meg egy feladat naplókimenetét.</span><span class="sxs-lookup"><span data-stu-id="5b653-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5b653-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b653-107">EXAMPLES</span></span>

### <span data-ttu-id="5b653-108">1. példa: Egy feladat naplókimenetének lekérte</span><span class="sxs-lookup"><span data-stu-id="5b653-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="5b653-109">Ez a parancs a naplókimenetet a saját-hadoop-001 nevű fürtből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5b653-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5b653-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b653-110">PARAMETERS</span></span>

### <span data-ttu-id="5b653-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5b653-111">-ClusterName</span></span>
<span data-ttu-id="5b653-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b653-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5b653-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="5b653-113">-DefaultContainer</span></span>
<span data-ttu-id="5b653-114">Az alapértelmezett tárolónevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b653-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="5b653-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b653-115">-DefaultProfile</span></span>
<span data-ttu-id="5b653-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5b653-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b653-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5b653-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="5b653-118">Az alapértelmezett tárfiókkulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b653-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="5b653-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5b653-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="5b653-120">A Tárfiók alapértelmezett nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b653-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="5b653-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="5b653-121">-DisplayOutputType</span></span>
<span data-ttu-id="5b653-122">A kért kimeneti típus megadása.</span><span class="sxs-lookup"><span data-stu-id="5b653-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="5b653-123">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5b653-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b653-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="5b653-124">StandardOutput</span></span>
- <span data-ttu-id="5b653-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="5b653-125">StandardError</span></span>

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

### <span data-ttu-id="5b653-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="5b653-126">-HttpCredential</span></span>
<span data-ttu-id="5b653-127">A fürt bejelentkezési (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="5b653-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="5b653-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="5b653-128">-JobId</span></span>
<span data-ttu-id="5b653-129">Annak a feladatnak a feladatazonosítóját adja meg, amelynek kimenetét lekéri a alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="5b653-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="5b653-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b653-130">-ResourceGroupName</span></span>
<span data-ttu-id="5b653-131">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b653-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5b653-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b653-132">CommonParameters</span></span>
<span data-ttu-id="5b653-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b653-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b653-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b653-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b653-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b653-135">INPUTS</span></span>

### <span data-ttu-id="5b653-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="5b653-136">None</span></span>

## <span data-ttu-id="5b653-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b653-137">OUTPUTS</span></span>

### <span data-ttu-id="5b653-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5b653-138">System.String</span></span>

## <span data-ttu-id="5b653-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b653-139">NOTES</span></span>

## <span data-ttu-id="5b653-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b653-140">RELATED LINKS</span></span>

[<span data-ttu-id="5b653-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5b653-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="5b653-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5b653-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


