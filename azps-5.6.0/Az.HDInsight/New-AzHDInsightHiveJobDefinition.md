---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: be8878d338206e1355dc36082d4f9941cf141838
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008998"
---
# <span data-ttu-id="b28dc-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b28dc-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="b28dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b28dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b28dc-103">Létrehoz egy Hive-feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="b28dc-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="b28dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b28dc-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b28dc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b28dc-105">DESCRIPTION</span></span>
<span data-ttu-id="b28dc-106">A **New-AzHDInsightHive JobDefinition** parancsmag egy Hive-feladatobjektumot definiál Azure HDInsight-fürthöz való használatra.</span><span class="sxs-lookup"><span data-stu-id="b28dc-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b28dc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b28dc-107">EXAMPLES</span></span>

### <span data-ttu-id="b28dc-108">1. példa: Hive-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="b28dc-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b28dc-109">Ez a parancs létrehoz egy Hive-feladatdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="b28dc-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="b28dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b28dc-110">PARAMETERS</span></span>

### <span data-ttu-id="b28dc-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="b28dc-111">-Arguments</span></span>
<span data-ttu-id="b28dc-112">Egy tömböt ad meg a feladat argumentumaiból.</span><span class="sxs-lookup"><span data-stu-id="b28dc-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b28dc-113">Az argumentumokat a függvény parancssori argumentumként minden tevékenységnek továbbkűni.</span><span class="sxs-lookup"><span data-stu-id="b28dc-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b28dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28dc-114">-DefaultProfile</span></span>
<span data-ttu-id="b28dc-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b28dc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b28dc-116">-Definiál</span><span class="sxs-lookup"><span data-stu-id="b28dc-116">-Defines</span></span>
<span data-ttu-id="b28dc-117">Megadja a Hadoop konfigurációs értékeit, amelyek a feladat futtatásakor adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="b28dc-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28dc-118">-File</span><span class="sxs-lookup"><span data-stu-id="b28dc-118">-File</span></span>
<span data-ttu-id="b28dc-119">A futtatni kívánt lekérdezést tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b28dc-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b28dc-120">A fájlnak elérhetőnek kell lennie a fürthöz társított tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="b28dc-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="b28dc-121">Ezt a paramétert használhatja a *Lekérdezés paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="b28dc-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b28dc-122">-Files</span><span class="sxs-lookup"><span data-stu-id="b28dc-122">-Files</span></span>
<span data-ttu-id="b28dc-123">A Hive-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b28dc-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b28dc-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="b28dc-124">-JobName</span></span>
<span data-ttu-id="b28dc-125">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b28dc-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="b28dc-126">-Query</span><span class="sxs-lookup"><span data-stu-id="b28dc-126">-Query</span></span>
<span data-ttu-id="b28dc-127">A Hive lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="b28dc-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="b28dc-128">-RunAsFileFile</span><span class="sxs-lookup"><span data-stu-id="b28dc-128">-RunAsFileJob</span></span>
<span data-ttu-id="b28dc-129">Azt jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure-tárfiókban, amelyben a lekérdezést tárolni lehet.</span><span class="sxs-lookup"><span data-stu-id="b28dc-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="b28dc-130">Ez a parancsmag parancsprogramként elküldi a fájlra hivatkozó feladatot.</span><span class="sxs-lookup"><span data-stu-id="b28dc-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="b28dc-131">Ez a funkció speciális karakterek, például százalékjel (%) kezeléséhez használható. hiba lépne fel a Templetonon keresztüli munkabeküldésekkor, mert a Templeton a százalékjelet beküldött lekérdezéseket URL-paraméterként értelmezi.</span><span class="sxs-lookup"><span data-stu-id="b28dc-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28dc-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b28dc-132">-StatusFolder</span></span>
<span data-ttu-id="b28dc-133">Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b28dc-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b28dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28dc-134">CommonParameters</span></span>
<span data-ttu-id="b28dc-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b28dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28dc-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b28dc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28dc-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b28dc-137">INPUTS</span></span>

### <span data-ttu-id="b28dc-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="b28dc-138">None</span></span>

## <span data-ttu-id="b28dc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b28dc-139">OUTPUTS</span></span>

### <span data-ttu-id="b28dc-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b28dc-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="b28dc-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b28dc-141">NOTES</span></span>

## <span data-ttu-id="b28dc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b28dc-142">RELATED LINKS</span></span>

[<span data-ttu-id="b28dc-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b28dc-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


