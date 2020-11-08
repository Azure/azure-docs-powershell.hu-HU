---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182476"
---
# <span data-ttu-id="81bd2-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="81bd2-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="81bd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="81bd2-103">A szinapszis-elemző szikra munkahelyének lemondása</span><span class="sxs-lookup"><span data-stu-id="81bd2-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="81bd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81bd2-104">SYNTAX</span></span>

### <span data-ttu-id="81bd2-105">StopSparkJobByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81bd2-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81bd2-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81bd2-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81bd2-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81bd2-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81bd2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="81bd2-108">DESCRIPTION</span></span>
<span data-ttu-id="81bd2-109">A **stop-AzSynapseSparkJob** parancsmag lemondja a szinapszis-elemző szikra munkát.</span><span class="sxs-lookup"><span data-stu-id="81bd2-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="81bd2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="81bd2-110">EXAMPLES</span></span>

### <span data-ttu-id="81bd2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81bd2-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="81bd2-112">Ez a parancs lemondja a szinapszis-elemző szikra munkát.</span><span class="sxs-lookup"><span data-stu-id="81bd2-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="81bd2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="81bd2-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="81bd2-114">Ez a parancs lemondja a szinapszis-elemző Spark-feladatot a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="81bd2-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="81bd2-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="81bd2-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="81bd2-116">Ez a parancs lemondja a szinapszis-elemző Spark-feladatot a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="81bd2-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="81bd2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81bd2-117">PARAMETERS</span></span>

### <span data-ttu-id="81bd2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bd2-118">-DefaultProfile</span></span>
<span data-ttu-id="81bd2-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81bd2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81bd2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="81bd2-120">-Force</span></span>
<span data-ttu-id="81bd2-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81bd2-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="81bd2-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="81bd2-122">-LivyId</span></span>
<span data-ttu-id="81bd2-123">A Spark-feladat azonosítója</span><span class="sxs-lookup"><span data-stu-id="81bd2-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="81bd2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81bd2-124">-PassThru</span></span>
<span data-ttu-id="81bd2-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="81bd2-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="81bd2-126">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="81bd2-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="81bd2-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="81bd2-127">-SparkJobObject</span></span>
<span data-ttu-id="81bd2-128">Szikra a projekt bemeneti objektuma, általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="81bd2-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="81bd2-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="81bd2-129">-SparkPoolName</span></span>
<span data-ttu-id="81bd2-130">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="81bd2-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="81bd2-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="81bd2-131">-SparkPoolObject</span></span>
<span data-ttu-id="81bd2-132">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="81bd2-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="81bd2-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="81bd2-133">-WorkspaceName</span></span>
<span data-ttu-id="81bd2-134">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="81bd2-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="81bd2-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81bd2-135">-Confirm</span></span>
<span data-ttu-id="81bd2-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81bd2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81bd2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81bd2-137">-WhatIf</span></span>
<span data-ttu-id="81bd2-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81bd2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81bd2-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81bd2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81bd2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bd2-140">CommonParameters</span></span>
<span data-ttu-id="81bd2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81bd2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bd2-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="81bd2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bd2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bd2-143">INPUTS</span></span>

### <span data-ttu-id="81bd2-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="81bd2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="81bd2-145">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="81bd2-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="81bd2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bd2-146">OUTPUTS</span></span>

### <span data-ttu-id="81bd2-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81bd2-147">System.Boolean</span></span>

## <span data-ttu-id="81bd2-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81bd2-148">NOTES</span></span>

## <span data-ttu-id="81bd2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81bd2-149">RELATED LINKS</span></span>
