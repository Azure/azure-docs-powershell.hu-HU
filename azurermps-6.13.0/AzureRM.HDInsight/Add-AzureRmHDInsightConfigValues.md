---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: dd577b5ae4aa61ff988b872bcd37eab1c911e6cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672612"
---
# <span data-ttu-id="42ae2-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="42ae2-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="42ae2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="42ae2-103">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="42ae2-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ae2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42ae2-104">SYNTAX</span></span>

### <span data-ttu-id="42ae2-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="42ae2-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42ae2-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="42ae2-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42ae2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="42ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="42ae2-108">Az **Add-AzureRmHDInsightConfigValues** parancsmag olyan Hadoop-konfigurációt ad hozzá, mint például core-site.xml vagy hive-site.xml, és/vagy egy, a New-AzureRmHDInsightClusterConfig parancsmag által létrehozott HDInsight konfigurációs objektumhoz tartozó kaptár megosztott tár.</span><span class="sxs-lookup"><span data-stu-id="42ae2-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="42ae2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="42ae2-109">EXAMPLES</span></span>

### <span data-ttu-id="42ae2-110">Példa 1: egyéni konfigurációs érték hozzáadása a cluster Configuration objektumhoz</span><span class="sxs-lookup"><span data-stu-id="42ae2-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="42ae2-111">A parancs hozzáadja a Hadoop konfigurációs értékét a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="42ae2-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="42ae2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42ae2-112">PARAMETERS</span></span>

### <span data-ttu-id="42ae2-113">-Config</span><span class="sxs-lookup"><span data-stu-id="42ae2-113">-Config</span></span>
<span data-ttu-id="42ae2-114">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="42ae2-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="42ae2-115">Ezt az objektumot az New-AzureRmHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="42ae2-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="42ae2-116">-Core</span><span class="sxs-lookup"><span data-stu-id="42ae2-116">-Core</span></span>
<span data-ttu-id="42ae2-117">A HDInsight-fürt fő webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ae2-118">-DefaultProfile</span></span>
<span data-ttu-id="42ae2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="42ae2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42ae2-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="42ae2-120">-HBaseEnv</span></span>
<span data-ttu-id="42ae2-121">A HDInsight-HBase env-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="42ae2-122">-HBaseSite</span></span>
<span data-ttu-id="42ae2-123">A HDInsight-fürt HBase-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-124">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="42ae2-124">-Hdfs</span></span>
<span data-ttu-id="42ae2-125">A HDInsight-fürt HDFS-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="42ae2-126">-HiveEnv</span></span>
<span data-ttu-id="42ae2-127">A HDInsight-fürt kaptár env konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="42ae2-128">-HiveSite</span></span>
<span data-ttu-id="42ae2-129">A HDInsight-fürt kaptár-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="42ae2-130">-MapRed</span></span>
<span data-ttu-id="42ae2-131">A HDInsight-fürt MapRed-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="42ae2-132">-OozieEnv</span></span>
<span data-ttu-id="42ae2-133">A HDInsight-Oozie env-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="42ae2-134">-OozieSite</span></span>
<span data-ttu-id="42ae2-135">A HDInsight-fürt Oozie-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="42ae2-136">-RServer</span></span>
<span data-ttu-id="42ae2-137">A RServer-konfigurációkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="42ae2-138">Csak RServer-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="42ae2-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="42ae2-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="42ae2-139">-Spark2Defaults</span></span>
<span data-ttu-id="42ae2-140">A HDInsight-fürt Spark2 alapértelmezett konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="42ae2-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="42ae2-142">Itt adhatja meg a HDInsight-Spark2 gazdaságossági SparkConf-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="42ae2-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="42ae2-143">-SparkDefaults</span></span>
<span data-ttu-id="42ae2-144">A HDInsight-fürt szikra alapértelmezett konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="42ae2-145">-SparkThriftConf</span></span>
<span data-ttu-id="42ae2-146">A HDInsight-fürt SparkConf-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-147">-Storm</span><span class="sxs-lookup"><span data-stu-id="42ae2-147">-Storm</span></span>
<span data-ttu-id="42ae2-148">A HDInsight-fürt viharos webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="42ae2-149">-Tez</span></span>
<span data-ttu-id="42ae2-150">A HDInsight-fürt TEZ-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="42ae2-151">-WebHCat</span></span>
<span data-ttu-id="42ae2-152">A HDInsight-fürt WebHCat-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-153">-Fonal</span><span class="sxs-lookup"><span data-stu-id="42ae2-153">-Yarn</span></span>
<span data-ttu-id="42ae2-154">A HDInsight-fürt fonal-webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42ae2-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="42ae2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ae2-155">CommonParameters</span></span>
<span data-ttu-id="42ae2-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42ae2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ae2-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ae2-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ae2-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42ae2-158">INPUTS</span></span>

### <span data-ttu-id="42ae2-159">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="42ae2-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="42ae2-160">Paraméterek: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42ae2-160">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="42ae2-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42ae2-161">OUTPUTS</span></span>

### <span data-ttu-id="42ae2-162">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="42ae2-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="42ae2-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42ae2-163">NOTES</span></span>

## <span data-ttu-id="42ae2-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42ae2-164">RELATED LINKS</span></span>

[<span data-ttu-id="42ae2-165">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="42ae2-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


