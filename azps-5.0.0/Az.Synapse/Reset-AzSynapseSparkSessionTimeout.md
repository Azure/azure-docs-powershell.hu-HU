---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194997"
---
# <span data-ttu-id="23f25-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="23f25-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="23f25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23f25-102">SYNOPSIS</span></span>
<span data-ttu-id="23f25-103">A szinapszis-elemző Spark-munkamenet időtúllépésének visszaállítása</span><span class="sxs-lookup"><span data-stu-id="23f25-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="23f25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23f25-104">SYNTAX</span></span>

### <span data-ttu-id="23f25-105">ResetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23f25-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f25-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23f25-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f25-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23f25-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f25-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="23f25-108">DESCRIPTION</span></span>
<span data-ttu-id="23f25-109">A **Remove-AzSynapseSparkSessionTimeout** parancsmag visszaállítja a szinapszis-elemző szikra-munkamenet időkorlátját.</span><span class="sxs-lookup"><span data-stu-id="23f25-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="23f25-110">Példák</span><span class="sxs-lookup"><span data-stu-id="23f25-110">EXAMPLES</span></span>

### <span data-ttu-id="23f25-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="23f25-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="23f25-112">Ez a parancs visszaállítja a szinapszis-elemző szikra munkamenet időkorlátját a megadott Livius-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="23f25-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="23f25-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="23f25-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="23f25-114">Ez a parancs visszaállítja a szinapszis-elemző szikra munkamenet időkorlátját a megadott Livius-AZONOSÍTÓval a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="23f25-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="23f25-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="23f25-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="23f25-116">Ez a parancs visszaállítja a szinapszis-elemző szikra munkamenet időkorlátját a megadott Livius-AZONOSÍTÓval a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="23f25-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="23f25-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23f25-117">PARAMETERS</span></span>

### <span data-ttu-id="23f25-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23f25-118">-AsJob</span></span>
<span data-ttu-id="23f25-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="23f25-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23f25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f25-120">-DefaultProfile</span></span>
<span data-ttu-id="23f25-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23f25-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23f25-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23f25-122">-InputObject</span></span>
<span data-ttu-id="23f25-123">A szikra-munkamenet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="23f25-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="23f25-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="23f25-124">-LivyId</span></span>
<span data-ttu-id="23f25-125">A szikra munkamenet azonosítója</span><span class="sxs-lookup"><span data-stu-id="23f25-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="23f25-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23f25-126">-PassThru</span></span>
<span data-ttu-id="23f25-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="23f25-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="23f25-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="23f25-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="23f25-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="23f25-129">-SparkPoolName</span></span>
<span data-ttu-id="23f25-130">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="23f25-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="23f25-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="23f25-131">-SparkPoolObject</span></span>
<span data-ttu-id="23f25-132">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="23f25-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="23f25-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23f25-133">-WorkspaceName</span></span>
<span data-ttu-id="23f25-134">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="23f25-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="23f25-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23f25-135">-Confirm</span></span>
<span data-ttu-id="23f25-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23f25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f25-137">-WhatIf</span></span>
<span data-ttu-id="23f25-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23f25-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f25-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23f25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f25-140">CommonParameters</span></span>
<span data-ttu-id="23f25-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23f25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f25-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23f25-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f25-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23f25-143">INPUTS</span></span>

### <span data-ttu-id="23f25-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="23f25-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="23f25-145">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="23f25-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="23f25-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23f25-146">OUTPUTS</span></span>

### <span data-ttu-id="23f25-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23f25-147">System.Boolean</span></span>

## <span data-ttu-id="23f25-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23f25-148">NOTES</span></span>

## <span data-ttu-id="23f25-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23f25-149">RELATED LINKS</span></span>
