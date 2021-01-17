---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466807"
---
# <span data-ttu-id="0e615-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="0e615-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="0e615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e615-102">SYNOPSIS</span></span>
<span data-ttu-id="0e615-103">Információkat kap a munkaterületen található csatolt szolgáltatásokról.</span><span class="sxs-lookup"><span data-stu-id="0e615-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="0e615-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e615-104">SYNTAX</span></span>

### <span data-ttu-id="0e615-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e615-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e615-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="0e615-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e615-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e615-107">DESCRIPTION</span></span>
<span data-ttu-id="0e615-108">A **Get-AzSynapseLinkedService** parancsmag információkat kap a munkaterületen található csatolt szolgáltatásokról.</span><span class="sxs-lookup"><span data-stu-id="0e615-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="0e615-109">Ha megadja egy csatolt szolgáltatás nevét, ez a parancsmag információt kap a hivatkozott szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="0e615-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="0e615-110">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen található összes csatolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="0e615-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="0e615-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e615-111">EXAMPLES</span></span>

### <span data-ttu-id="0e615-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0e615-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0e615-113">Ez a parancs információkat kap a ContosoWorkspace nevű munkaterület összes csatolt szolgáltatásának adatairól.</span><span class="sxs-lookup"><span data-stu-id="0e615-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0e615-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0e615-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="0e615-115">Ez a parancs információkat kap a ContosoLinkedService nevű csatolt szolgáltatásról a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="0e615-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0e615-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="0e615-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="0e615-117">Ez a parancs információkat kap a ContosoLinkedService nevű csatolt szolgáltatásról a ContosoWorkspace nevű munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="0e615-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0e615-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e615-118">PARAMETERS</span></span>

### <span data-ttu-id="0e615-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e615-119">-DefaultProfile</span></span>
<span data-ttu-id="0e615-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e615-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e615-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0e615-121">-Name</span></span>
<span data-ttu-id="0e615-122">A hivatkozott szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0e615-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e615-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0e615-123">-WorkspaceName</span></span>
<span data-ttu-id="0e615-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="0e615-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e615-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0e615-125">-WorkspaceObject</span></span>
<span data-ttu-id="0e615-126">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e615-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e615-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e615-127">CommonParameters</span></span>
<span data-ttu-id="0e615-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e615-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e615-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e615-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e615-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e615-130">INPUTS</span></span>

### <span data-ttu-id="0e615-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e615-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0e615-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e615-132">OUTPUTS</span></span>

### <span data-ttu-id="0e615-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="0e615-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="0e615-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e615-134">NOTES</span></span>

## <span data-ttu-id="0e615-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e615-135">RELATED LINKS</span></span>
