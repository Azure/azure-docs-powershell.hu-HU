---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339270"
---
# <span data-ttu-id="496ed-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="496ed-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="496ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496ed-102">SYNOPSIS</span></span>
<span data-ttu-id="496ed-103">Információkat kap a munkaterületen folyó adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="496ed-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="496ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="496ed-104">SYNTAX</span></span>

### <span data-ttu-id="496ed-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="496ed-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="496ed-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="496ed-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="496ed-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="496ed-107">DESCRIPTION</span></span>
<span data-ttu-id="496ed-108">A **Get-AzSynapseDataFlow** parancsmag információkat kap a munkaterületen folyó adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="496ed-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="496ed-109">Ha megadja egy adatfolyam nevét, ez a parancsmag információt kap az adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="496ed-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="496ed-110">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen lévő összes adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="496ed-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="496ed-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="496ed-111">EXAMPLES</span></span>

### <span data-ttu-id="496ed-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="496ed-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="496ed-113">Ez a parancs információkat kap a ContosoWorkspace nevű munkaterület összes adatfolyamának adatairól.</span><span class="sxs-lookup"><span data-stu-id="496ed-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="496ed-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="496ed-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="496ed-115">Ez a parancs információkat kap a ContosoDataFlow nevű adatfolyamról a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="496ed-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="496ed-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="496ed-116">PARAMETERS</span></span>

### <span data-ttu-id="496ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496ed-117">-DefaultProfile</span></span>
<span data-ttu-id="496ed-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="496ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="496ed-119">-Name</span><span class="sxs-lookup"><span data-stu-id="496ed-119">-Name</span></span>
<span data-ttu-id="496ed-120">Az adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="496ed-120">The data flow name.</span></span>

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

### <span data-ttu-id="496ed-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="496ed-121">-WorkspaceName</span></span>
<span data-ttu-id="496ed-122">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="496ed-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="496ed-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="496ed-123">-WorkspaceObject</span></span>
<span data-ttu-id="496ed-124">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="496ed-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="496ed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496ed-125">CommonParameters</span></span>
<span data-ttu-id="496ed-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496ed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496ed-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="496ed-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496ed-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="496ed-128">INPUTS</span></span>

### <span data-ttu-id="496ed-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="496ed-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="496ed-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="496ed-130">OUTPUTS</span></span>

### <span data-ttu-id="496ed-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="496ed-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="496ed-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="496ed-132">NOTES</span></span>

## <span data-ttu-id="496ed-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="496ed-133">RELATED LINKS</span></span>
