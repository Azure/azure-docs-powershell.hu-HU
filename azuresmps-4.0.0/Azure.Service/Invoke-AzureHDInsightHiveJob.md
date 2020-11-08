---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016248"
---
# <span data-ttu-id="555e2-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="555e2-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="555e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="555e2-102">SYNOPSIS</span></span>
<span data-ttu-id="555e2-103">A kaptár-lekérdezéseket egy HDInsight-fürtbe küldi, a lekérdezés végrehajtásának előrehaladását jeleníti meg, és a lekérdezés eredményét egy műveletben kapja.</span><span class="sxs-lookup"><span data-stu-id="555e2-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="555e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="555e2-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="555e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="555e2-105">DESCRIPTION</span></span>
<span data-ttu-id="555e2-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="555e2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="555e2-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="555e2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="555e2-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="555e2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="555e2-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="555e2-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="555e2-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="555e2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="555e2-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="555e2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="555e2-112">A **meghívó-AzureHDInsightHiveJob** parancsmag HDInsight-fürtökhöz küldi a kaptár-lekérdezéseket, a lekérdezés végrehajtásának előrehaladását jeleníti meg, és a lekérdezés eredményét egy műveletben kapja.</span><span class="sxs-lookup"><span data-stu-id="555e2-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="555e2-113">Ahhoz, hogy a HDInsight-fürtöt be szeretné állítani, a **AzureHDInsightHiveJob** futtatása előtt futtatnia kell az Use-AzureHDInsightCluster parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="555e2-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="555e2-114">Példák</span><span class="sxs-lookup"><span data-stu-id="555e2-114">EXAMPLES</span></span>

### <span data-ttu-id="555e2-115">1. példa: a kaptár-lekérdezés elterjesztése</span><span class="sxs-lookup"><span data-stu-id="555e2-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="555e2-116">Az első parancs a **use-AzureHDInsightCluster** parancsmaggal megadhatja a kaptár-lekérdezéshez használni kívánt fürtöt a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="555e2-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="555e2-117">A második parancs a **meghívott AzureHDInsightHiveJob** parancsmagot használja a kaptár lekérdezés elküldéséhez.</span><span class="sxs-lookup"><span data-stu-id="555e2-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="555e2-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="555e2-118">PARAMETERS</span></span>

### <span data-ttu-id="555e2-119">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="555e2-119">-Arguments</span></span>
<span data-ttu-id="555e2-120">Argumentumokat ad meg egy Hadoop-feladathoz.</span><span class="sxs-lookup"><span data-stu-id="555e2-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="555e2-121">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="555e2-121">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-122">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="555e2-122">-Defines</span></span>
<span data-ttu-id="555e2-123">Itt adhatja meg a Hadoop konfigurációs értékeit a feladatok futásakor.</span><span class="sxs-lookup"><span data-stu-id="555e2-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-124">-Fájl</span><span class="sxs-lookup"><span data-stu-id="555e2-124">-File</span></span>
<span data-ttu-id="555e2-125">A Windows Azure Storage blob (WASB) elérési útját adja meg a futtatandó lekérdezést tartalmazó Azure Blob-tárolóban lévő fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="555e2-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="555e2-126">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="555e2-126">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-127">-Files</span><span class="sxs-lookup"><span data-stu-id="555e2-127">-Files</span></span>
<span data-ttu-id="555e2-128">A kaptár-feladathoz szükséges fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="555e2-128">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-129">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="555e2-129">-JobName</span></span>
<span data-ttu-id="555e2-130">A kaptár-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="555e2-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="555e2-131">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett értéket használja: "kaptár: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="555e2-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="555e2-132">-Profile</span></span>
<span data-ttu-id="555e2-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="555e2-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="555e2-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="555e2-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-135">-Query</span><span class="sxs-lookup"><span data-stu-id="555e2-135">-Query</span></span>
<span data-ttu-id="555e2-136">A kaptár-lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="555e2-136">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="555e2-137">-RunAsFileJob</span></span>
<span data-ttu-id="555e2-138">Jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure Storage-fiókban, amelyben a lekérdezés tárolható.</span><span class="sxs-lookup"><span data-stu-id="555e2-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="555e2-139">Ez a parancsmag elküldi azt a feladatot, amely parancsfájlként hivatkozik erre a fájlra.</span><span class="sxs-lookup"><span data-stu-id="555e2-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="555e2-140">Ezt a funkciót speciális karakterek (például százalék (%)) kezelésére használhatja. Ez a Templeton-on keresztül sikertelen volt, mert a Templeton URL-ként értelmezi a százalékos jellel ellátni kívánt lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="555e2-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="555e2-141">-StatusFolder</span></span>
<span data-ttu-id="555e2-142">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.</span><span class="sxs-lookup"><span data-stu-id="555e2-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555e2-143">CommonParameters</span></span>
<span data-ttu-id="555e2-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="555e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555e2-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555e2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555e2-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="555e2-146">INPUTS</span></span>

## <span data-ttu-id="555e2-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="555e2-147">OUTPUTS</span></span>

## <span data-ttu-id="555e2-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="555e2-148">NOTES</span></span>

## <span data-ttu-id="555e2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="555e2-149">RELATED LINKS</span></span>

[<span data-ttu-id="555e2-150">Új – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="555e2-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="555e2-151">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="555e2-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


