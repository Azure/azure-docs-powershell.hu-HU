---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156018"
---
# <span data-ttu-id="d8e7d-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="d8e7d-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="d8e7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e7d-103">Egy adattár vagy egy felhőszolgáltatás munkaterületre csatolása.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="d8e7d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8e7d-104">SYNTAX</span></span>

### <span data-ttu-id="d8e7d-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8e7d-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e7d-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="d8e7d-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e7d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8e7d-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e7d-108">A **Set-AzSynapseLinkedService** parancsmag egy adattárat vagy egy felhőszolgáltatást a munkaterületre csatol.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="d8e7d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8e7d-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e7d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d8e7d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="d8e7d-111">Ez a parancs létrehoz egy ContosoLinkedService nevű csatolt szolgáltatást a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d8e7d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d8e7d-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="d8e7d-113">Ez a parancs létrehoz egy ContosoLinkedService nevű csatolt szolgáltatást a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d8e7d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8e7d-114">PARAMETERS</span></span>

### <span data-ttu-id="d8e7d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8e7d-115">-AsJob</span></span>
<span data-ttu-id="d8e7d-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d8e7d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8e7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e7d-117">-DefaultProfile</span></span>
<span data-ttu-id="d8e7d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8e7d-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d8e7d-119">-DefinitionFile</span></span>
<span data-ttu-id="d8e7d-120">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d8e7d-121">-Name</span></span>
<span data-ttu-id="d8e7d-122">A hivatkozott szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e7d-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8e7d-123">-WorkspaceName</span></span>
<span data-ttu-id="d8e7d-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e7d-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8e7d-125">-WorkspaceObject</span></span>
<span data-ttu-id="d8e7d-126">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e7d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8e7d-127">-Confirm</span></span>
<span data-ttu-id="d8e7d-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e7d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e7d-129">-WhatIf</span></span>
<span data-ttu-id="d8e7d-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e7d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e7d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e7d-132">CommonParameters</span></span>
<span data-ttu-id="d8e7d-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e7d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e7d-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8e7d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e7d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8e7d-135">INPUTS</span></span>

### <span data-ttu-id="d8e7d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8e7d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d8e7d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8e7d-137">OUTPUTS</span></span>

### <span data-ttu-id="d8e7d-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="d8e7d-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="d8e7d-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8e7d-139">NOTES</span></span>

## <span data-ttu-id="d8e7d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8e7d-140">RELATED LINKS</span></span>
