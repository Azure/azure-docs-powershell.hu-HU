---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185742"
---
# <span data-ttu-id="8477b-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8477b-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="8477b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8477b-102">SYNOPSIS</span></span>
<span data-ttu-id="8477b-103">A szinapszis-elemző szikra munkamenet leállítása.</span><span class="sxs-lookup"><span data-stu-id="8477b-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="8477b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8477b-104">SYNTAX</span></span>

### <span data-ttu-id="8477b-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8477b-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8477b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8477b-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8477b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8477b-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8477b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8477b-108">DESCRIPTION</span></span>
<span data-ttu-id="8477b-109">A **stop-AzSynapseSparkSession** parancsmag leállítja a szinapszis-elemző szikra-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="8477b-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="8477b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8477b-110">EXAMPLES</span></span>

### <span data-ttu-id="8477b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8477b-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="8477b-112">Ez a parancs leállítja a szinapszis-elemző szikra-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="8477b-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="8477b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8477b-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="8477b-114">Ez a parancs a szinapszis-statisztika kivezetését a csővezetéken keresztül szünteti meg.</span><span class="sxs-lookup"><span data-stu-id="8477b-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="8477b-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="8477b-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="8477b-116">Ez a parancs a szinapszis-statisztika kivezetését a csővezetéken keresztül szünteti meg.</span><span class="sxs-lookup"><span data-stu-id="8477b-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="8477b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8477b-117">PARAMETERS</span></span>

### <span data-ttu-id="8477b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8477b-118">-AsJob</span></span>
<span data-ttu-id="8477b-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8477b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8477b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8477b-120">-DefaultProfile</span></span>
<span data-ttu-id="8477b-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8477b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8477b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8477b-122">-InputObject</span></span>
<span data-ttu-id="8477b-123">A szikra-munkamenet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="8477b-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8477b-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="8477b-124">-LivyId</span></span>
<span data-ttu-id="8477b-125">A szikra munkamenet azonosítója</span><span class="sxs-lookup"><span data-stu-id="8477b-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="8477b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8477b-126">-PassThru</span></span>
<span data-ttu-id="8477b-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="8477b-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8477b-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="8477b-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8477b-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8477b-129">-SparkPoolName</span></span>
<span data-ttu-id="8477b-130">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="8477b-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8477b-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="8477b-131">-SparkPoolObject</span></span>
<span data-ttu-id="8477b-132">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="8477b-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8477b-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8477b-133">-WorkspaceName</span></span>
<span data-ttu-id="8477b-134">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="8477b-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8477b-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8477b-135">-Confirm</span></span>
<span data-ttu-id="8477b-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8477b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8477b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8477b-137">-WhatIf</span></span>
<span data-ttu-id="8477b-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8477b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8477b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8477b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8477b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8477b-140">CommonParameters</span></span>
<span data-ttu-id="8477b-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8477b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8477b-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8477b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8477b-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8477b-143">INPUTS</span></span>

### <span data-ttu-id="8477b-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8477b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="8477b-145">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8477b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="8477b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8477b-146">OUTPUTS</span></span>

### <span data-ttu-id="8477b-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8477b-147">System.Boolean</span></span>

## <span data-ttu-id="8477b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8477b-148">NOTES</span></span>

## <span data-ttu-id="8477b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8477b-149">RELATED LINKS</span></span>
