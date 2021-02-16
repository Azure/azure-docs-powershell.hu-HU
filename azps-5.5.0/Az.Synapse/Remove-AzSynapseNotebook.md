---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162810"
---
# <span data-ttu-id="cba86-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="cba86-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="cba86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba86-102">SYNOPSIS</span></span>
<span data-ttu-id="cba86-103">Eltávolít egy jegyzetfüzetet egy munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="cba86-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="cba86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cba86-104">SYNTAX</span></span>

### <span data-ttu-id="cba86-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cba86-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba86-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="cba86-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba86-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="cba86-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cba86-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cba86-108">DESCRIPTION</span></span>
<span data-ttu-id="cba86-109">A **Remove-AzSynapseNotebook** parancsmag eltávolítja a jegyzetfüzetet a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="cba86-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="cba86-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cba86-110">EXAMPLES</span></span>

### <span data-ttu-id="cba86-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cba86-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="cba86-112">Távolítsa el a ContosoNotebook nevű jegyzetfüzetet a ContosoWorkspace munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="cba86-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cba86-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cba86-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="cba86-114">Távolítsa el a ContosoNotebook nevű jegyzetfüzetet a ContosoWorkspace-munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="cba86-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="cba86-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="cba86-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="cba86-116">Távolítsa el a ContosoNotebook nevű jegyzetfüzetet a ContosoWorkspace-munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="cba86-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cba86-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cba86-117">PARAMETERS</span></span>

### <span data-ttu-id="cba86-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cba86-118">-AsJob</span></span>
<span data-ttu-id="cba86-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cba86-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cba86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba86-120">-DefaultProfile</span></span>
<span data-ttu-id="cba86-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cba86-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cba86-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cba86-122">-Force</span></span>
<span data-ttu-id="cba86-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cba86-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cba86-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cba86-124">-InputObject</span></span>
<span data-ttu-id="cba86-125">A jegyzetfüzet-objektum.</span><span class="sxs-lookup"><span data-stu-id="cba86-125">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cba86-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cba86-126">-Name</span></span>
<span data-ttu-id="cba86-127">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="cba86-127">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba86-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cba86-128">-PassThru</span></span>
<span data-ttu-id="cba86-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="cba86-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cba86-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="cba86-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cba86-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cba86-131">-WorkspaceName</span></span>
<span data-ttu-id="cba86-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="cba86-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cba86-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cba86-133">-WorkspaceObject</span></span>
<span data-ttu-id="cba86-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="cba86-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cba86-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cba86-135">-Confirm</span></span>
<span data-ttu-id="cba86-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cba86-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cba86-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cba86-137">-WhatIf</span></span>
<span data-ttu-id="cba86-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cba86-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cba86-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cba86-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cba86-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba86-140">CommonParameters</span></span>
<span data-ttu-id="cba86-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba86-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba86-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cba86-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba86-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cba86-143">INPUTS</span></span>

### <span data-ttu-id="cba86-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cba86-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cba86-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="cba86-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="cba86-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cba86-146">OUTPUTS</span></span>

### <span data-ttu-id="cba86-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cba86-147">System.Boolean</span></span>

## <span data-ttu-id="cba86-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cba86-148">NOTES</span></span>

## <span data-ttu-id="cba86-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cba86-149">RELATED LINKS</span></span>
