---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: e7e873638e38ed8c0c561fce5c4cd425be7bafbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939177"
---
# <span data-ttu-id="db0bc-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="db0bc-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="db0bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="db0bc-103">Synapse Analytics Spark munkamenetet kezd.</span><span class="sxs-lookup"><span data-stu-id="db0bc-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="db0bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db0bc-104">SYNTAX</span></span>

### <span data-ttu-id="db0bc-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db0bc-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db0bc-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db0bc-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db0bc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db0bc-107">DESCRIPTION</span></span>
<span data-ttu-id="db0bc-108">A **Start-AzSynapseSparkSession** parancsmag elindítja a Synapse Analytics Spark munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="db0bc-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="db0bc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db0bc-109">EXAMPLES</span></span>

### <span data-ttu-id="db0bc-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="db0bc-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="db0bc-111">Ez a parancs elindít egy Azure Synapse Analytics Spark munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="db0bc-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="db0bc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="db0bc-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="db0bc-113">Ez a parancs elindít egy Azure Synapse Analytics Spark-munkamenetet a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="db0bc-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="db0bc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db0bc-114">PARAMETERS</span></span>

### <span data-ttu-id="db0bc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db0bc-115">-AsJob</span></span>
<span data-ttu-id="db0bc-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="db0bc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db0bc-117">- Konfiguráció</span><span class="sxs-lookup"><span data-stu-id="db0bc-117">-Configuration</span></span>
<span data-ttu-id="db0bc-118">Spark configuration properties.</span><span class="sxs-lookup"><span data-stu-id="db0bc-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="db0bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0bc-119">-DefaultProfile</span></span>
<span data-ttu-id="db0bc-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db0bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db0bc-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="db0bc-121">-ExecutorCount</span></span>
<span data-ttu-id="db0bc-122">A feladathoz a megadott értékgörbekészletben kiosztandó végrehajtók száma.</span><span class="sxs-lookup"><span data-stu-id="db0bc-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="db0bc-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="db0bc-123">-ExecutorSize</span></span>
<span data-ttu-id="db0bc-124">A feladathoz a megadott Értékgörbekészletben kiosztott végrehajtók számára használt alapértékek és memória száma.</span><span class="sxs-lookup"><span data-stu-id="db0bc-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="db0bc-125">-Language</span><span class="sxs-lookup"><span data-stu-id="db0bc-125">-Language</span></span>
<span data-ttu-id="db0bc-126">A végrehajtási kód nyelve.</span><span class="sxs-lookup"><span data-stu-id="db0bc-126">Language of the execution code.</span></span>

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

### <span data-ttu-id="db0bc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="db0bc-127">-Name</span></span>
<span data-ttu-id="db0bc-128">A Spark-munkamenet neve.</span><span class="sxs-lookup"><span data-stu-id="db0bc-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="db0bc-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="db0bc-129">-ReferenceFile</span></span>
<span data-ttu-id="db0bc-130">A fődefiníciós fájlban hivatkozásként használt további fájlok.</span><span class="sxs-lookup"><span data-stu-id="db0bc-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="db0bc-131">Vesszővel elválasztott tároló URI-lista.</span><span class="sxs-lookup"><span data-stu-id="db0bc-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="db0bc-132">pl. " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="db0bc-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="db0bc-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="db0bc-133">-SparkPoolName</span></span>
<span data-ttu-id="db0bc-134">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="db0bc-134">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="db0bc-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="db0bc-135">-SparkPoolObject</span></span>
<span data-ttu-id="db0bc-136">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="db0bc-136">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="db0bc-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db0bc-137">-WorkspaceName</span></span>
<span data-ttu-id="db0bc-138">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="db0bc-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="db0bc-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db0bc-139">-Confirm</span></span>
<span data-ttu-id="db0bc-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db0bc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db0bc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db0bc-141">-WhatIf</span></span>
<span data-ttu-id="db0bc-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db0bc-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db0bc-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db0bc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db0bc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0bc-144">CommonParameters</span></span>
<span data-ttu-id="db0bc-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db0bc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0bc-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db0bc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0bc-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db0bc-147">INPUTS</span></span>

### <span data-ttu-id="db0bc-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="db0bc-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="db0bc-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db0bc-149">OUTPUTS</span></span>

### <span data-ttu-id="db0bc-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="db0bc-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="db0bc-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db0bc-151">NOTES</span></span>

## <span data-ttu-id="db0bc-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db0bc-152">RELATED LINKS</span></span>
