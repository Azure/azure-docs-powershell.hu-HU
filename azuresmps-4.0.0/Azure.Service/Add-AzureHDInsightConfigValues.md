---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015728"
---
# <span data-ttu-id="62722-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="62722-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="62722-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62722-102">SYNOPSIS</span></span>
<span data-ttu-id="62722-103">A Hadoop konfigurációs érték testreszabása vagy a kaptár megosztott tár testreszabása HDInsight-fürtkonfiguráció beállítással.</span><span class="sxs-lookup"><span data-stu-id="62722-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="62722-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62722-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="62722-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62722-105">DESCRIPTION</span></span>
<span data-ttu-id="62722-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="62722-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="62722-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="62722-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="62722-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="62722-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="62722-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell használatával HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)című témakört.</span><span class="sxs-lookup"><span data-stu-id="62722-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="62722-110">Ha többet szeretne tudni arról, hogy miként küldhet feladatokat az Azure PowerShell és más megközelítések segítségével, olvassa el [az Hadoop-feladatok elküldése az HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="62722-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="62722-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight-parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62722-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="62722-112">Az **Add-AzureHDInsightConfigValues** parancsmag Hadoop-konfigurációt (például Core-site.xml vagy Hive-site.xml) ad hozzá, vagy egy, az Azure HDInsight cluster konfigurációjának megfelelő megosztott tár-testreszabást.</span><span class="sxs-lookup"><span data-stu-id="62722-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="62722-113">A parancsmag egyéni konfigurációs értékeket ad egy megadott konfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="62722-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="62722-114">Az egyéni beállítások hozzáadódnak a megfelelő Hadoop-szolgáltatások konfigurációs fájljaihoz a fürt telepítésekor.</span><span class="sxs-lookup"><span data-stu-id="62722-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="62722-115">Példák</span><span class="sxs-lookup"><span data-stu-id="62722-115">EXAMPLES</span></span>

### <span data-ttu-id="62722-116">1. példa: fürt beállítása</span><span class="sxs-lookup"><span data-stu-id="62722-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="62722-117">Az első parancs létrehoz egy új **AzureHDInsightHiveConfiguration** objektumot, majd a $HiveConfigValues változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="62722-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="62722-118">A következő öt parancs a kaptár konfigurációs értékeit hozza létre, és az értékeket az $HiveConfigValues tagjaiként tárolja.</span><span class="sxs-lookup"><span data-stu-id="62722-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="62722-119">A hetedik parancs létrehoz egy **AzureHDInsightOozieConfiguration** objektumot, majd a $OozieConfigValues változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="62722-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="62722-120">A nyolcadik parancs létrehoz egy konfigurációs értéket a Oozie-hoz, majd az értékeket az $OozieConfigValues tagjaként tárolja.</span><span class="sxs-lookup"><span data-stu-id="62722-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="62722-121">A kilencedik parancs létrehoz egy **AzureHDInsightMapReduceConfiguration** objektumot, majd a $MapredConfigValues változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="62722-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="62722-122">A következő két parancs konfigurációs értékeket hoz létre a MapReduce, és ezeket az értékeket az $MapredConfigValues tagjaiként tárolja.</span><span class="sxs-lookup"><span data-stu-id="62722-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="62722-123">A tizenkettedik parancs a **New-AzureHDInsightClusterConfig** parancsmagot használja az HDInsight-beli fürtkonfiguráció létrehozásához, majd a $config változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="62722-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="62722-124">A parancs a pipeline operátor segítségével átadja $Config a **set-AzureHDInsightDefaultStorage** parancsmagnak, hogy frissítse az alapértelmezett tárterületet és az **Add-AzureHDInsightConfigValues** parancsmagot, hogy az új konfigurációs értékeket hozzáadja a fürtkonfiguráció beállításához.</span><span class="sxs-lookup"><span data-stu-id="62722-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="62722-125">A végleges parancs a pipeline operátor segítségével átadja $Configt a **New-AzureHDInsightCluster** parancsmagnak, hogy új HDInsight-fürtöt hozzon létre a testre szabott beállításokkal.</span><span class="sxs-lookup"><span data-stu-id="62722-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="62722-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62722-126">PARAMETERS</span></span>

### <span data-ttu-id="62722-127">-Config</span><span class="sxs-lookup"><span data-stu-id="62722-127">-Config</span></span>
<span data-ttu-id="62722-128">Annak a konfigurációs objektumnak a megadása, amelyhez Hadoop-konfigurációt kíván hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="62722-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62722-129">-Core</span><span class="sxs-lookup"><span data-stu-id="62722-129">-Core</span></span>
<span data-ttu-id="62722-130">A Core-site.xml Hadoop konfigurációs értékeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="62722-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="62722-131">-HBase</span></span>
<span data-ttu-id="62722-132">A Hbase-site.xml HBase konfigurációs értékeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="62722-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-133">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="62722-133">-Hdfs</span></span>
<span data-ttu-id="62722-134">A Hdfs-site.xml Hadoop konfigurációs értékeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="62722-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-135">-Kaptár</span><span class="sxs-lookup"><span data-stu-id="62722-135">-Hive</span></span>
<span data-ttu-id="62722-136">A Hadoop-kaptár szolgáltatás testreszabási objektumát adja meg, többek között a Hive-site.xml és a kaptár megosztott tárakra vonatkozó konfigurációs értékeket is.</span><span class="sxs-lookup"><span data-stu-id="62722-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="62722-137">-MapReduce</span></span>
<span data-ttu-id="62722-138">A MapReduce és a kapacitás-ütemező testreszabási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62722-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="62722-139">-Oozie</span></span>
<span data-ttu-id="62722-140">A Hadoop Oozie szolgáltatás testreszabási objektumát adja meg, többek között az Oozie-site.xml Hadoop konfigurációs értékeit is.</span><span class="sxs-lookup"><span data-stu-id="62722-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="62722-141">-Profile</span></span>
<span data-ttu-id="62722-142">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="62722-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62722-143">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="62722-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62722-144">-Szikra</span><span class="sxs-lookup"><span data-stu-id="62722-144">-Spark</span></span>
<span data-ttu-id="62722-145">Az Apache Spark testreszabási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62722-145">Specifies a customization object for Apache Spark.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-146">-Storm</span><span class="sxs-lookup"><span data-stu-id="62722-146">-Storm</span></span>
<span data-ttu-id="62722-147">Az Apache Storm testreszabási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62722-147">Specifies a customization object for Apache Storm.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-148">-Fonal</span><span class="sxs-lookup"><span data-stu-id="62722-148">-Yarn</span></span>
<span data-ttu-id="62722-149">A Hadoop-fonal testreszabási objektumát adja meg, amely a Yarn-site.xml egyéni fonal-konfigurációjának halmazát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62722-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62722-150">CommonParameters</span></span>
<span data-ttu-id="62722-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62722-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62722-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62722-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62722-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62722-153">INPUTS</span></span>

## <span data-ttu-id="62722-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62722-154">OUTPUTS</span></span>

## <span data-ttu-id="62722-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62722-155">NOTES</span></span>

## <span data-ttu-id="62722-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62722-156">RELATED LINKS</span></span>

[<span data-ttu-id="62722-157">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="62722-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="62722-158">Új – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="62722-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="62722-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="62722-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
