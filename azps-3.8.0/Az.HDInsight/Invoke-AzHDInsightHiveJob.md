---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: be478ff5c5fb6c638a0fc775c7c6787083a182cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847550"
---
# <span data-ttu-id="06cde-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="06cde-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="06cde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06cde-102">SYNOPSIS</span></span>
<span data-ttu-id="06cde-103">A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="06cde-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="06cde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06cde-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06cde-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06cde-105">DESCRIPTION</span></span>
<span data-ttu-id="06cde-106">A **meghívó-AzHDInsightHiveJob** parancsmag a kaptár-lekérdezést egy Azure HDInsight-fürthöz továbbítja, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="06cde-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="06cde-107">Használja az Use-AzHDInsightCluster parancsmagot az **AzHDInsightHiveJob** hívása előtt, és adja meg, hogy melyik fürtöt fogja használni a lekérdezéshez.</span><span class="sxs-lookup"><span data-stu-id="06cde-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="06cde-108">Példák</span><span class="sxs-lookup"><span data-stu-id="06cde-108">EXAMPLES</span></span>

### <span data-ttu-id="06cde-109">1. példa: a kaptár-lekérdezés beadása Azure HDInsight-fürtbe</span><span class="sxs-lookup"><span data-stu-id="06cde-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="06cde-110">Ez a parancs elküldi a lekérdezést a TÁBLÁKnak a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="06cde-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="06cde-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06cde-111">PARAMETERS</span></span>

### <span data-ttu-id="06cde-112">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="06cde-112">-Arguments</span></span>
<span data-ttu-id="06cde-113">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06cde-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="06cde-114">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="06cde-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="06cde-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="06cde-115">-DefaultContainer</span></span>
<span data-ttu-id="06cde-116">Annak az alapértelmezett tárolónak a nevét adja meg az alapértelmezett Azure Storage-fiókban, amelyet egy HDInsight-fürt használ.</span><span class="sxs-lookup"><span data-stu-id="06cde-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="06cde-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06cde-117">-DefaultProfile</span></span>
<span data-ttu-id="06cde-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="06cde-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06cde-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="06cde-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="06cde-120">A HDInsight-fürtöt használó alapértelmezett tárterület-fiókhoz tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="06cde-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="06cde-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06cde-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="06cde-122">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06cde-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="06cde-123">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="06cde-123">-Defines</span></span>
<span data-ttu-id="06cde-124">Itt adhatja meg a Hadoop konfigurációs értékeit a feladatok futásakor.</span><span class="sxs-lookup"><span data-stu-id="06cde-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="06cde-125">-Fájl</span><span class="sxs-lookup"><span data-stu-id="06cde-125">-File</span></span>
<span data-ttu-id="06cde-126">A futtatni kívánt lekérdezést tartalmazó Azure-tárterületen lévő fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="06cde-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="06cde-127">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="06cde-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="06cde-128">-Files</span><span class="sxs-lookup"><span data-stu-id="06cde-128">-Files</span></span>
<span data-ttu-id="06cde-129">A kaptár-feladathoz szükséges fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06cde-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="06cde-130">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="06cde-130">-JobName</span></span>
<span data-ttu-id="06cde-131">A kaptár-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06cde-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="06cde-132">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett értéket használja: "kaptár: a \< lekérdezés első 100 karaktere \> ".</span><span class="sxs-lookup"><span data-stu-id="06cde-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="06cde-133">-Query</span><span class="sxs-lookup"><span data-stu-id="06cde-133">-Query</span></span>
<span data-ttu-id="06cde-134">A kaptár-lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="06cde-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="06cde-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="06cde-135">-RunAsFileJob</span></span>
<span data-ttu-id="06cde-136">Jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure Storage-fiókban, amelyben a lekérdezés tárolható.</span><span class="sxs-lookup"><span data-stu-id="06cde-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="06cde-137">Ez a parancsmag elküldi azt a feladatot, amely parancsfájlként hivatkozik erre a fájlra.</span><span class="sxs-lookup"><span data-stu-id="06cde-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="06cde-138">Ezt a funkciót speciális karakterek (például százalék (%)) kezelésére használhatja. Ez a Templeton-on keresztül sikertelen volt, mert a Templeton URL-ként értelmezi a százalékos jellel ellátni kívánt lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="06cde-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="06cde-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="06cde-139">-StatusFolder</span></span>
<span data-ttu-id="06cde-140">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="06cde-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="06cde-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06cde-141">CommonParameters</span></span>
<span data-ttu-id="06cde-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06cde-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06cde-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06cde-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06cde-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06cde-144">INPUTS</span></span>

### <span data-ttu-id="06cde-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="06cde-145">None</span></span>

## <span data-ttu-id="06cde-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06cde-146">OUTPUTS</span></span>

### <span data-ttu-id="06cde-147">System. String</span><span class="sxs-lookup"><span data-stu-id="06cde-147">System.String</span></span>

## <span data-ttu-id="06cde-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06cde-148">NOTES</span></span>

## <span data-ttu-id="06cde-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06cde-149">RELATED LINKS</span></span>

[<span data-ttu-id="06cde-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="06cde-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)

