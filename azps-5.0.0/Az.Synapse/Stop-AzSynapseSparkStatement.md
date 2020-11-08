---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194992"
---
# <span data-ttu-id="9e379-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="9e379-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="9e379-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e379-102">SYNOPSIS</span></span>
<span data-ttu-id="9e379-103">A szinapszis-elemző szikra nyilatkozatának lemondása</span><span class="sxs-lookup"><span data-stu-id="9e379-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="9e379-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e379-104">SYNTAX</span></span>

### <span data-ttu-id="9e379-105">StopSparkStatementByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e379-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e379-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e379-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e379-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e379-107">DESCRIPTION</span></span>
<span data-ttu-id="9e379-108">A **stop-AzSynapseSparkStatement** parancsmag visszamondja a szinapszis-elemző szikra utasítását.</span><span class="sxs-lookup"><span data-stu-id="9e379-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="9e379-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9e379-109">EXAMPLES</span></span>

### <span data-ttu-id="9e379-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e379-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="9e379-111">Ez a parancs a megadott Livius-azonosítójú Spark-azonosítóval mondja le a szikra utasítását.</span><span class="sxs-lookup"><span data-stu-id="9e379-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="9e379-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9e379-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="9e379-113">Ez a parancs lemondja a szikra-kimutatást a megadott Livius-AZONOSÍTÓval a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="9e379-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="9e379-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e379-114">PARAMETERS</span></span>

### <span data-ttu-id="9e379-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e379-115">-DefaultProfile</span></span>
<span data-ttu-id="9e379-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e379-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e379-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9e379-117">-Force</span></span>
<span data-ttu-id="9e379-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e379-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9e379-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="9e379-119">-LivyId</span></span>
<span data-ttu-id="9e379-120">A szikra-utasítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="9e379-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="9e379-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e379-121">-PassThru</span></span>
<span data-ttu-id="9e379-122">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="9e379-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9e379-123">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="9e379-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9e379-124">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="9e379-124">-SessionId</span></span>
<span data-ttu-id="9e379-125">A szikra munkamenet azonosítója</span><span class="sxs-lookup"><span data-stu-id="9e379-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="9e379-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="9e379-126">-SessionObject</span></span>
<span data-ttu-id="9e379-127">A szikra-munkamenet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9e379-127">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e379-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9e379-128">-SparkPoolName</span></span>
<span data-ttu-id="9e379-129">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="9e379-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9e379-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e379-130">-WorkspaceName</span></span>
<span data-ttu-id="9e379-131">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="9e379-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e379-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e379-132">-Confirm</span></span>
<span data-ttu-id="9e379-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e379-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e379-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e379-134">-WhatIf</span></span>
<span data-ttu-id="9e379-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e379-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e379-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e379-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e379-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e379-137">CommonParameters</span></span>
<span data-ttu-id="9e379-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e379-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e379-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9e379-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e379-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e379-140">INPUTS</span></span>

### <span data-ttu-id="9e379-141">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9e379-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9e379-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e379-142">OUTPUTS</span></span>

### <span data-ttu-id="9e379-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e379-143">System.Boolean</span></span>

## <span data-ttu-id="9e379-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e379-144">NOTES</span></span>

## <span data-ttu-id="9e379-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e379-145">RELATED LINKS</span></span>
