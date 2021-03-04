---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 168a19c6e3900b395841aabbc19359d9fa4858f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933521"
---
# <span data-ttu-id="fea1a-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fea1a-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="fea1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea1a-102">SYNOPSIS</span></span>
<span data-ttu-id="fea1a-103">Információkat kap az integrációs futásidejű erőforrásokról.</span><span class="sxs-lookup"><span data-stu-id="fea1a-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="fea1a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fea1a-104">SYNTAX</span></span>

### <span data-ttu-id="fea1a-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fea1a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea1a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea1a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea1a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea1a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fea1a-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea1a-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fea1a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fea1a-109">DESCRIPTION</span></span>
<span data-ttu-id="fea1a-110">A **Get-AzSynapseIntegrationRuntime parancsmag** információkat kap a munkaterületen használt integrációs futásidőkről.</span><span class="sxs-lookup"><span data-stu-id="fea1a-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="fea1a-111">Ha megadja egy integrációs futásidő nevét, ez a parancsmag információt kap az integrációs futásidőről.</span><span class="sxs-lookup"><span data-stu-id="fea1a-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="fea1a-112">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen található integrációs futásidőkről.</span><span class="sxs-lookup"><span data-stu-id="fea1a-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="fea1a-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fea1a-113">EXAMPLES</span></span>

### <span data-ttu-id="fea1a-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="fea1a-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fea1a-115">List all integration runtimes in the workspace named ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fea1a-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fea1a-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="fea1a-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="fea1a-117">Ez a parancs a ContosoWorkspace nevű munkaterületen megjeleníti a "test-selfhost-ir" nevű integrációs futásidővel kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="fea1a-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fea1a-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="fea1a-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="fea1a-119">Ez a parancs részletesen megjeleníti a ContosoWorkspace nevű munkaterület "test-selfhost-ir" nevű integrációs futási futási állapotát.</span><span class="sxs-lookup"><span data-stu-id="fea1a-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fea1a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fea1a-120">PARAMETERS</span></span>

### <span data-ttu-id="fea1a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea1a-121">-DefaultProfile</span></span>
<span data-ttu-id="fea1a-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fea1a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea1a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea1a-123">-InputObject</span></span>
<span data-ttu-id="fea1a-124">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="fea1a-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="fea1a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fea1a-125">-Name</span></span>
<span data-ttu-id="fea1a-126">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="fea1a-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="fea1a-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fea1a-128">Resource group name.</span></span>

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

### <span data-ttu-id="fea1a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea1a-129">-ResourceId</span></span>
<span data-ttu-id="fea1a-130">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fea1a-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="fea1a-131">-Állapot</span><span class="sxs-lookup"><span data-stu-id="fea1a-131">-Status</span></span>
<span data-ttu-id="fea1a-132">Az integráció futásidejű részleteinek állapota.</span><span class="sxs-lookup"><span data-stu-id="fea1a-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="fea1a-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fea1a-133">-WorkspaceName</span></span>
<span data-ttu-id="fea1a-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="fea1a-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fea1a-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fea1a-135">-WorkspaceObject</span></span>
<span data-ttu-id="fea1a-136">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="fea1a-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fea1a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea1a-137">CommonParameters</span></span>
<span data-ttu-id="fea1a-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea1a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea1a-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fea1a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea1a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fea1a-140">INPUTS</span></span>

### <span data-ttu-id="fea1a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fea1a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fea1a-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fea1a-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fea1a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea1a-143">OUTPUTS</span></span>

### <span data-ttu-id="fea1a-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fea1a-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fea1a-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fea1a-145">NOTES</span></span>

## <span data-ttu-id="fea1a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fea1a-146">RELATED LINKS</span></span>
