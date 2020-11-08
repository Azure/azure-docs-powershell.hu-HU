---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187964"
---
# <span data-ttu-id="d963c-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d963c-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="d963c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d963c-102">SYNOPSIS</span></span>
<span data-ttu-id="d963c-103">Információt kap az integrációs futtatókörnyezet erőforrásairól.</span><span class="sxs-lookup"><span data-stu-id="d963c-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="d963c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d963c-104">SYNTAX</span></span>

### <span data-ttu-id="d963c-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d963c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d963c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d963c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d963c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d963c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d963c-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d963c-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d963c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d963c-109">DESCRIPTION</span></span>
<span data-ttu-id="d963c-110">A **Get-AzSynapseIntegrationRuntime** parancsmag információkat kap a munkaterületek integrációs futtatókörnyezetéről.</span><span class="sxs-lookup"><span data-stu-id="d963c-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="d963c-111">Ha az integrációs futtatókörnyezet nevét adja meg, ez a parancsmag információkat kap az integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="d963c-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="d963c-112">Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterület összes integrációs futtatókörnyezetéről.</span><span class="sxs-lookup"><span data-stu-id="d963c-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="d963c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d963c-113">EXAMPLES</span></span>

### <span data-ttu-id="d963c-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d963c-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d963c-115">A ContosoWorkspace nevű munkaterületen minden integrációs futtatókörnyezet felsorolása.</span><span class="sxs-lookup"><span data-stu-id="d963c-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d963c-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="d963c-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="d963c-117">Ez a parancs a ContosoWorkspace nevű munkaterületen jeleníti meg az "ellenőrzés – selfhost – IR" nevű integrációs futtatókörnyezetről szóló információkat.</span><span class="sxs-lookup"><span data-stu-id="d963c-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d963c-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="d963c-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="d963c-119">Ez a parancs a ContosoWorkspace nevű munkaterületen jeleníti meg a "teszt-selfhost-IR" nevű integrációs futtatókörnyezet részleteit.</span><span class="sxs-lookup"><span data-stu-id="d963c-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d963c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d963c-120">PARAMETERS</span></span>

### <span data-ttu-id="d963c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d963c-121">-DefaultProfile</span></span>
<span data-ttu-id="d963c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d963c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d963c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d963c-123">-InputObject</span></span>
<span data-ttu-id="d963c-124">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="d963c-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="d963c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d963c-125">-Name</span></span>
<span data-ttu-id="d963c-126">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="d963c-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="d963c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d963c-127">-ResourceGroupName</span></span>
<span data-ttu-id="d963c-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d963c-128">Resource group name.</span></span>

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

### <span data-ttu-id="d963c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d963c-129">-ResourceId</span></span>
<span data-ttu-id="d963c-130">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d963c-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="d963c-131">-Állapot</span><span class="sxs-lookup"><span data-stu-id="d963c-131">-Status</span></span>
<span data-ttu-id="d963c-132">Az integrációs futtatókörnyezet részletének állapota.</span><span class="sxs-lookup"><span data-stu-id="d963c-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="d963c-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d963c-133">-WorkspaceName</span></span>
<span data-ttu-id="d963c-134">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="d963c-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d963c-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d963c-135">-WorkspaceObject</span></span>
<span data-ttu-id="d963c-136">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="d963c-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d963c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d963c-137">CommonParameters</span></span>
<span data-ttu-id="d963c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d963c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d963c-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d963c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d963c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d963c-140">INPUTS</span></span>

### <span data-ttu-id="d963c-141">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d963c-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d963c-142">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d963c-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d963c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d963c-143">OUTPUTS</span></span>

### <span data-ttu-id="d963c-144">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d963c-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d963c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d963c-145">NOTES</span></span>

## <span data-ttu-id="d963c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d963c-146">RELATED LINKS</span></span>
