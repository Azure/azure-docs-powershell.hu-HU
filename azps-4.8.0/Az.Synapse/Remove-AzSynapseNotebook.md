---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025620"
---
# <span data-ttu-id="4ac8e-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="4ac8e-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="4ac8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ac8e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac8e-103">Jegyzetfüzet eltávolítása munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="4ac8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ac8e-104">SYNTAX</span></span>

### <span data-ttu-id="4ac8e-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ac8e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ac8e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4ac8e-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ac8e-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ac8e-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac8e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ac8e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ac8e-109">A **Remove-AzSynapseNotebook** parancsmag eltávolítja a jegyzetfüzetet egy munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="4ac8e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4ac8e-110">EXAMPLES</span></span>

### <span data-ttu-id="4ac8e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ac8e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="4ac8e-112">Távolítsa el a ContosoNotebook nevű jegyzetfüzetet a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="4ac8e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4ac8e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="4ac8e-114">Távolítson el egy ContosoNotebook nevű jegyzetfüzetet a munkaterület ContosoWorkspace a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4ac8e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="4ac8e-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="4ac8e-116">Távolítson el egy ContosoNotebook nevű jegyzetfüzetet a munkaterület ContosoWorkspace a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4ac8e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ac8e-117">PARAMETERS</span></span>

### <span data-ttu-id="4ac8e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ac8e-118">-AsJob</span></span>
<span data-ttu-id="4ac8e-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4ac8e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ac8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac8e-120">-DefaultProfile</span></span>
<span data-ttu-id="4ac8e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac8e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ac8e-122">-InputObject</span></span>
<span data-ttu-id="4ac8e-123">A jegyzetfüzet objektuma.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-123">The notebook object.</span></span>

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

### <span data-ttu-id="4ac8e-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ac8e-124">-Name</span></span>
<span data-ttu-id="4ac8e-125">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-125">The notebook name.</span></span>

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

### <span data-ttu-id="4ac8e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ac8e-126">-PassThru</span></span>
<span data-ttu-id="4ac8e-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4ac8e-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4ac8e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ac8e-129">-WorkspaceName</span></span>
<span data-ttu-id="4ac8e-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4ac8e-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4ac8e-131">-WorkspaceObject</span></span>
<span data-ttu-id="4ac8e-132">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4ac8e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ac8e-133">-Confirm</span></span>
<span data-ttu-id="4ac8e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac8e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac8e-135">-WhatIf</span></span>
<span data-ttu-id="4ac8e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ac8e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac8e-138">CommonParameters</span></span>
<span data-ttu-id="4ac8e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ac8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac8e-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ac8e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac8e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ac8e-141">INPUTS</span></span>

### <span data-ttu-id="4ac8e-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4ac8e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4ac8e-143">Microsoft. Azure. commands. szinapszis. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="4ac8e-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="4ac8e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ac8e-144">OUTPUTS</span></span>

### <span data-ttu-id="4ac8e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ac8e-145">System.Boolean</span></span>

## <span data-ttu-id="4ac8e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ac8e-146">NOTES</span></span>

## <span data-ttu-id="4ac8e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ac8e-147">RELATED LINKS</span></span>
