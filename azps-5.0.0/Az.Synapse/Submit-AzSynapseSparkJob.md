---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195458"
---
# <span data-ttu-id="b8653-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b8653-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="b8653-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8653-102">SYNOPSIS</span></span>
<span data-ttu-id="b8653-103">Elküldhet egy szinapszis-elemző szikra munkát.</span><span class="sxs-lookup"><span data-stu-id="b8653-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="b8653-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8653-104">SYNTAX</span></span>

### <span data-ttu-id="b8653-105">RunSparkJobParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8653-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8653-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8653-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8653-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8653-107">DESCRIPTION</span></span>
<span data-ttu-id="b8653-108">A **Submit-AzSynapseSparkJob** parancsmag egy szinapszis-elemzési Spark-feladatot terjeszt elő.</span><span class="sxs-lookup"><span data-stu-id="b8653-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="b8653-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b8653-109">EXAMPLES</span></span>

### <span data-ttu-id="b8653-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b8653-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="b8653-111">Ez a parancs a szinapszis-elemző szikra munkahelyét továbbítja.</span><span class="sxs-lookup"><span data-stu-id="b8653-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="b8653-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="b8653-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="b8653-113">Ez a parancs a szinapszis Analytics Spark .NET-feladatot továbbítja.</span><span class="sxs-lookup"><span data-stu-id="b8653-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="b8653-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="b8653-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="b8653-115">Ez a parancs a szinapszis Analytics PySpark-feladatot eljuttatja.</span><span class="sxs-lookup"><span data-stu-id="b8653-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="b8653-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8653-116">PARAMETERS</span></span>

### <span data-ttu-id="b8653-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="b8653-117">-CommandLineArgument</span></span>
<span data-ttu-id="b8653-118">Nem kötelező argumentumok a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="b8653-118">Optional arguments to the job.</span></span> <span data-ttu-id="b8653-119">például "---ismétlési 10000 –--időkorlát" 20-as "</span><span class="sxs-lookup"><span data-stu-id="b8653-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="b8653-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="b8653-120">-Configuration</span></span>
<span data-ttu-id="b8653-121">A szikra konfigurációjának tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="b8653-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="b8653-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8653-122">-DefaultProfile</span></span>
<span data-ttu-id="b8653-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8653-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8653-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="b8653-124">-ExecutorCount</span></span>
<span data-ttu-id="b8653-125">A projekthez megadott Spark-készletben kiosztani kívánt kivitelezők száma.</span><span class="sxs-lookup"><span data-stu-id="b8653-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="b8653-126">-ExecutorSize</span></span>
<span data-ttu-id="b8653-127">A projekthez megadott Spark-készletben kiosztott végrehajtók számára használandó alapvető és memória száma.</span><span class="sxs-lookup"><span data-stu-id="b8653-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-128">-Nyelv</span><span class="sxs-lookup"><span data-stu-id="b8653-128">-Language</span></span>
<span data-ttu-id="b8653-129">A elküldeni kívánt feladat nyelve.</span><span class="sxs-lookup"><span data-stu-id="b8653-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="b8653-130">-MainClassName</span></span>
<span data-ttu-id="b8653-131">A teljes mértékben minősített azonosító vagy a fő kategória a fő definíciós fájlban.</span><span class="sxs-lookup"><span data-stu-id="b8653-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="b8653-132">A Spark és a .NET Spark feladatához szükséges.</span><span class="sxs-lookup"><span data-stu-id="b8653-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="b8653-133">például "org. Apache. Spark. examples. SparkPi"</span><span class="sxs-lookup"><span data-stu-id="b8653-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b8653-134">-MainDefinitionFile</span></span>
<span data-ttu-id="b8653-135">A projekthez használt fő fájl.</span><span class="sxs-lookup"><span data-stu-id="b8653-135">The main file used for the job.</span></span>
<span data-ttu-id="b8653-136">például " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="b8653-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8653-137">-Name</span></span>
<span data-ttu-id="b8653-138">A szikra munkahelyének neve.</span><span class="sxs-lookup"><span data-stu-id="b8653-138">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="b8653-139">-ReferenceFile</span></span>
<span data-ttu-id="b8653-140">A fő definíciós fájlban való hivatkozáshoz használt további fájlok.</span><span class="sxs-lookup"><span data-stu-id="b8653-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="b8653-141">Vesszővel elválasztott tárolási URI-lista.</span><span class="sxs-lookup"><span data-stu-id="b8653-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="b8653-142">például " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="b8653-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="b8653-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b8653-143">-SparkPoolName</span></span>
<span data-ttu-id="b8653-144">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="b8653-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="b8653-145">-SparkPoolObject</span></span>
<span data-ttu-id="b8653-146">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="b8653-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b8653-147">-WorkspaceName</span></span>
<span data-ttu-id="b8653-148">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="b8653-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8653-149">-Confirm</span></span>
<span data-ttu-id="b8653-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8653-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8653-151">-WhatIf</span></span>
<span data-ttu-id="b8653-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8653-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8653-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8653-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8653-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8653-154">CommonParameters</span></span>
<span data-ttu-id="b8653-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8653-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8653-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8653-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8653-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8653-157">INPUTS</span></span>

### <span data-ttu-id="b8653-158">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b8653-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="b8653-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8653-159">OUTPUTS</span></span>

### <span data-ttu-id="b8653-160">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b8653-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="b8653-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8653-161">NOTES</span></span>

## <span data-ttu-id="b8653-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8653-162">RELATED LINKS</span></span>
