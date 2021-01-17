---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466811"
---
# <span data-ttu-id="1aa2d-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aa2d-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="1aa2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa2d-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa2d-103">Információkat kap az integrációs futásidejű erőforrásokról.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="1aa2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1aa2d-104">SYNTAX</span></span>

### <span data-ttu-id="1aa2d-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1aa2d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aa2d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa2d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aa2d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa2d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1aa2d-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa2d-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aa2d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1aa2d-109">DESCRIPTION</span></span>
<span data-ttu-id="1aa2d-110">A **Get-AzSynapseIntegrationRuntime parancsmag** információkat kap a munkaterületen használt integrációs futásidőkről.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="1aa2d-111">Ha megadja egy integrációs futásidő nevét, ez a parancsmag információt kap az integrációs futásidőről.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="1aa2d-112">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen található integrációs futásidőkről.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="1aa2d-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1aa2d-113">EXAMPLES</span></span>

### <span data-ttu-id="1aa2d-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="1aa2d-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1aa2d-115">List all integration runtimes in the workspace named ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1aa2d-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="1aa2d-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="1aa2d-117">Ez a parancs a ContosoWorkspace nevű munkaterületen megjeleníti a "test-selfhost-ir" nevű integrációs futásidővel kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1aa2d-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="1aa2d-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="1aa2d-119">Ez a parancs részletesen megjeleníti a ContosoWorkspace nevű munkaterület "test-selfhost-ir" nevű integrációs futási futási állapotát.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1aa2d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aa2d-120">PARAMETERS</span></span>

### <span data-ttu-id="1aa2d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa2d-121">-DefaultProfile</span></span>
<span data-ttu-id="1aa2d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa2d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa2d-123">-InputObject</span></span>
<span data-ttu-id="1aa2d-124">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="1aa2d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1aa2d-125">-Name</span></span>
<span data-ttu-id="1aa2d-126">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="1aa2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1aa2d-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-128">Resource group name.</span></span>

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

### <span data-ttu-id="1aa2d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa2d-129">-ResourceId</span></span>
<span data-ttu-id="1aa2d-130">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="1aa2d-131">-Állapot</span><span class="sxs-lookup"><span data-stu-id="1aa2d-131">-Status</span></span>
<span data-ttu-id="1aa2d-132">Az integráció futásidejű részleteinek állapota.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="1aa2d-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1aa2d-133">-WorkspaceName</span></span>
<span data-ttu-id="1aa2d-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1aa2d-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1aa2d-135">-WorkspaceObject</span></span>
<span data-ttu-id="1aa2d-136">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1aa2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa2d-137">CommonParameters</span></span>
<span data-ttu-id="1aa2d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa2d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aa2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa2d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1aa2d-140">INPUTS</span></span>

### <span data-ttu-id="1aa2d-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1aa2d-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1aa2d-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aa2d-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1aa2d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aa2d-143">OUTPUTS</span></span>

### <span data-ttu-id="1aa2d-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aa2d-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1aa2d-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1aa2d-145">NOTES</span></span>

## <span data-ttu-id="1aa2d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1aa2d-146">RELATED LINKS</span></span>
