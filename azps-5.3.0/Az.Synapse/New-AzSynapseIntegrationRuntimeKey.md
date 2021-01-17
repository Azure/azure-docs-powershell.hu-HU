---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383625"
---
# <span data-ttu-id="c5b48-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="c5b48-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="c5b48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b48-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b48-103">Az önkiszolgáló integráció futásidejű kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c5b48-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="c5b48-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5b48-104">SYNTAX</span></span>

### <span data-ttu-id="c5b48-105">NewByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5b48-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5b48-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b48-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b48-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b48-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b48-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b48-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b48-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5b48-109">DESCRIPTION</span></span>
<span data-ttu-id="c5b48-110">A **New-AzSynapseIntegrationRuntimeKey** parancsmag a "KeyName" paraméterben megadott kulcsnévvel újragenerálja az integrációs futásidejű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="c5b48-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="c5b48-111">Az előző kulcs érvénytelen.</span><span class="sxs-lookup"><span data-stu-id="c5b48-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="c5b48-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5b48-112">EXAMPLES</span></span>

### <span data-ttu-id="c5b48-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5b48-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="c5b48-114">A parancsmag a "test-selfhost-ir" nevű integrációs runtime-hoz újragenerálja az "authKey2" kulcsot.</span><span class="sxs-lookup"><span data-stu-id="c5b48-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c5b48-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5b48-115">PARAMETERS</span></span>

### <span data-ttu-id="c5b48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b48-116">-DefaultProfile</span></span>
<span data-ttu-id="c5b48-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5b48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5b48-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c5b48-118">-Force</span></span>
<span data-ttu-id="c5b48-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5b48-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c5b48-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5b48-120">-InputObject</span></span>
<span data-ttu-id="c5b48-121">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="c5b48-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b48-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c5b48-122">-KeyName</span></span>
<span data-ttu-id="c5b48-123">Az önkiszolgáló integrációs futásidejű hitelesítési kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="c5b48-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b48-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c5b48-124">-Name</span></span>
<span data-ttu-id="c5b48-125">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="c5b48-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b48-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b48-126">-ResourceGroupName</span></span>
<span data-ttu-id="c5b48-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5b48-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b48-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5b48-128">-ResourceId</span></span>
<span data-ttu-id="c5b48-129">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c5b48-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b48-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5b48-130">-WorkspaceName</span></span>
<span data-ttu-id="c5b48-131">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="c5b48-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b48-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c5b48-132">-WorkspaceObject</span></span>
<span data-ttu-id="c5b48-133">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5b48-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b48-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5b48-134">-Confirm</span></span>
<span data-ttu-id="c5b48-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5b48-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b48-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b48-136">-WhatIf</span></span>
<span data-ttu-id="c5b48-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5b48-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b48-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5b48-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b48-139">CommonParameters</span></span>
<span data-ttu-id="c5b48-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b48-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5b48-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b48-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5b48-142">INPUTS</span></span>

### <span data-ttu-id="c5b48-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5b48-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c5b48-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c5b48-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c5b48-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5b48-145">OUTPUTS</span></span>

### <span data-ttu-id="c5b48-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="c5b48-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="c5b48-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5b48-147">NOTES</span></span>

## <span data-ttu-id="c5b48-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5b48-148">RELATED LINKS</span></span>
