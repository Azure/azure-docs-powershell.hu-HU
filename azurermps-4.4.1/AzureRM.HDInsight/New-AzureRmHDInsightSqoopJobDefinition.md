---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680271"
---
# <span data-ttu-id="2d1e9-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2d1e9-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="2d1e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1e9-103">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d1e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d1e9-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d1e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="2d1e9-106">A **New-AzureRmHDInsightSqoopJobDefinition** parancsmag az Azure HDInsight-fürtökkel használható Sqoop-objektumot definiálja.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2d1e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="2d1e9-108">Példa 1: Sqoop-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="2d1e9-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2d1e9-109">Ez a parancs létrehoz egy Sqoop-feladatdefiníció.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="2d1e9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d1e9-110">PARAMETERS</span></span>

### <span data-ttu-id="2d1e9-111">-Command</span><span class="sxs-lookup"><span data-stu-id="2d1e9-111">-Command</span></span>
<span data-ttu-id="2d1e9-112">A Sqoop parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="2d1e9-113">-Fájl</span><span class="sxs-lookup"><span data-stu-id="2d1e9-113">-File</span></span>
<span data-ttu-id="2d1e9-114">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="2d1e9-115">A fájlnak elérhetőnek kell lennie a fürthöz társított tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="2d1e9-116">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="2d1e9-117">-Files</span><span class="sxs-lookup"><span data-stu-id="2d1e9-117">-Files</span></span>
<span data-ttu-id="2d1e9-118">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-118">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="2d1e9-119">-LibDir</span><span class="sxs-lookup"><span data-stu-id="2d1e9-119">-LibDir</span></span>
<span data-ttu-id="2d1e9-120">A Sqoop-feladat könyvtári könyvtárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="2d1e9-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="2d1e9-121">-StatusFolder</span></span>
<span data-ttu-id="2d1e9-122">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="2d1e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1e9-123">-DefaultProfile</span></span>
<span data-ttu-id="2d1e9-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d1e9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d1e9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1e9-125">CommonParameters</span></span>
<span data-ttu-id="2d1e9-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d1e9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d1e9-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d1e9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1e9-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d1e9-128">INPUTS</span></span>

## <span data-ttu-id="2d1e9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d1e9-129">OUTPUTS</span></span>

### <span data-ttu-id="2d1e9-130">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2d1e9-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="2d1e9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d1e9-131">NOTES</span></span>

## <span data-ttu-id="2d1e9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d1e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="2d1e9-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2d1e9-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


