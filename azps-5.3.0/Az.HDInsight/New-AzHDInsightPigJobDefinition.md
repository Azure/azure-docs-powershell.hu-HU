---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: 4a21a8fdacdb53df7e513744cae31da4a7a61ca7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469661"
---
# <span data-ttu-id="49dff-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="49dff-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="49dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49dff-102">SYNOPSIS</span></span>
<span data-ttu-id="49dff-103">Ezzel a beállításokkal egy feladatobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="49dff-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="49dff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49dff-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49dff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49dff-105">DESCRIPTION</span></span>
<span data-ttu-id="49dff-106">A **New-AzHDInsightPig JobDefinition** parancsmag egy Feladatobjektumot definiál Azure HDInsight-fürthöz való használatra.</span><span class="sxs-lookup"><span data-stu-id="49dff-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="49dff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49dff-107">EXAMPLES</span></span>

### <span data-ttu-id="49dff-108">1. példa: Feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="49dff-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="49dff-109">Ez a parancs létrehoz egy feladatdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="49dff-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="49dff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49dff-110">PARAMETERS</span></span>

### <span data-ttu-id="49dff-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="49dff-111">-Arguments</span></span>
<span data-ttu-id="49dff-112">Egy tömböt ad meg a feladat argumentumaiból.</span><span class="sxs-lookup"><span data-stu-id="49dff-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="49dff-113">Az argumentumokat a függvény parancssori argumentumként minden tevékenységnek továbbkűni.</span><span class="sxs-lookup"><span data-stu-id="49dff-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="49dff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49dff-114">-DefaultProfile</span></span>
<span data-ttu-id="49dff-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49dff-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49dff-116">-File</span><span class="sxs-lookup"><span data-stu-id="49dff-116">-File</span></span>
<span data-ttu-id="49dff-117">A futtatni kívánt lekérdezést tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dff-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="49dff-118">A fájlnak elérhetőnek kell lennie a fürthöz társított tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="49dff-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="49dff-119">Ezt a paramétert használhatja a *Lekérdezés paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="49dff-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="49dff-120">-Files</span><span class="sxs-lookup"><span data-stu-id="49dff-120">-Files</span></span>
<span data-ttu-id="49dff-121">A Hive-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dff-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="49dff-122">-Query</span><span class="sxs-lookup"><span data-stu-id="49dff-122">-Query</span></span>
<span data-ttu-id="49dff-123">A Saláta lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dff-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="49dff-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="49dff-124">-StatusFolder</span></span>
<span data-ttu-id="49dff-125">Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="49dff-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="49dff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49dff-126">CommonParameters</span></span>
<span data-ttu-id="49dff-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49dff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49dff-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49dff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49dff-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49dff-129">INPUTS</span></span>

### <span data-ttu-id="49dff-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="49dff-130">None</span></span>

## <span data-ttu-id="49dff-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49dff-131">OUTPUTS</span></span>

### <span data-ttu-id="49dff-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="49dff-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="49dff-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49dff-133">NOTES</span></span>

## <span data-ttu-id="49dff-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49dff-134">RELATED LINKS</span></span>

[<span data-ttu-id="49dff-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="49dff-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


