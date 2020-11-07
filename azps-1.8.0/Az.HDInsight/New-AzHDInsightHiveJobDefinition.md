---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4d8a35498462cae6e218fc41365de89a897bb555
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836013"
---
# <span data-ttu-id="a2db3-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a2db3-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="a2db3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2db3-102">SYNOPSIS</span></span>
<span data-ttu-id="a2db3-103">Kaptár-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a2db3-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="a2db3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2db3-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2db3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2db3-105">DESCRIPTION</span></span>
<span data-ttu-id="a2db3-106">A **New-AzHDInsightHiveJobDefinition** parancsmag az Azure HDInsight-fürtökhöz használható kaptár-munkaobjektumot definiálja.</span><span class="sxs-lookup"><span data-stu-id="a2db3-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a2db3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2db3-107">EXAMPLES</span></span>

### <span data-ttu-id="a2db3-108">1. példa: a kaptár-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="a2db3-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="a2db3-109">Ez a parancs létrehoz egy kaptár-feladatdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="a2db3-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="a2db3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2db3-110">PARAMETERS</span></span>

### <span data-ttu-id="a2db3-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="a2db3-111">-Arguments</span></span>
<span data-ttu-id="a2db3-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2db3-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="a2db3-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="a2db3-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="a2db3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2db3-114">-DefaultProfile</span></span>
<span data-ttu-id="a2db3-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a2db3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2db3-116">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="a2db3-116">-Defines</span></span>
<span data-ttu-id="a2db3-117">Itt adhatja meg a Hadoop konfigurációs értékeit, amelyeket a feladat futásakor be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="a2db3-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="a2db3-118">-Fájl</span><span class="sxs-lookup"><span data-stu-id="a2db3-118">-File</span></span>
<span data-ttu-id="a2db3-119">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2db3-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="a2db3-120">A fájlnak elérhetőnek kell lennie a fürthöz társított tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="a2db3-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="a2db3-121">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="a2db3-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="a2db3-122">-Files</span><span class="sxs-lookup"><span data-stu-id="a2db3-122">-Files</span></span>
<span data-ttu-id="a2db3-123">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2db3-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="a2db3-124">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="a2db3-124">-JobName</span></span>
<span data-ttu-id="a2db3-125">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2db3-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="a2db3-126">-Query</span><span class="sxs-lookup"><span data-stu-id="a2db3-126">-Query</span></span>
<span data-ttu-id="a2db3-127">A kaptár-lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2db3-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="a2db3-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="a2db3-128">-RunAsFileJob</span></span>
<span data-ttu-id="a2db3-129">Jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure Storage-fiókban, amelyben a lekérdezés tárolható.</span><span class="sxs-lookup"><span data-stu-id="a2db3-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="a2db3-130">Ez a parancsmag elküldi azt a feladatot, amely parancsfájlként hivatkozik erre a fájlra.</span><span class="sxs-lookup"><span data-stu-id="a2db3-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="a2db3-131">Ezt a funkciót speciális karakterek (például százalék (%)) kezelésére használhatja. Ez a Templeton-on keresztül sikertelen volt, mert a Templeton URL-ként értelmezi a százalékos jellel ellátni kívánt lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="a2db3-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="a2db3-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="a2db3-132">-StatusFolder</span></span>
<span data-ttu-id="a2db3-133">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a2db3-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="a2db3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2db3-134">CommonParameters</span></span>
<span data-ttu-id="a2db3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2db3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2db3-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2db3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2db3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2db3-137">INPUTS</span></span>

### <span data-ttu-id="a2db3-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="a2db3-138">None</span></span>

## <span data-ttu-id="a2db3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2db3-139">OUTPUTS</span></span>

### <span data-ttu-id="a2db3-140">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a2db3-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="a2db3-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2db3-141">NOTES</span></span>

## <span data-ttu-id="a2db3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2db3-142">RELATED LINKS</span></span>

[<span data-ttu-id="a2db3-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a2db3-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


