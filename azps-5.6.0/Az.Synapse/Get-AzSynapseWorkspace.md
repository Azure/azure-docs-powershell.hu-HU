---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: 25107456afbf85aa41dd0be600a20f7a5fcbb640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927666"
---
# <span data-ttu-id="9db65-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9db65-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="9db65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9db65-102">SYNOPSIS</span></span>
<span data-ttu-id="9db65-103">Synapse Analytics munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="9db65-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="9db65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9db65-104">SYNTAX</span></span>

### <span data-ttu-id="9db65-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9db65-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9db65-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9db65-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9db65-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9db65-107">DESCRIPTION</span></span>
<span data-ttu-id="9db65-108">A **Get-AzSynapseWorkspace** parancsmag információkat kap az Azure Synapse Analytics munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="9db65-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="9db65-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9db65-109">EXAMPLES</span></span>

### <span data-ttu-id="9db65-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9db65-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="9db65-111">Ez a parancs az összes Azure Synapse Analytics-munkaterületet az aktuális előfizetés alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9db65-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="9db65-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9db65-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="9db65-113">Ez a parancs az összes Azure Synapse Analytics-munkaterületet az aktuális előfizetés alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9db65-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="9db65-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="9db65-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="9db65-115">Ez a parancs a megadott nevű Azure Synapse Analytics munkaterületet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9db65-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="9db65-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="9db65-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="9db65-117">Ez a parancs az Azure Synapse Analytics munkaterületet kapja meg a megadott erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="9db65-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="9db65-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9db65-118">PARAMETERS</span></span>

### <span data-ttu-id="9db65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db65-119">-DefaultProfile</span></span>
<span data-ttu-id="9db65-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9db65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9db65-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9db65-121">-Name</span></span>
<span data-ttu-id="9db65-122">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9db65-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9db65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db65-123">-ResourceGroupName</span></span>
<span data-ttu-id="9db65-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9db65-124">Resource group name.</span></span>

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

### <span data-ttu-id="9db65-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9db65-125">-ResourceId</span></span>
<span data-ttu-id="9db65-126">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9db65-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="9db65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db65-127">CommonParameters</span></span>
<span data-ttu-id="9db65-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db65-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9db65-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db65-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9db65-130">INPUTS</span></span>

### <span data-ttu-id="9db65-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="9db65-131">None</span></span>

## <span data-ttu-id="9db65-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9db65-132">OUTPUTS</span></span>

### <span data-ttu-id="9db65-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9db65-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9db65-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9db65-134">NOTES</span></span>

## <span data-ttu-id="9db65-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9db65-135">RELATED LINKS</span></span>
