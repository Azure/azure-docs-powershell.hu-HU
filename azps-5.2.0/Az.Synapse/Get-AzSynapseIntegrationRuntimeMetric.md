---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339209"
---
# <span data-ttu-id="89056-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="89056-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="89056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89056-102">SYNOPSIS</span></span>
<span data-ttu-id="89056-103">Az integrációs futásidejű metrikus adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="89056-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="89056-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89056-104">SYNTAX</span></span>

### <span data-ttu-id="89056-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89056-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89056-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89056-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89056-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89056-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89056-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89056-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89056-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89056-109">DESCRIPTION</span></span>
<span data-ttu-id="89056-110">A **Get-AzSynapseIntegrationRuntimeMetric parancsmag** metrikus adatokat kap az integrációs futásidőről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="89056-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="89056-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89056-111">EXAMPLES</span></span>

### <span data-ttu-id="89056-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="89056-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="89056-113">Ez a parancs a ContosoWorkspace nevű munkaterületen megjeleníti a "test-selfhost-ir" nevű integrációs futásidő metrikus adatait.</span><span class="sxs-lookup"><span data-stu-id="89056-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="89056-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89056-114">PARAMETERS</span></span>

### <span data-ttu-id="89056-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89056-115">-DefaultProfile</span></span>
<span data-ttu-id="89056-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89056-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89056-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89056-117">-InputObject</span></span>
<span data-ttu-id="89056-118">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="89056-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89056-119">-Name</span><span class="sxs-lookup"><span data-stu-id="89056-119">-Name</span></span>
<span data-ttu-id="89056-120">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="89056-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89056-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89056-121">-ResourceGroupName</span></span>
<span data-ttu-id="89056-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89056-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89056-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89056-123">-ResourceId</span></span>
<span data-ttu-id="89056-124">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89056-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89056-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89056-125">-WorkspaceName</span></span>
<span data-ttu-id="89056-126">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="89056-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89056-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="89056-127">-WorkspaceObject</span></span>
<span data-ttu-id="89056-128">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="89056-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89056-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89056-129">CommonParameters</span></span>
<span data-ttu-id="89056-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89056-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89056-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89056-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89056-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89056-132">INPUTS</span></span>

### <span data-ttu-id="89056-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="89056-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="89056-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89056-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="89056-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89056-135">OUTPUTS</span></span>

### <span data-ttu-id="89056-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="89056-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="89056-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89056-137">NOTES</span></span>

## <span data-ttu-id="89056-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89056-138">RELATED LINKS</span></span>
