---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 69bb20b8a6610d2701a6c2256317b081dc11ad3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167451"
---
# <span data-ttu-id="fee96-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fee96-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="fee96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee96-102">SYNOPSIS</span></span>
<span data-ttu-id="fee96-103">Létrehoz egy Sqoop feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="fee96-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="fee96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fee96-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fee96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fee96-105">DESCRIPTION</span></span>
<span data-ttu-id="fee96-106">A **New-AzHDInsightSqoop JobDefinition** parancsmag egy Azure HDInsight-fürthöz használható Sqoop-feladatobjektumot definiál.</span><span class="sxs-lookup"><span data-stu-id="fee96-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fee96-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fee96-107">EXAMPLES</span></span>

### <span data-ttu-id="fee96-108">1. példa: Sqoop-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="fee96-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="fee96-109">Ez a parancs létrehoz egy Sqoop feladatdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="fee96-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="fee96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee96-110">PARAMETERS</span></span>

### <span data-ttu-id="fee96-111">-Command</span><span class="sxs-lookup"><span data-stu-id="fee96-111">-Command</span></span>
<span data-ttu-id="fee96-112">A Sqoop parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fee96-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="fee96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee96-113">-DefaultProfile</span></span>
<span data-ttu-id="fee96-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fee96-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fee96-115">-File</span><span class="sxs-lookup"><span data-stu-id="fee96-115">-File</span></span>
<span data-ttu-id="fee96-116">A futtatni kívánt lekérdezést tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fee96-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="fee96-117">A fájlnak elérhetőnek kell lennie a fürthöz társított Tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="fee96-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="fee96-118">Ezt a paramétert használhatja a *Lekérdezés paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="fee96-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="fee96-119">-Files</span><span class="sxs-lookup"><span data-stu-id="fee96-119">-Files</span></span>
<span data-ttu-id="fee96-120">A Hive-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fee96-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="fee96-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="fee96-121">-LibDir</span></span>
<span data-ttu-id="fee96-122">A Sqoop feladat tárkönyvtárát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fee96-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="fee96-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="fee96-123">-StatusFolder</span></span>
<span data-ttu-id="fee96-124">Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fee96-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="fee96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee96-125">CommonParameters</span></span>
<span data-ttu-id="fee96-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee96-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fee96-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee96-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fee96-128">INPUTS</span></span>

### <span data-ttu-id="fee96-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="fee96-129">None</span></span>

## <span data-ttu-id="fee96-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fee96-130">OUTPUTS</span></span>

### <span data-ttu-id="fee96-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fee96-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="fee96-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fee96-132">NOTES</span></span>

## <span data-ttu-id="fee96-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fee96-133">RELATED LINKS</span></span>

[<span data-ttu-id="fee96-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fee96-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


