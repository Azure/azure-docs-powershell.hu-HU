---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: d5179bd15212e2d5bfa7eb5d903b2c37620ffb23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938114"
---
# <span data-ttu-id="88905-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="88905-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="88905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88905-102">SYNOPSIS</span></span>
<span data-ttu-id="88905-103">A Hadoop konfigurációs értékének és/vagy a Hive-tárak megosztott testreszabásának hozzáadása a fürtkonfigurációs objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="88905-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="88905-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="88905-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88905-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="88905-105">DESCRIPTION</span></span>
<span data-ttu-id="88905-106">Az **Add-AzHDInsightConfigValue** parancsmag hozzáadja a Hadoop konfigurációs érték (például core-site.xml vagy hive-site.xml) és/vagy a Hive megosztott tár testreszabását a New-AzHDInsightClusterConfig parancsmag által létrehozott HDInsight konfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="88905-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="88905-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="88905-107">EXAMPLES</span></span>

### <span data-ttu-id="88905-108">1. példa: Egyéni konfigurációs érték hozzáadása a fürt konfigurációs objektumához</span><span class="sxs-lookup"><span data-stu-id="88905-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="88905-109">Ez a parancs hozzáad egy Hadoop konfigurációs értéket a "saját-hadoop-001" nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="88905-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="88905-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88905-110">PARAMETERS</span></span>

### <span data-ttu-id="88905-111">-Config</span><span class="sxs-lookup"><span data-stu-id="88905-111">-Config</span></span>
<span data-ttu-id="88905-112">Ez a parancsmag által módosított HDInsight-fürtkonfigurációs objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="88905-113">Ezt az objektumot a New-AzHDInsightClusterConfig hozta létre.</span><span class="sxs-lookup"><span data-stu-id="88905-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="88905-114">-Core</span><span class="sxs-lookup"><span data-stu-id="88905-114">-Core</span></span>
<span data-ttu-id="88905-115">A HDInsight-fürt alapvető webhelykonfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88905-116">-DefaultProfile</span></span>
<span data-ttu-id="88905-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="88905-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88905-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="88905-118">-HBaseEnv</span></span>
<span data-ttu-id="88905-119">A HDInsight-fürt HBase Env-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="88905-120">-HBaseSite</span></span>
<span data-ttu-id="88905-121">A HDInsight-fürt HBase-webhelykonfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="88905-122">-Hdfs</span></span>
<span data-ttu-id="88905-123">A HDInsight-fürt HDFS-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="88905-124">-HiveEnv</span></span>
<span data-ttu-id="88905-125">A HDInsight-fürt Hive Env-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="88905-126">-HiveSite</span></span>
<span data-ttu-id="88905-127">A HDInsight-fürt Hive-webhely-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="88905-128">-MapRed</span></span>
<span data-ttu-id="88905-129">A HDInsight-fürt MapRed-webhelykonfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="88905-130">-OozieEnv</span></span>
<span data-ttu-id="88905-131">A HDInsight-fürt Oozie Env-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="88905-132">-OozieSite</span></span>
<span data-ttu-id="88905-133">A HDInsight-fürt Oozie-webhelykonfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="88905-134">-RServer</span></span>
<span data-ttu-id="88905-135">Az RServer-konfigurációkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="88905-136">Csak RServer-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="88905-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="88905-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="88905-137">-Spark2Defaults</span></span>
<span data-ttu-id="88905-138">A HdInsight-fürt Spark2 alapértelmezett konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="88905-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="88905-140">A HDInsight-fürt Spark2 Thrift SparkConf-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="88905-141">-SparkDefaults</span></span>
<span data-ttu-id="88905-142">A HDInsight-fürt Spark Defaults (Értékgörbe) beállítása.</span><span class="sxs-lookup"><span data-stu-id="88905-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="88905-143">-SparkThriftConf</span></span>
<span data-ttu-id="88905-144">A HDInsight-fürt Spark Thrift SparkConf-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="88905-145">-Storm</span></span>
<span data-ttu-id="88905-146">A HdInsight-fürthöz a Storm Site konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="88905-147">-Tez</span></span>
<span data-ttu-id="88905-148">A Tez-webhely konfigurációját adja meg ennek a HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="88905-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="88905-149">-WebHCat</span></span>
<span data-ttu-id="88905-150">Ez a HDInsight-fürt WebHCat-webhelykonfigurációit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="88905-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-151">– Sivad</span><span class="sxs-lookup"><span data-stu-id="88905-151">-Yarn</span></span>
<span data-ttu-id="88905-152">Ennek a HDInsight-fürtnek a KELLÉK-webhelykonfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="88905-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="88905-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88905-153">CommonParameters</span></span>
<span data-ttu-id="88905-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88905-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88905-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88905-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88905-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88905-156">INPUTS</span></span>

### <span data-ttu-id="88905-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="88905-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="88905-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88905-158">OUTPUTS</span></span>

### <span data-ttu-id="88905-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="88905-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="88905-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="88905-160">NOTES</span></span>

## <span data-ttu-id="88905-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88905-161">RELATED LINKS</span></span>

[<span data-ttu-id="88905-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="88905-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


