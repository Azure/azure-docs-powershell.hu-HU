---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187132"
---
# <span data-ttu-id="68d96-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="68d96-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="68d96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68d96-102">SYNOPSIS</span></span>
<span data-ttu-id="68d96-103">A szinapszis Analytics-munkaterületének törlése.</span><span class="sxs-lookup"><span data-stu-id="68d96-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="68d96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68d96-104">SYNTAX</span></span>

### <span data-ttu-id="68d96-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68d96-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d96-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68d96-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d96-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68d96-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68d96-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="68d96-108">DESCRIPTION</span></span>
<span data-ttu-id="68d96-109">A **Remove-AzSynapseWorkspace** parancsmag véglegesen törli az Azure szinapszis Analytics-munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="68d96-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="68d96-110">Példák</span><span class="sxs-lookup"><span data-stu-id="68d96-110">EXAMPLES</span></span>

### <span data-ttu-id="68d96-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68d96-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="68d96-112">Ez a parancs törli az Azure szinapszis Analytics-munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="68d96-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="68d96-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="68d96-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="68d96-114">Ez a parancs egy Azure szinapszis Analytics-munkaterületet töröl egy csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="68d96-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="68d96-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="68d96-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="68d96-116">Ez a parancs az Azure szinapszis Analytics-munkaterületet egy, a megadott erőforrás-AZONOSÍTÓval rendelkező csővezetéken keresztül törli.</span><span class="sxs-lookup"><span data-stu-id="68d96-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="68d96-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68d96-117">PARAMETERS</span></span>

### <span data-ttu-id="68d96-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68d96-118">-AsJob</span></span>
<span data-ttu-id="68d96-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="68d96-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68d96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d96-120">-DefaultProfile</span></span>
<span data-ttu-id="68d96-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68d96-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68d96-122">-InputObject</span></span>
<span data-ttu-id="68d96-123">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="68d96-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68d96-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68d96-124">-Name</span></span>
<span data-ttu-id="68d96-125">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="68d96-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d96-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68d96-126">-PassThru</span></span>
<span data-ttu-id="68d96-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="68d96-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="68d96-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="68d96-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="68d96-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d96-129">-ResourceGroupName</span></span>
<span data-ttu-id="68d96-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="68d96-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d96-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68d96-131">-ResourceId</span></span>
<span data-ttu-id="68d96-132">A szinapszis-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="68d96-132">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d96-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68d96-133">-Confirm</span></span>
<span data-ttu-id="68d96-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68d96-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d96-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d96-135">-WhatIf</span></span>
<span data-ttu-id="68d96-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68d96-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68d96-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68d96-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d96-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d96-138">CommonParameters</span></span>
<span data-ttu-id="68d96-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68d96-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d96-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="68d96-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d96-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d96-141">INPUTS</span></span>

### <span data-ttu-id="68d96-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="68d96-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="68d96-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d96-143">OUTPUTS</span></span>

### <span data-ttu-id="68d96-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68d96-144">System.Boolean</span></span>

## <span data-ttu-id="68d96-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68d96-145">NOTES</span></span>

## <span data-ttu-id="68d96-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68d96-146">RELATED LINKS</span></span>
