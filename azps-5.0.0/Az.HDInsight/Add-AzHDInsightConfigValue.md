---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185391"
---
# <span data-ttu-id="4e6ee-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="4e6ee-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="4e6ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6ee-103">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="4e6ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e6ee-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e6ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e6ee-105">DESCRIPTION</span></span>
<span data-ttu-id="4e6ee-106">Az **Add-AzHDInsightConfigValue** parancsmag olyan Hadoop-konfigurációt ad hozzá, mint például core-site.xml vagy hive-site.xml, és/vagy egy, a New-AzHDInsightClusterConfig parancsmag által létrehozott HDInsight konfigurációs objektumhoz tartozó kaptár megosztott tár.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4e6ee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4e6ee-107">EXAMPLES</span></span>

### <span data-ttu-id="4e6ee-108">Példa 1: egyéni konfigurációs érték hozzáadása a cluster Configuration objektumhoz</span><span class="sxs-lookup"><span data-stu-id="4e6ee-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="4e6ee-109">A parancs hozzáadja a Hadoop konfigurációs értékét a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4e6ee-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e6ee-110">PARAMETERS</span></span>

### <span data-ttu-id="4e6ee-111">-Config</span><span class="sxs-lookup"><span data-stu-id="4e6ee-111">-Config</span></span>
<span data-ttu-id="4e6ee-112">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4e6ee-113">Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="4e6ee-114">-Core</span><span class="sxs-lookup"><span data-stu-id="4e6ee-114">-Core</span></span>
<span data-ttu-id="4e6ee-115">A HDInsight-fürt fő webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6ee-116">-DefaultProfile</span></span>
<span data-ttu-id="4e6ee-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4e6ee-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e6ee-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="4e6ee-118">-HBaseEnv</span></span>
<span data-ttu-id="4e6ee-119">A HDInsight-HBase env-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="4e6ee-120">-HBaseSite</span></span>
<span data-ttu-id="4e6ee-121">A HDInsight-fürt HBase-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="4e6ee-122">-Hdfs</span></span>
<span data-ttu-id="4e6ee-123">A HDInsight-fürt HDFS-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="4e6ee-124">-HiveEnv</span></span>
<span data-ttu-id="4e6ee-125">A HDInsight-fürt kaptár env konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="4e6ee-126">-HiveSite</span></span>
<span data-ttu-id="4e6ee-127">A HDInsight-fürt kaptár-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="4e6ee-128">-MapRed</span></span>
<span data-ttu-id="4e6ee-129">A HDInsight-fürt MapRed-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="4e6ee-130">-OozieEnv</span></span>
<span data-ttu-id="4e6ee-131">A HDInsight-Oozie env-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="4e6ee-132">-OozieSite</span></span>
<span data-ttu-id="4e6ee-133">A HDInsight-fürt Oozie-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="4e6ee-134">-RServer</span></span>
<span data-ttu-id="4e6ee-135">A RServer-konfigurációkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="4e6ee-136">Csak RServer-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4e6ee-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="4e6ee-137">-Spark2Defaults</span></span>
<span data-ttu-id="4e6ee-138">A HDInsight-fürt Spark2 alapértelmezett konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="4e6ee-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="4e6ee-140">Itt adhatja meg a HDInsight-Spark2 gazdaságossági SparkConf-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="4e6ee-141">-SparkDefaults</span></span>
<span data-ttu-id="4e6ee-142">A HDInsight-fürt szikra alapértelmezett konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="4e6ee-143">-SparkThriftConf</span></span>
<span data-ttu-id="4e6ee-144">A HDInsight-fürt SparkConf-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="4e6ee-145">-Storm</span></span>
<span data-ttu-id="4e6ee-146">A HDInsight-fürt viharos webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="4e6ee-147">-Tez</span></span>
<span data-ttu-id="4e6ee-148">A HDInsight-fürt TEZ-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="4e6ee-149">-WebHCat</span></span>
<span data-ttu-id="4e6ee-150">A HDInsight-fürt WebHCat-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-151">-Fonal</span><span class="sxs-lookup"><span data-stu-id="4e6ee-151">-Yarn</span></span>
<span data-ttu-id="4e6ee-152">A HDInsight-fürt fonal-webhelyének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4e6ee-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6ee-153">CommonParameters</span></span>
<span data-ttu-id="4e6ee-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e6ee-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6ee-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6ee-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e6ee-156">INPUTS</span></span>

### <span data-ttu-id="4e6ee-157">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4e6ee-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4e6ee-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e6ee-158">OUTPUTS</span></span>

### <span data-ttu-id="4e6ee-159">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4e6ee-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4e6ee-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e6ee-160">NOTES</span></span>

## <span data-ttu-id="4e6ee-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e6ee-161">RELATED LINKS</span></span>

[<span data-ttu-id="4e6ee-162">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4e6ee-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


