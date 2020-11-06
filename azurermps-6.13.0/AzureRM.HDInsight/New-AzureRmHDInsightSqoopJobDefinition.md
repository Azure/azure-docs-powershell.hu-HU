---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 709c87084cc871814e4760e0d2641c59b0e5a64e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496112"
---
# <span data-ttu-id="39aa4-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="39aa4-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="39aa4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="39aa4-103">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="39aa4-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39aa4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39aa4-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39aa4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="39aa4-106">A **New-AzureRmHDInsightSqoopJobDefinition** parancsmag az Azure HDInsight-fürtökkel használható Sqoop-objektumot definiálja.</span><span class="sxs-lookup"><span data-stu-id="39aa4-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="39aa4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="39aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="39aa4-108">Példa 1: Sqoop-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="39aa4-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="39aa4-109">Ez a parancs létrehoz egy Sqoop-feladatdefiníció.</span><span class="sxs-lookup"><span data-stu-id="39aa4-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="39aa4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39aa4-110">PARAMETERS</span></span>

### <span data-ttu-id="39aa4-111">-Command</span><span class="sxs-lookup"><span data-stu-id="39aa4-111">-Command</span></span>
<span data-ttu-id="39aa4-112">A Sqoop parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="39aa4-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="39aa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39aa4-113">-DefaultProfile</span></span>
<span data-ttu-id="39aa4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="39aa4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39aa4-115">-Fájl</span><span class="sxs-lookup"><span data-stu-id="39aa4-115">-File</span></span>
<span data-ttu-id="39aa4-116">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="39aa4-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="39aa4-117">A fájlnak elérhetőnek kell lennie a fürthöz társított tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="39aa4-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="39aa4-118">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="39aa4-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="39aa4-119">-Files</span><span class="sxs-lookup"><span data-stu-id="39aa4-119">-Files</span></span>
<span data-ttu-id="39aa4-120">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39aa4-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="39aa4-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="39aa4-121">-LibDir</span></span>
<span data-ttu-id="39aa4-122">A Sqoop-feladat könyvtári könyvtárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="39aa4-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="39aa4-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="39aa4-123">-StatusFolder</span></span>
<span data-ttu-id="39aa4-124">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="39aa4-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="39aa4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39aa4-125">CommonParameters</span></span>
<span data-ttu-id="39aa4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39aa4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39aa4-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39aa4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39aa4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39aa4-128">INPUTS</span></span>

### <span data-ttu-id="39aa4-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="39aa4-129">None</span></span>

## <span data-ttu-id="39aa4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39aa4-130">OUTPUTS</span></span>

### <span data-ttu-id="39aa4-131">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="39aa4-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="39aa4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39aa4-132">NOTES</span></span>

## <span data-ttu-id="39aa4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39aa4-133">RELATED LINKS</span></span>

[<span data-ttu-id="39aa4-134">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="39aa4-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


