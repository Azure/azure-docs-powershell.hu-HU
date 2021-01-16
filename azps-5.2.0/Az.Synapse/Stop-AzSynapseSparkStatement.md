---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347322"
---
# <span data-ttu-id="a9953-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="a9953-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="a9953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9953-102">SYNOPSIS</span></span>
<span data-ttu-id="a9953-103">Visszavonja a Synapse Analytics Spark utasítást.</span><span class="sxs-lookup"><span data-stu-id="a9953-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="a9953-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9953-104">SYNTAX</span></span>

### <span data-ttu-id="a9953-105">StopSparkStatementByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9953-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9953-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9953-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9953-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9953-107">DESCRIPTION</span></span>
<span data-ttu-id="a9953-108">A **Stop-AzSynapseSparkStatement** parancsmag megszakítja a Synapse Analytics Spark utasítást.</span><span class="sxs-lookup"><span data-stu-id="a9953-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="a9953-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9953-109">EXAMPLES</span></span>

### <span data-ttu-id="a9953-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a9953-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="a9953-111">Ez a parancs megszakítja a Spark utasítást a megadott y azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="a9953-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="a9953-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a9953-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="a9953-113">Ez a parancs megszakítja a Spark utasítást a megadott y azonosítóval a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="a9953-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="a9953-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9953-114">PARAMETERS</span></span>

### <span data-ttu-id="a9953-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9953-115">-DefaultProfile</span></span>
<span data-ttu-id="a9953-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9953-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9953-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a9953-117">-Force</span></span>
<span data-ttu-id="a9953-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9953-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a9953-119">-SiyId</span><span class="sxs-lookup"><span data-stu-id="a9953-119">-LivyId</span></span>
<span data-ttu-id="a9953-120">Az Értékgörbe utasítás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9953-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9953-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9953-121">-PassThru</span></span>
<span data-ttu-id="a9953-122">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="a9953-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a9953-123">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="a9953-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a9953-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="a9953-124">-SessionId</span></span>
<span data-ttu-id="a9953-125">A Spark-munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9953-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9953-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="a9953-126">-SessionObject</span></span>
<span data-ttu-id="a9953-127">Spark session input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9953-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9953-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="a9953-128">-SparkPoolName</span></span>
<span data-ttu-id="a9953-129">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="a9953-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9953-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9953-130">-WorkspaceName</span></span>
<span data-ttu-id="a9953-131">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="a9953-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9953-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9953-132">-Confirm</span></span>
<span data-ttu-id="a9953-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a9953-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9953-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9953-134">-WhatIf</span></span>
<span data-ttu-id="a9953-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a9953-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9953-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9953-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9953-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9953-137">CommonParameters</span></span>
<span data-ttu-id="a9953-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9953-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9953-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9953-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9953-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9953-140">INPUTS</span></span>

### <span data-ttu-id="a9953-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="a9953-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="a9953-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9953-142">OUTPUTS</span></span>

### <span data-ttu-id="a9953-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9953-143">System.Boolean</span></span>

## <span data-ttu-id="a9953-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9953-144">NOTES</span></span>

## <span data-ttu-id="a9953-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9953-145">RELATED LINKS</span></span>
