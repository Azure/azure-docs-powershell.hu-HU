---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383696"
---
# <span data-ttu-id="7e6c8-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e6c8-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="7e6c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6c8-103">Synapse Analytics munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7e6c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e6c8-104">SYNTAX</span></span>

### <span data-ttu-id="7e6c8-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e6c8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e6c8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e6c8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e6c8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e6c8-107">DESCRIPTION</span></span>
<span data-ttu-id="7e6c8-108">A **Get-AzSynapseWorkspace** parancsmag információkat kap az Azure Synapse Analytics munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7e6c8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e6c8-109">EXAMPLES</span></span>

### <span data-ttu-id="7e6c8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e6c8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="7e6c8-111">Ez a parancs az összes Azure Synapse Analytics-munkaterületet az aktuális előfizetés alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="7e6c8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7e6c8-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="7e6c8-113">Ez a parancs az összes Azure Synapse Analytics-munkaterületet az aktuális előfizetés alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="7e6c8-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="7e6c8-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="7e6c8-115">Ez a parancs a megadott nevű Azure Synapse Analytics munkaterületet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="7e6c8-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="7e6c8-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="7e6c8-117">Ez a parancs az Azure Synapse Analytics munkaterületet kapja meg a megadott erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="7e6c8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e6c8-118">PARAMETERS</span></span>

### <span data-ttu-id="7e6c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6c8-119">-DefaultProfile</span></span>
<span data-ttu-id="7e6c8-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e6c8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e6c8-121">-Name</span></span>
<span data-ttu-id="7e6c8-122">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e6c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e6c8-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-124">Resource group name.</span></span>

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

### <span data-ttu-id="7e6c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e6c8-125">-ResourceId</span></span>
<span data-ttu-id="7e6c8-126">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="7e6c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6c8-127">CommonParameters</span></span>
<span data-ttu-id="7e6c8-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6c8-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e6c8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6c8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e6c8-130">INPUTS</span></span>

### <span data-ttu-id="7e6c8-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="7e6c8-131">None</span></span>

## <span data-ttu-id="7e6c8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e6c8-132">OUTPUTS</span></span>

### <span data-ttu-id="7e6c8-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e6c8-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7e6c8-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e6c8-134">NOTES</span></span>

## <span data-ttu-id="7e6c8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e6c8-135">RELATED LINKS</span></span>
