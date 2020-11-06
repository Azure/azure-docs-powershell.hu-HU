---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504984"
---
# <span data-ttu-id="931b7-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="931b7-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="931b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="931b7-102">SYNOPSIS</span></span>
<span data-ttu-id="931b7-103">A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="931b7-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="931b7-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="931b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="931b7-105">DESCRIPTION</span></span>
<span data-ttu-id="931b7-106">A **meghívó-AzureRmHDInsightHiveJob** parancsmag a kaptár-lekérdezést egy Azure HDInsight-fürthöz továbbítja, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="931b7-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="931b7-107">Használja az Use-AzureRmHDInsightCluster parancsmagot az **AzureRmHDInsightHiveJob** hívása előtt, és adja meg, hogy melyik fürtöt fogja használni a lekérdezéshez.</span><span class="sxs-lookup"><span data-stu-id="931b7-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="931b7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="931b7-108">EXAMPLES</span></span>

### <span data-ttu-id="931b7-109">1. példa: a kaptár-lekérdezés beadása Azure HDInsight-fürtbe</span><span class="sxs-lookup"><span data-stu-id="931b7-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="931b7-110">Ez a parancs elküldi a lekérdezést a TÁBLÁKnak a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="931b7-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="931b7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="931b7-111">PARAMETERS</span></span>

### <span data-ttu-id="931b7-112">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="931b7-112">-Arguments</span></span>
<span data-ttu-id="931b7-113">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="931b7-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="931b7-114">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="931b7-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="931b7-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="931b7-115">-DefaultContainer</span></span>
<span data-ttu-id="931b7-116">Annak az alapértelmezett tárolónak a nevét adja meg az alapértelmezett Azure Storage-fiókban, amelyet egy HDInsight-fürt használ.</span><span class="sxs-lookup"><span data-stu-id="931b7-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="931b7-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="931b7-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="931b7-118">A HDInsight-fürtöt használó alapértelmezett tárterület-fiókhoz tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="931b7-118">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="931b7-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="931b7-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="931b7-120">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="931b7-120">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="931b7-121">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="931b7-121">-Defines</span></span>
<span data-ttu-id="931b7-122">Itt adhatja meg a Hadoop konfigurációs értékeit a feladatok futásakor.</span><span class="sxs-lookup"><span data-stu-id="931b7-122">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="931b7-123">-Fájl</span><span class="sxs-lookup"><span data-stu-id="931b7-123">-File</span></span>
<span data-ttu-id="931b7-124">A futtatni kívánt lekérdezést tartalmazó Azure-tárterületen lévő fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="931b7-124">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="931b7-125">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="931b7-125">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="931b7-126">-Files</span><span class="sxs-lookup"><span data-stu-id="931b7-126">-Files</span></span>
<span data-ttu-id="931b7-127">A kaptár-feladathoz szükséges fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="931b7-127">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="931b7-128">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="931b7-128">-JobName</span></span>
<span data-ttu-id="931b7-129">A kaptár-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="931b7-129">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="931b7-130">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett értéket használja: "kaptár: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="931b7-130">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="931b7-131">-Query</span><span class="sxs-lookup"><span data-stu-id="931b7-131">-Query</span></span>
<span data-ttu-id="931b7-132">A kaptár-lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="931b7-132">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="931b7-133">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="931b7-133">-RunAsFileJob</span></span>
<span data-ttu-id="931b7-134">Jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure Storage-fiókban, amelyben a lekérdezés tárolható.</span><span class="sxs-lookup"><span data-stu-id="931b7-134">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="931b7-135">Ez a parancsmag elküldi azt a feladatot, amely parancsfájlként hivatkozik erre a fájlra.</span><span class="sxs-lookup"><span data-stu-id="931b7-135">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="931b7-136">Ezt a funkciót speciális karakterek (például százalék (%)) kezelésére használhatja. Ez a Templeton-on keresztül sikertelen volt, mert a Templeton URL-ként értelmezi a százalékos jellel ellátni kívánt lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="931b7-136">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="931b7-137">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="931b7-137">-StatusFolder</span></span>
<span data-ttu-id="931b7-138">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="931b7-138">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="931b7-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931b7-139">-DefaultProfile</span></span>
<span data-ttu-id="931b7-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="931b7-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="931b7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931b7-141">CommonParameters</span></span>
<span data-ttu-id="931b7-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="931b7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931b7-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931b7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931b7-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="931b7-144">INPUTS</span></span>

## <span data-ttu-id="931b7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="931b7-145">OUTPUTS</span></span>

### <span data-ttu-id="931b7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="931b7-146">System.String</span></span>

## <span data-ttu-id="931b7-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="931b7-147">NOTES</span></span>

## <span data-ttu-id="931b7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="931b7-148">RELATED LINKS</span></span>

[<span data-ttu-id="931b7-149">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="931b7-149">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)

