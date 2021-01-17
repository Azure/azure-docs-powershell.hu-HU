---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334709"
---
# <span data-ttu-id="9dc02-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="9dc02-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="9dc02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dc02-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc02-103">Alaphelyzetbe állítja a Synapse Analytics Spark munkamenet időkorlátját.</span><span class="sxs-lookup"><span data-stu-id="9dc02-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9dc02-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9dc02-104">SYNTAX</span></span>

### <span data-ttu-id="9dc02-105">ResetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9dc02-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dc02-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dc02-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dc02-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dc02-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc02-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9dc02-108">DESCRIPTION</span></span>
<span data-ttu-id="9dc02-109">A **Remove-AzSynapseSparkSessionTimeout** parancsmag alaphelyzetbe állítja a Synapse Analytics Spark munkamenet időtúllépését.</span><span class="sxs-lookup"><span data-stu-id="9dc02-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9dc02-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9dc02-110">EXAMPLES</span></span>

### <span data-ttu-id="9dc02-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9dc02-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="9dc02-112">Ez a parancs alaphelyzetbe állítja a Synapse Analytics Spark munkamenet időtúllépését a megadott y azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="9dc02-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="9dc02-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9dc02-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="9dc02-114">Ez a parancs alaphelyzetbe állítja a Synapse Analytics Spark munkamenet időtúllépését a megadott y azonosítóval a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="9dc02-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="9dc02-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="9dc02-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="9dc02-116">Ez a parancs alaphelyzetbe állítja a Synapse Analytics Spark munkamenet időtúllépését a megadott y azonosítóval a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="9dc02-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="9dc02-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dc02-117">PARAMETERS</span></span>

### <span data-ttu-id="9dc02-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dc02-118">-AsJob</span></span>
<span data-ttu-id="9dc02-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9dc02-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dc02-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc02-120">-DefaultProfile</span></span>
<span data-ttu-id="9dc02-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dc02-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dc02-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dc02-122">-InputObject</span></span>
<span data-ttu-id="9dc02-123">Spark session input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="9dc02-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc02-124">-SiyId</span><span class="sxs-lookup"><span data-stu-id="9dc02-124">-LivyId</span></span>
<span data-ttu-id="9dc02-125">A Spark-munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9dc02-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc02-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dc02-126">-PassThru</span></span>
<span data-ttu-id="9dc02-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="9dc02-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9dc02-128">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="9dc02-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9dc02-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9dc02-129">-SparkPoolName</span></span>
<span data-ttu-id="9dc02-130">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="9dc02-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc02-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9dc02-131">-SparkPoolObject</span></span>
<span data-ttu-id="9dc02-132">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="9dc02-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc02-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9dc02-133">-WorkspaceName</span></span>
<span data-ttu-id="9dc02-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9dc02-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc02-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dc02-135">-Confirm</span></span>
<span data-ttu-id="9dc02-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9dc02-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc02-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc02-137">-WhatIf</span></span>
<span data-ttu-id="9dc02-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9dc02-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc02-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9dc02-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc02-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc02-140">CommonParameters</span></span>
<span data-ttu-id="9dc02-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc02-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc02-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dc02-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc02-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dc02-143">INPUTS</span></span>

### <span data-ttu-id="9dc02-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9dc02-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="9dc02-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9dc02-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9dc02-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dc02-146">OUTPUTS</span></span>

### <span data-ttu-id="9dc02-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9dc02-147">System.Boolean</span></span>

## <span data-ttu-id="9dc02-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9dc02-148">NOTES</span></span>

## <span data-ttu-id="9dc02-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dc02-149">RELATED LINKS</span></span>
