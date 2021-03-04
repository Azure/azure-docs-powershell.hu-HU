---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: 640992f0070d6cff14852000b07ecd8eddc61c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936586"
---
# <span data-ttu-id="951da-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="951da-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="951da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="951da-102">SYNOPSIS</span></span>
<span data-ttu-id="951da-103">Eltávolít egy csatolt szolgáltatást a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="951da-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="951da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="951da-104">SYNTAX</span></span>

### <span data-ttu-id="951da-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="951da-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951da-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="951da-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951da-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="951da-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="951da-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="951da-108">DESCRIPTION</span></span>
<span data-ttu-id="951da-109">A **Remove-AzSynapseLinkedService** parancsmag eltávolít egy csatolt szolgáltatást a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="951da-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="951da-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="951da-110">EXAMPLES</span></span>

### <span data-ttu-id="951da-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="951da-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="951da-112">Ez a parancs eltávolítja a ContosoLinkedService nevű csatolt szolgáltatást a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="951da-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="951da-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="951da-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="951da-114">Ez a parancs eltávolítja a ContosoLinkedService nevű csatolt szolgáltatást a ContosoWorkspace nevű munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="951da-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="951da-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="951da-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="951da-116">Ez a parancs eltávolítja a ContosoLinkedService nevű csatolt szolgáltatást a ContosoWorkspace nevű munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="951da-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="951da-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="951da-117">PARAMETERS</span></span>

### <span data-ttu-id="951da-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="951da-118">-AsJob</span></span>
<span data-ttu-id="951da-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="951da-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="951da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951da-120">-DefaultProfile</span></span>
<span data-ttu-id="951da-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="951da-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="951da-122">-Force</span><span class="sxs-lookup"><span data-stu-id="951da-122">-Force</span></span>
<span data-ttu-id="951da-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="951da-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="951da-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="951da-124">-InputObject</span></span>
<span data-ttu-id="951da-125">A csatolt szolgáltatásobjektum.</span><span class="sxs-lookup"><span data-stu-id="951da-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="951da-126">-Name</span><span class="sxs-lookup"><span data-stu-id="951da-126">-Name</span></span>
<span data-ttu-id="951da-127">A hivatkozott szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="951da-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951da-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="951da-128">-PassThru</span></span>
<span data-ttu-id="951da-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="951da-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="951da-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="951da-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="951da-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="951da-131">-WorkspaceName</span></span>
<span data-ttu-id="951da-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="951da-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951da-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="951da-133">-WorkspaceObject</span></span>
<span data-ttu-id="951da-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="951da-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="951da-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="951da-135">-Confirm</span></span>
<span data-ttu-id="951da-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="951da-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="951da-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="951da-137">-WhatIf</span></span>
<span data-ttu-id="951da-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="951da-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="951da-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="951da-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="951da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951da-140">CommonParameters</span></span>
<span data-ttu-id="951da-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="951da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951da-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="951da-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951da-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="951da-143">INPUTS</span></span>

### <span data-ttu-id="951da-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="951da-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="951da-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="951da-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="951da-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="951da-146">OUTPUTS</span></span>

### <span data-ttu-id="951da-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="951da-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="951da-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="951da-148">NOTES</span></span>

## <span data-ttu-id="951da-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="951da-149">RELATED LINKS</span></span>
