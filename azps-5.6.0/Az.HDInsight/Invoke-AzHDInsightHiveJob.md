---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 2846848394cf6f376bd6b4064e193640806f81b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922434"
---
# <span data-ttu-id="9733b-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="9733b-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="9733b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9733b-102">SYNOPSIS</span></span>
<span data-ttu-id="9733b-103">Hive-lekérdezést küld egy HDInsight-fürtnek, és egy művelettel beolvassa a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="9733b-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="9733b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9733b-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9733b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9733b-105">DESCRIPTION</span></span>
<span data-ttu-id="9733b-106">Az **Invoke-AzHDInsightHiveCm** parancsmag egy Hive-lekérdezést küld egy Azure HDInsight-fürtnek, és egy művelettel beolvassa a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="9733b-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="9733b-107">Mielőtt meghívja Use-AzHDInsightCluster **Invoke-AzHDInsightHiveFeladatot,** adja meg a lekérdezéshez használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="9733b-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="9733b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9733b-108">EXAMPLES</span></span>

### <span data-ttu-id="9733b-109">1. példa: Hive-lekérdezés elküldése Azure HDInsight-fürtbe</span><span class="sxs-lookup"><span data-stu-id="9733b-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="9733b-110">Ez a parancs elküldi a TÁBLA MEGJELENÍTÉSE lekérdezést a "your-hadoop-001" nevű fürtnek.</span><span class="sxs-lookup"><span data-stu-id="9733b-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9733b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9733b-111">PARAMETERS</span></span>

### <span data-ttu-id="9733b-112">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="9733b-112">-Arguments</span></span>
<span data-ttu-id="9733b-113">Egy tömböt ad meg a feladat argumentumaiból.</span><span class="sxs-lookup"><span data-stu-id="9733b-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="9733b-114">Az argumentumokat a függvény parancssori argumentumként minden tevékenységnek továbbkűni.</span><span class="sxs-lookup"><span data-stu-id="9733b-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="9733b-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="9733b-115">-DefaultContainer</span></span>
<span data-ttu-id="9733b-116">A HDInsight-fürt alapértelmezett Azure Storage-fiókjában található alapértelmezett tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9733b-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="9733b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9733b-117">-DefaultProfile</span></span>
<span data-ttu-id="9733b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9733b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9733b-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9733b-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="9733b-120">A HDInsight-fürt által használt alapértelmezett tárfiók fiókkulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9733b-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="9733b-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9733b-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="9733b-122">A HDInsight-fürt által használt alapértelmezett tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="9733b-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="9733b-123">-Definiál</span><span class="sxs-lookup"><span data-stu-id="9733b-123">-Defines</span></span>
<span data-ttu-id="9733b-124">Megadja a hadoop konfigurációs értékeit, amelyek a feladat futtatásakor adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="9733b-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="9733b-125">-File</span><span class="sxs-lookup"><span data-stu-id="9733b-125">-File</span></span>
<span data-ttu-id="9733b-126">A futtatni kívánt lekérdezést tartalmazó fájl elérési útját adja meg az Azure Storage-ban.</span><span class="sxs-lookup"><span data-stu-id="9733b-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="9733b-127">Ezt a paramétert használhatja a *Lekérdezés paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="9733b-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="9733b-128">-Files</span><span class="sxs-lookup"><span data-stu-id="9733b-128">-Files</span></span>
<span data-ttu-id="9733b-129">A Hive-feladathoz szükséges fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9733b-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="9733b-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="9733b-130">-JobName</span></span>
<span data-ttu-id="9733b-131">A Hive-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9733b-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="9733b-132">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett értéket használja: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="9733b-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="9733b-133">-Query</span><span class="sxs-lookup"><span data-stu-id="9733b-133">-Query</span></span>
<span data-ttu-id="9733b-134">A Hive lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="9733b-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="9733b-135">-RunAsFileFile</span><span class="sxs-lookup"><span data-stu-id="9733b-135">-RunAsFileJob</span></span>
<span data-ttu-id="9733b-136">Azt jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure-tárfiókban, amelyben a lekérdezést tárolni lehet.</span><span class="sxs-lookup"><span data-stu-id="9733b-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="9733b-137">Ez a parancsmag parancsprogramként elküldi a fájlra hivatkozó feladatot.</span><span class="sxs-lookup"><span data-stu-id="9733b-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="9733b-138">Ez a funkció speciális karakterek, például százalékjel (%) kezeléséhez használható. hiba lépne fel a Templetonon keresztüli munkabeküldésekkor, mert a Templeton a százalékjelet beküldött lekérdezéseket URL-paraméterként értelmezi.</span><span class="sxs-lookup"><span data-stu-id="9733b-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="9733b-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="9733b-139">-StatusFolder</span></span>
<span data-ttu-id="9733b-140">Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9733b-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="9733b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9733b-141">CommonParameters</span></span>
<span data-ttu-id="9733b-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9733b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9733b-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9733b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9733b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9733b-144">INPUTS</span></span>

### <span data-ttu-id="9733b-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="9733b-145">None</span></span>

## <span data-ttu-id="9733b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9733b-146">OUTPUTS</span></span>

### <span data-ttu-id="9733b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9733b-147">System.String</span></span>

## <span data-ttu-id="9733b-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9733b-148">NOTES</span></span>

## <span data-ttu-id="9733b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9733b-149">RELATED LINKS</span></span>

[<span data-ttu-id="9733b-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9733b-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


