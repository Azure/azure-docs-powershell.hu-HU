---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363298"
---
# <span data-ttu-id="89dc7-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="89dc7-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="89dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="89dc7-103">Leállítja a Synapse Analytics Spark munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="89dc7-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="89dc7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89dc7-104">SYNTAX</span></span>

### <span data-ttu-id="89dc7-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89dc7-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89dc7-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89dc7-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89dc7-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89dc7-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89dc7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89dc7-108">DESCRIPTION</span></span>
<span data-ttu-id="89dc7-109">A **Stop-AzSynapseSparkSession** parancsmag leállítja a Synapse Analytics Spark munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="89dc7-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="89dc7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89dc7-110">EXAMPLES</span></span>

### <span data-ttu-id="89dc7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="89dc7-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="89dc7-112">Ez a parancs leállítja a Synapse Analytics Spark munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="89dc7-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="89dc7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="89dc7-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="89dc7-114">Ez a parancs leállítja a Synapse Analytics Spark munkamenetet a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="89dc7-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="89dc7-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="89dc7-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="89dc7-116">Ez a parancs leállítja a Synapse Analytics Spark munkamenetet a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="89dc7-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="89dc7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89dc7-117">PARAMETERS</span></span>

### <span data-ttu-id="89dc7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89dc7-118">-AsJob</span></span>
<span data-ttu-id="89dc7-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="89dc7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89dc7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89dc7-120">-DefaultProfile</span></span>
<span data-ttu-id="89dc7-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89dc7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89dc7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89dc7-122">-InputObject</span></span>
<span data-ttu-id="89dc7-123">Spark session input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="89dc7-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89dc7-124">-SiyId</span><span class="sxs-lookup"><span data-stu-id="89dc7-124">-LivyId</span></span>
<span data-ttu-id="89dc7-125">A Spark-munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89dc7-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89dc7-126">-PassThru</span></span>
<span data-ttu-id="89dc7-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="89dc7-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="89dc7-128">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="89dc7-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="89dc7-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="89dc7-129">-SparkPoolName</span></span>
<span data-ttu-id="89dc7-130">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="89dc7-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc7-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="89dc7-131">-SparkPoolObject</span></span>
<span data-ttu-id="89dc7-132">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="89dc7-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89dc7-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89dc7-133">-WorkspaceName</span></span>
<span data-ttu-id="89dc7-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="89dc7-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89dc7-135">-Confirm</span></span>
<span data-ttu-id="89dc7-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89dc7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89dc7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89dc7-137">-WhatIf</span></span>
<span data-ttu-id="89dc7-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89dc7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89dc7-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89dc7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89dc7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89dc7-140">CommonParameters</span></span>
<span data-ttu-id="89dc7-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89dc7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89dc7-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89dc7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89dc7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89dc7-143">INPUTS</span></span>

### <span data-ttu-id="89dc7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="89dc7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="89dc7-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="89dc7-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="89dc7-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89dc7-146">OUTPUTS</span></span>

### <span data-ttu-id="89dc7-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89dc7-147">System.Boolean</span></span>

## <span data-ttu-id="89dc7-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89dc7-148">NOTES</span></span>

## <span data-ttu-id="89dc7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89dc7-149">RELATED LINKS</span></span>
