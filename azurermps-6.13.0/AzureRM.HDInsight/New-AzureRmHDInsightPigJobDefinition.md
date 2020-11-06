---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 27f2e9d6dbc823f7148db6a299f9e999131c75d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505396"
---
# <span data-ttu-id="93a44-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="93a44-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="93a44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93a44-102">SYNOPSIS</span></span>
<span data-ttu-id="93a44-103">Egy Pig-Job objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="93a44-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93a44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93a44-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93a44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93a44-105">DESCRIPTION</span></span>
<span data-ttu-id="93a44-106">A **New-AzureRmHDInsightPigJobDefinition** parancsmag az Azure HDInsight-fürtökhöz használható Pig Job objektumot definiálja.</span><span class="sxs-lookup"><span data-stu-id="93a44-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="93a44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93a44-107">EXAMPLES</span></span>

### <span data-ttu-id="93a44-108">1. példa: a sertések feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="93a44-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="93a44-109">Ez a parancs egy Pig-feladatdefiníció létrehozásakor hoz létre.</span><span class="sxs-lookup"><span data-stu-id="93a44-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="93a44-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93a44-110">PARAMETERS</span></span>

### <span data-ttu-id="93a44-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="93a44-111">-Arguments</span></span>
<span data-ttu-id="93a44-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93a44-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="93a44-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="93a44-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="93a44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a44-114">-DefaultProfile</span></span>
<span data-ttu-id="93a44-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="93a44-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93a44-116">-Fájl</span><span class="sxs-lookup"><span data-stu-id="93a44-116">-File</span></span>
<span data-ttu-id="93a44-117">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="93a44-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="93a44-118">A fájlnak elérhetőnek kell lennie a fürthöz társított tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="93a44-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="93a44-119">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="93a44-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="93a44-120">-Files</span><span class="sxs-lookup"><span data-stu-id="93a44-120">-Files</span></span>
<span data-ttu-id="93a44-121">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93a44-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="93a44-122">-Query</span><span class="sxs-lookup"><span data-stu-id="93a44-122">-Query</span></span>
<span data-ttu-id="93a44-123">A sertések lekérdezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="93a44-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="93a44-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="93a44-124">-StatusFolder</span></span>
<span data-ttu-id="93a44-125">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="93a44-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="93a44-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a44-126">CommonParameters</span></span>
<span data-ttu-id="93a44-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93a44-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a44-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a44-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a44-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93a44-129">INPUTS</span></span>

### <span data-ttu-id="93a44-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="93a44-130">None</span></span>

## <span data-ttu-id="93a44-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93a44-131">OUTPUTS</span></span>

### <span data-ttu-id="93a44-132">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="93a44-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="93a44-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93a44-133">NOTES</span></span>

## <span data-ttu-id="93a44-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93a44-134">RELATED LINKS</span></span>

[<span data-ttu-id="93a44-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="93a44-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


