---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183166"
---
# <span data-ttu-id="09521-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="09521-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="09521-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09521-102">SYNOPSIS</span></span>
<span data-ttu-id="09521-103">Az integrációs futtatókörnyezet metrikus adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="09521-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="09521-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09521-104">SYNTAX</span></span>

### <span data-ttu-id="09521-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09521-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09521-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09521-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09521-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09521-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09521-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09521-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09521-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="09521-109">DESCRIPTION</span></span>
<span data-ttu-id="09521-110">A **Get-AzSynapseIntegrationRuntimeMetric** parancsmag metrikus adatokat kap a munkaterületek integrációs futtatókörnyezetéről.</span><span class="sxs-lookup"><span data-stu-id="09521-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="09521-111">Példák</span><span class="sxs-lookup"><span data-stu-id="09521-111">EXAMPLES</span></span>

### <span data-ttu-id="09521-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="09521-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="09521-113">Ez a parancs metrikus adatokat jelenít meg a ContosoWorkspace nevű munkaterületen az "selfhost-IR" nevű integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="09521-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="09521-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09521-114">PARAMETERS</span></span>

### <span data-ttu-id="09521-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09521-115">-DefaultProfile</span></span>
<span data-ttu-id="09521-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09521-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09521-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09521-117">-InputObject</span></span>
<span data-ttu-id="09521-118">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="09521-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="09521-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09521-119">-Name</span></span>
<span data-ttu-id="09521-120">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="09521-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="09521-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09521-121">-ResourceGroupName</span></span>
<span data-ttu-id="09521-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="09521-122">Resource group name.</span></span>

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

### <span data-ttu-id="09521-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09521-123">-ResourceId</span></span>
<span data-ttu-id="09521-124">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="09521-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="09521-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09521-125">-WorkspaceName</span></span>
<span data-ttu-id="09521-126">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="09521-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="09521-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09521-127">-WorkspaceObject</span></span>
<span data-ttu-id="09521-128">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="09521-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="09521-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09521-129">CommonParameters</span></span>
<span data-ttu-id="09521-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09521-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09521-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="09521-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09521-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09521-132">INPUTS</span></span>

### <span data-ttu-id="09521-133">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="09521-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="09521-134">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="09521-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="09521-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09521-135">OUTPUTS</span></span>

### <span data-ttu-id="09521-136">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="09521-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="09521-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09521-137">NOTES</span></span>

## <span data-ttu-id="09521-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09521-138">RELATED LINKS</span></span>
