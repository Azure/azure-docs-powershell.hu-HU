---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165634"
---
# <span data-ttu-id="ea33d-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="ea33d-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="ea33d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea33d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea33d-103">Információkat kap a munkaterületen folyó adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="ea33d-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="ea33d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea33d-104">SYNTAX</span></span>

### <span data-ttu-id="ea33d-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea33d-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea33d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="ea33d-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea33d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea33d-107">DESCRIPTION</span></span>
<span data-ttu-id="ea33d-108">A **Get-AzSynapseDataFlow** parancsmag információkat kap a munkaterületen folyó adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="ea33d-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="ea33d-109">Ha megadja egy adatfolyam nevét, ez a parancsmag információt kap az adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="ea33d-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="ea33d-110">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen lévő összes adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="ea33d-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="ea33d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea33d-111">EXAMPLES</span></span>

### <span data-ttu-id="ea33d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea33d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ea33d-113">Ez a parancs információkat kap a ContosoWorkspace nevű munkaterület összes adatfolyamának adatairól.</span><span class="sxs-lookup"><span data-stu-id="ea33d-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ea33d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ea33d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="ea33d-115">Ez a parancs információkat kap a ContosoDataFlow nevű adatfolyamról a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="ea33d-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ea33d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea33d-116">PARAMETERS</span></span>

### <span data-ttu-id="ea33d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea33d-117">-DefaultProfile</span></span>
<span data-ttu-id="ea33d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea33d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea33d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ea33d-119">-Name</span></span>
<span data-ttu-id="ea33d-120">Az adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="ea33d-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea33d-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ea33d-121">-WorkspaceName</span></span>
<span data-ttu-id="ea33d-122">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="ea33d-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ea33d-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ea33d-123">-WorkspaceObject</span></span>
<span data-ttu-id="ea33d-124">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea33d-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea33d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea33d-125">CommonParameters</span></span>
<span data-ttu-id="ea33d-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea33d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea33d-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea33d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea33d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea33d-128">INPUTS</span></span>

### <span data-ttu-id="ea33d-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea33d-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ea33d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea33d-130">OUTPUTS</span></span>

### <span data-ttu-id="ea33d-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="ea33d-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="ea33d-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea33d-132">NOTES</span></span>

## <span data-ttu-id="ea33d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea33d-133">RELATED LINKS</span></span>
