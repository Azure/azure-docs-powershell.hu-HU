---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: d9ea9152844db82d345ba1f6f50305b33975ced4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024771"
---
# <span data-ttu-id="a78be-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a78be-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="a78be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a78be-102">SYNOPSIS</span></span>
<span data-ttu-id="a78be-103">Egy Pig-Job objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a78be-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="a78be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a78be-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a78be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a78be-105">DESCRIPTION</span></span>
<span data-ttu-id="a78be-106">A **New-AzHDInsightPigJobDefinition** parancsmag az Azure HDInsight-fürtökhöz használható Pig Job objektumot definiálja.</span><span class="sxs-lookup"><span data-stu-id="a78be-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a78be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a78be-107">EXAMPLES</span></span>

### <span data-ttu-id="a78be-108">1. példa: a sertések feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="a78be-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="a78be-109">Ez a parancs egy Pig-feladatdefiníció létrehozásakor hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a78be-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="a78be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a78be-110">PARAMETERS</span></span>

### <span data-ttu-id="a78be-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="a78be-111">-Arguments</span></span>
<span data-ttu-id="a78be-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a78be-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="a78be-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="a78be-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="a78be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78be-114">-DefaultProfile</span></span>
<span data-ttu-id="a78be-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a78be-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a78be-116">-Fájl</span><span class="sxs-lookup"><span data-stu-id="a78be-116">-File</span></span>
<span data-ttu-id="a78be-117">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a78be-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="a78be-118">A fájlnak elérhetőnek kell lennie a fürthöz társított tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="a78be-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="a78be-119">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="a78be-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="a78be-120">-Files</span><span class="sxs-lookup"><span data-stu-id="a78be-120">-Files</span></span>
<span data-ttu-id="a78be-121">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a78be-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="a78be-122">-Query</span><span class="sxs-lookup"><span data-stu-id="a78be-122">-Query</span></span>
<span data-ttu-id="a78be-123">A sertések lekérdezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="a78be-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="a78be-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="a78be-124">-StatusFolder</span></span>
<span data-ttu-id="a78be-125">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a78be-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="a78be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78be-126">CommonParameters</span></span>
<span data-ttu-id="a78be-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a78be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78be-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a78be-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78be-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a78be-129">INPUTS</span></span>

### <span data-ttu-id="a78be-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="a78be-130">None</span></span>

## <span data-ttu-id="a78be-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a78be-131">OUTPUTS</span></span>

### <span data-ttu-id="a78be-132">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a78be-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="a78be-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a78be-133">NOTES</span></span>

## <span data-ttu-id="a78be-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a78be-134">RELATED LINKS</span></span>

[<span data-ttu-id="a78be-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a78be-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


