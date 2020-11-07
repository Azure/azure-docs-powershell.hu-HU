---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847517"
---
# <span data-ttu-id="7cbb5-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7cbb5-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="7cbb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbb5-103">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="7cbb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cbb5-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cbb5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cbb5-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbb5-106">A **New-AzHDInsightSqoopJobDefinition** parancsmag az Azure HDInsight-fürtökkel használható Sqoop-objektumot definiálja.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7cbb5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7cbb5-107">EXAMPLES</span></span>

### <span data-ttu-id="7cbb5-108">Példa 1: Sqoop-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="7cbb5-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="7cbb5-109">Ez a parancs létrehoz egy Sqoop-feladatdefiníció.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="7cbb5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cbb5-110">PARAMETERS</span></span>

### <span data-ttu-id="7cbb5-111">-Command</span><span class="sxs-lookup"><span data-stu-id="7cbb5-111">-Command</span></span>
<span data-ttu-id="7cbb5-112">A Sqoop parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="7cbb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbb5-113">-DefaultProfile</span></span>
<span data-ttu-id="7cbb5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7cbb5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cbb5-115">-Fájl</span><span class="sxs-lookup"><span data-stu-id="7cbb5-115">-File</span></span>
<span data-ttu-id="7cbb5-116">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="7cbb5-117">A fájlnak elérhetőnek kell lennie a fürthöz társított tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="7cbb5-118">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="7cbb5-119">-Files</span><span class="sxs-lookup"><span data-stu-id="7cbb5-119">-Files</span></span>
<span data-ttu-id="7cbb5-120">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-120">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbb5-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="7cbb5-121">-LibDir</span></span>
<span data-ttu-id="7cbb5-122">A Sqoop-feladat könyvtári könyvtárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="7cbb5-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="7cbb5-123">-StatusFolder</span></span>
<span data-ttu-id="7cbb5-124">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7cbb5-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="7cbb5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbb5-125">CommonParameters</span></span>
<span data-ttu-id="7cbb5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cbb5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbb5-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cbb5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbb5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cbb5-128">INPUTS</span></span>

### <span data-ttu-id="7cbb5-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="7cbb5-129">None</span></span>

## <span data-ttu-id="7cbb5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cbb5-130">OUTPUTS</span></span>

### <span data-ttu-id="7cbb5-131">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7cbb5-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="7cbb5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cbb5-132">NOTES</span></span>

## <span data-ttu-id="7cbb5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cbb5-133">RELATED LINKS</span></span>

[<span data-ttu-id="7cbb5-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7cbb5-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

