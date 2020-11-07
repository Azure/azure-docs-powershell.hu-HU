---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 0e287922c692a8271a82a62f20539bb97518b9f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679771"
---
# <span data-ttu-id="694e4-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="694e4-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="694e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="694e4-102">SYNOPSIS</span></span>
<span data-ttu-id="694e4-103">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="694e4-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="694e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="694e4-104">SYNTAX</span></span>

### <span data-ttu-id="694e4-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="694e4-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="694e4-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="694e4-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="694e4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="694e4-107">DESCRIPTION</span></span>
<span data-ttu-id="694e4-108">Az **Add-AzureRmHDInsightConfigValues** parancsmag olyan Hadoop-konfigurációt ad hozzá, mint például core-site.xml vagy hive-site.xml, és/vagy egy, a New-AzureRmHDInsightClusterConfig parancsmag által létrehozott HDInsight konfigurációs objektumhoz tartozó kaptár megosztott tár.</span><span class="sxs-lookup"><span data-stu-id="694e4-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="694e4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="694e4-109">EXAMPLES</span></span>

### <span data-ttu-id="694e4-110">Példa 1: egyéni konfigurációs érték hozzáadása a cluster Configuration objektumhoz</span><span class="sxs-lookup"><span data-stu-id="694e4-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="694e4-111">A parancs hozzáadja a Hadoop konfigurációs értékét a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="694e4-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="694e4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="694e4-112">PARAMETERS</span></span>

### <span data-ttu-id="694e4-113">-Config</span><span class="sxs-lookup"><span data-stu-id="694e4-113">-Config</span></span>
<span data-ttu-id="694e4-114">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="694e4-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="694e4-115">Ezt az objektumot az New-AzureRmHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="694e4-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="694e4-116">-Core</span><span class="sxs-lookup"><span data-stu-id="694e4-116">-Core</span></span>
<span data-ttu-id="694e4-117">A HDInsight-fürt fő webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="694e4-118">-HBaseEnv</span></span>
<span data-ttu-id="694e4-119">A HDInsight-HBase env-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="694e4-120">-HBaseSite</span></span>
<span data-ttu-id="694e4-121">A HDInsight-fürt HBase-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="694e4-122">-Hdfs</span></span>
<span data-ttu-id="694e4-123">A HDInsight-fürt HDFS-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="694e4-124">-HiveEnv</span></span>
<span data-ttu-id="694e4-125">A HDInsight-fürt kaptár env konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="694e4-126">-HiveSite</span></span>
<span data-ttu-id="694e4-127">A HDInsight-fürt kaptár-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="694e4-128">-MapRed</span></span>
<span data-ttu-id="694e4-129">A HDInsight-fürt MapRed-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="694e4-130">-OozieEnv</span></span>
<span data-ttu-id="694e4-131">A HDInsight-Oozie env-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="694e4-132">-OozieSite</span></span>
<span data-ttu-id="694e4-133">A HDInsight-fürt Oozie-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="694e4-134">-RServer</span></span>
<span data-ttu-id="694e4-135">A RServer-konfigurációkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="694e4-136">Csak RServer-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="694e4-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="694e4-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="694e4-137">-Spark2Defaults</span></span>
<span data-ttu-id="694e4-138">A HDInsight-fürt Spark2 alapértelmezett konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694e4-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="694e4-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="694e4-140">Itt adhatja meg a HDInsight-Spark2 gazdaságossági SparkConf-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="694e4-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694e4-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="694e4-141">-SparkDefaults</span></span>
<span data-ttu-id="694e4-142">A HDInsight-fürt szikra alapértelmezett konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694e4-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="694e4-143">-SparkThriftConf</span></span>
<span data-ttu-id="694e4-144">A HDInsight-fürt SparkConf-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694e4-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="694e4-145">-Storm</span></span>
<span data-ttu-id="694e4-146">A HDInsight-fürt viharos webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="694e4-147">-Tez</span></span>
<span data-ttu-id="694e4-148">A HDInsight-fürt TEZ-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="694e4-149">-WebHCat</span></span>
<span data-ttu-id="694e4-150">A HDInsight-fürt WebHCat-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-151">-Fonal</span><span class="sxs-lookup"><span data-stu-id="694e4-151">-Yarn</span></span>
<span data-ttu-id="694e4-152">A HDInsight-fürt fonal-webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="694e4-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="694e4-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694e4-153">-DefaultProfile</span></span>
<span data-ttu-id="694e4-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="694e4-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="694e4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694e4-155">CommonParameters</span></span>
<span data-ttu-id="694e4-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="694e4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694e4-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694e4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694e4-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="694e4-158">INPUTS</span></span>

### <span data-ttu-id="694e4-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="694e4-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="694e4-160">A "config" paraméter elfogadja a "AzureHDInsightConfig" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="694e4-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="694e4-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="694e4-161">OUTPUTS</span></span>

### <span data-ttu-id="694e4-162">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="694e4-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="694e4-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="694e4-163">NOTES</span></span>

## <span data-ttu-id="694e4-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="694e4-164">RELATED LINKS</span></span>

[<span data-ttu-id="694e4-165">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="694e4-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


