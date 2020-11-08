---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187958"
---
# <span data-ttu-id="3c8a5-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3c8a5-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="3c8a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8a5-103">Elindítja a szinapszis-elemző szikra-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3c8a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c8a5-104">SYNTAX</span></span>

### <span data-ttu-id="3c8a5-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c8a5-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8a5-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c8a5-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c8a5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c8a5-107">DESCRIPTION</span></span>
<span data-ttu-id="3c8a5-108">A **Start-AzSynapseSparkSession** parancsmag a szinapszis-elemző Spark-munkamenetet indítja el.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3c8a5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3c8a5-109">EXAMPLES</span></span>

### <span data-ttu-id="3c8a5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3c8a5-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="3c8a5-111">Ez a parancs elindítja az Azure szinapszis Analytics Spark-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="3c8a5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3c8a5-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="3c8a5-113">Ez a parancs elindítja az Azure szinapszis Analytics Spark-munkamenetet a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="3c8a5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c8a5-114">PARAMETERS</span></span>

### <span data-ttu-id="3c8a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c8a5-115">-AsJob</span></span>
<span data-ttu-id="3c8a5-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3c8a5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c8a5-117">-Configuration</span><span class="sxs-lookup"><span data-stu-id="3c8a5-117">-Configuration</span></span>
<span data-ttu-id="3c8a5-118">A szikra konfigurációjának tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="3c8a5-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="3c8a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8a5-119">-DefaultProfile</span></span>
<span data-ttu-id="3c8a5-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c8a5-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="3c8a5-121">-ExecutorCount</span></span>
<span data-ttu-id="3c8a5-122">A projekthez megadott Spark-készletben kiosztani kívánt kivitelezők száma.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="3c8a5-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="3c8a5-123">-ExecutorSize</span></span>
<span data-ttu-id="3c8a5-124">A projekthez megadott Spark-készletben kiosztott végrehajtók számára használandó alapvető és memória száma.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="3c8a5-125">-Nyelv</span><span class="sxs-lookup"><span data-stu-id="3c8a5-125">-Language</span></span>
<span data-ttu-id="3c8a5-126">A végrehajtási kód nyelve.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a5-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c8a5-127">-Name</span></span>
<span data-ttu-id="3c8a5-128">A szikra munkamenet neve</span><span class="sxs-lookup"><span data-stu-id="3c8a5-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="3c8a5-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="3c8a5-129">-ReferenceFile</span></span>
<span data-ttu-id="3c8a5-130">A fő definíciós fájlban való hivatkozáshoz használt további fájlok.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="3c8a5-131">Vesszővel elválasztott tárolási URI-lista.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="3c8a5-132">például " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="3c8a5-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="3c8a5-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3c8a5-133">-SparkPoolName</span></span>
<span data-ttu-id="3c8a5-134">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a5-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3c8a5-135">-SparkPoolObject</span></span>
<span data-ttu-id="3c8a5-136">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a5-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3c8a5-137">-WorkspaceName</span></span>
<span data-ttu-id="3c8a5-138">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a5-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c8a5-139">-Confirm</span></span>
<span data-ttu-id="3c8a5-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c8a5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c8a5-141">-WhatIf</span></span>
<span data-ttu-id="3c8a5-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c8a5-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c8a5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8a5-144">CommonParameters</span></span>
<span data-ttu-id="3c8a5-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c8a5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8a5-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8a5-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c8a5-147">INPUTS</span></span>

### <span data-ttu-id="3c8a5-148">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3c8a5-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="3c8a5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c8a5-149">OUTPUTS</span></span>

### <span data-ttu-id="3c8a5-150">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3c8a5-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="3c8a5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c8a5-151">NOTES</span></span>

## <span data-ttu-id="3c8a5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c8a5-152">RELATED LINKS</span></span>