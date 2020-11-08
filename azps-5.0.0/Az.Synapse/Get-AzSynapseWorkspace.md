---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187916"
---
# <span data-ttu-id="e271c-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e271c-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="e271c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e271c-102">SYNOPSIS</span></span>
<span data-ttu-id="e271c-103">A szinapszis Analytics-munkaterületet kapja.</span><span class="sxs-lookup"><span data-stu-id="e271c-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e271c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e271c-104">SYNTAX</span></span>

### <span data-ttu-id="e271c-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e271c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e271c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e271c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e271c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e271c-107">DESCRIPTION</span></span>
<span data-ttu-id="e271c-108">A **Get-AzSynapseWorkspace** parancsmag információkat kap az Azure szinapszis Analytics-munkaterületéről.</span><span class="sxs-lookup"><span data-stu-id="e271c-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e271c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e271c-109">EXAMPLES</span></span>

### <span data-ttu-id="e271c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e271c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="e271c-111">Ez a parancs a jelenlegi előfizetés alatt az Azure szinapszis Analytics-munkaterületeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e271c-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="e271c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e271c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="e271c-113">Ez a parancs a jelenlegi előfizetés alatt az Azure szinapszis Analytics-munkaterületeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e271c-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="e271c-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="e271c-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="e271c-115">Ez a parancs az Azure szinapszis Analytics-munkaterületet kapja meg a megadott néven.</span><span class="sxs-lookup"><span data-stu-id="e271c-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="e271c-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="e271c-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="e271c-117">Ez a parancs az Azure szinapszis Analytics-munkaterületet kapja meg a megadott erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="e271c-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="e271c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e271c-118">PARAMETERS</span></span>

### <span data-ttu-id="e271c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e271c-119">-DefaultProfile</span></span>
<span data-ttu-id="e271c-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e271c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e271c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e271c-121">-Name</span></span>
<span data-ttu-id="e271c-122">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="e271c-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e271c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e271c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e271c-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e271c-124">Resource group name.</span></span>

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

### <span data-ttu-id="e271c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e271c-125">-ResourceId</span></span>
<span data-ttu-id="e271c-126">A szinapszis-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e271c-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="e271c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e271c-127">CommonParameters</span></span>
<span data-ttu-id="e271c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e271c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e271c-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e271c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e271c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e271c-130">INPUTS</span></span>

### <span data-ttu-id="e271c-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="e271c-131">None</span></span>

## <span data-ttu-id="e271c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e271c-132">OUTPUTS</span></span>

### <span data-ttu-id="e271c-133">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e271c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e271c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e271c-134">NOTES</span></span>

## <span data-ttu-id="e271c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e271c-135">RELATED LINKS</span></span>