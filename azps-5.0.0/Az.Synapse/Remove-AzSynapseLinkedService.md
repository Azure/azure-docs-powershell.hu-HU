---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187913"
---
# <span data-ttu-id="d3589-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="d3589-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="d3589-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3589-102">SYNOPSIS</span></span>
<span data-ttu-id="d3589-103">Egy kapcsolt szolgáltatás eltávolítása a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d3589-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="d3589-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3589-104">SYNTAX</span></span>

### <span data-ttu-id="d3589-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3589-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3589-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="d3589-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3589-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3589-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3589-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3589-108">DESCRIPTION</span></span>
<span data-ttu-id="d3589-109">A **Remove-AzSynapseLinkedService** parancsmag eltávolított egy kapcsolt szolgáltatást a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d3589-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="d3589-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d3589-110">EXAMPLES</span></span>

### <span data-ttu-id="d3589-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3589-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="d3589-112">Ez a parancs eltávolítja a ContosoLinkedService nevű kapcsolt szolgáltatást a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d3589-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d3589-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d3589-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="d3589-114">Ez a parancs eltávolítja a ContosoLinkedService nevű kapcsolt szolgáltatást a ContosoWorkspace – csővezeték nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d3589-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="d3589-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d3589-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="d3589-116">Ez a parancs eltávolítja a ContosoLinkedService nevű kapcsolt szolgáltatást a ContosoWorkspace – csővezeték nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d3589-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d3589-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3589-117">PARAMETERS</span></span>

### <span data-ttu-id="d3589-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3589-118">-AsJob</span></span>
<span data-ttu-id="d3589-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d3589-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3589-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3589-120">-DefaultProfile</span></span>
<span data-ttu-id="d3589-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3589-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3589-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3589-122">-InputObject</span></span>
<span data-ttu-id="d3589-123">A kapcsolt szolgáltatás objektum.</span><span class="sxs-lookup"><span data-stu-id="d3589-123">The linked service object.</span></span>

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

### <span data-ttu-id="d3589-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3589-124">-Name</span></span>
<span data-ttu-id="d3589-125">A kapcsolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d3589-125">The linked service name.</span></span>

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

### <span data-ttu-id="d3589-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3589-126">-PassThru</span></span>
<span data-ttu-id="d3589-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="d3589-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d3589-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="d3589-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d3589-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3589-129">-WorkspaceName</span></span>
<span data-ttu-id="d3589-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="d3589-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d3589-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d3589-131">-WorkspaceObject</span></span>
<span data-ttu-id="d3589-132">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="d3589-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d3589-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3589-133">-Confirm</span></span>
<span data-ttu-id="d3589-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3589-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3589-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3589-135">-WhatIf</span></span>
<span data-ttu-id="d3589-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3589-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3589-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3589-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3589-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3589-138">CommonParameters</span></span>
<span data-ttu-id="d3589-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3589-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3589-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3589-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3589-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3589-141">INPUTS</span></span>

### <span data-ttu-id="d3589-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3589-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d3589-143">Microsoft. Azure. commands. szinapszis. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="d3589-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="d3589-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3589-144">OUTPUTS</span></span>

### <span data-ttu-id="d3589-145">Microsoft. Azure. commands. szinapszis. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="d3589-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="d3589-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3589-146">NOTES</span></span>

## <span data-ttu-id="d3589-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3589-147">RELATED LINKS</span></span>
