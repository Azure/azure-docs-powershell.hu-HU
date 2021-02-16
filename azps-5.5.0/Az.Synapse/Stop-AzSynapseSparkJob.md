---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162771"
---
# <span data-ttu-id="dc3db-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="dc3db-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="dc3db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3db-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3db-103">Megszakítja a Synapse Analytics Spark-feladatot.</span><span class="sxs-lookup"><span data-stu-id="dc3db-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="dc3db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dc3db-104">SYNTAX</span></span>

### <span data-ttu-id="dc3db-105">StopSparkByByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc3db-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc3db-106">StopSparkByByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc3db-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc3db-107">StopSparkByByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc3db-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc3db-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dc3db-108">DESCRIPTION</span></span>
<span data-ttu-id="dc3db-109">A **Stop-AzSynapseSpark Job** parancsmag megszakítja a Synapse Analytics Spark-feladatot.</span><span class="sxs-lookup"><span data-stu-id="dc3db-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="dc3db-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dc3db-110">EXAMPLES</span></span>

### <span data-ttu-id="dc3db-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="dc3db-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="dc3db-112">Ez a parancs megszakítja a Synapse Analytics Spark-feladatot.</span><span class="sxs-lookup"><span data-stu-id="dc3db-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="dc3db-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="dc3db-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="dc3db-114">Ez a parancs megszakítja a Synapse Analytics Spark-feladatot a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="dc3db-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="dc3db-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="dc3db-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="dc3db-116">Ez a parancs megszakítja a Synapse Analytics Spark-feladatot a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="dc3db-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="dc3db-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc3db-117">PARAMETERS</span></span>

### <span data-ttu-id="dc3db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3db-118">-DefaultProfile</span></span>
<span data-ttu-id="dc3db-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc3db-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc3db-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dc3db-120">-Force</span></span>
<span data-ttu-id="dc3db-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc3db-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dc3db-122">-SiyId</span><span class="sxs-lookup"><span data-stu-id="dc3db-122">-LivyId</span></span>
<span data-ttu-id="dc3db-123">Az értékgörbe-feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc3db-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3db-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc3db-124">-PassThru</span></span>
<span data-ttu-id="dc3db-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="dc3db-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="dc3db-126">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="dc3db-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dc3db-127">-SparkObject</span><span class="sxs-lookup"><span data-stu-id="dc3db-127">-SparkJobObject</span></span>
<span data-ttu-id="dc3db-128">Spark job input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc3db-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3db-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="dc3db-129">-SparkPoolName</span></span>
<span data-ttu-id="dc3db-130">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="dc3db-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3db-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="dc3db-131">-SparkPoolObject</span></span>
<span data-ttu-id="dc3db-132">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc3db-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3db-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dc3db-133">-WorkspaceName</span></span>
<span data-ttu-id="dc3db-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="dc3db-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3db-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc3db-135">-Confirm</span></span>
<span data-ttu-id="dc3db-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dc3db-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc3db-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc3db-137">-WhatIf</span></span>
<span data-ttu-id="dc3db-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dc3db-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc3db-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc3db-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc3db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3db-140">CommonParameters</span></span>
<span data-ttu-id="dc3db-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3db-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc3db-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3db-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc3db-143">INPUTS</span></span>

### <span data-ttu-id="dc3db-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="dc3db-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="dc3db-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="dc3db-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="dc3db-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc3db-146">OUTPUTS</span></span>

### <span data-ttu-id="dc3db-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc3db-147">System.Boolean</span></span>

## <span data-ttu-id="dc3db-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dc3db-148">NOTES</span></span>

## <span data-ttu-id="dc3db-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc3db-149">RELATED LINKS</span></span>
