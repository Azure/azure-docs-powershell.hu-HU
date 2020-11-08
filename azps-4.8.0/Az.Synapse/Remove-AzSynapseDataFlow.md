---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: dcfcd391d1103b0755a3ffae481e4f1bd5fde2c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025627"
---
# <span data-ttu-id="09c67-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="09c67-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="09c67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09c67-102">SYNOPSIS</span></span>
<span data-ttu-id="09c67-103">Adatforgalom eltávolítása a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="09c67-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="09c67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09c67-104">SYNTAX</span></span>

### <span data-ttu-id="09c67-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09c67-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c67-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="09c67-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c67-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="09c67-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c67-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="09c67-108">DESCRIPTION</span></span>
<span data-ttu-id="09c67-109">A **Remove-AzSynapseDataFlow** parancsmag eltávolítja a munkaterületről származó adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="09c67-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="09c67-110">Példák</span><span class="sxs-lookup"><span data-stu-id="09c67-110">EXAMPLES</span></span>

### <span data-ttu-id="09c67-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="09c67-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="09c67-112">Ez a parancs eltávolítja a ContosoDataFlow nevű adatfolyamot a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="09c67-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="09c67-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09c67-113">PARAMETERS</span></span>

### <span data-ttu-id="09c67-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09c67-114">-AsJob</span></span>
<span data-ttu-id="09c67-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="09c67-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09c67-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c67-116">-DefaultProfile</span></span>
<span data-ttu-id="09c67-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09c67-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09c67-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09c67-118">-InputObject</span></span>
<span data-ttu-id="09c67-119">Az adatfolyam-objektum.</span><span class="sxs-lookup"><span data-stu-id="09c67-119">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09c67-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09c67-120">-Name</span></span>
<span data-ttu-id="09c67-121">Az adatforgalom neve.</span><span class="sxs-lookup"><span data-stu-id="09c67-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c67-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09c67-122">-PassThru</span></span>
<span data-ttu-id="09c67-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="09c67-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="09c67-124">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="09c67-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="09c67-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09c67-125">-WorkspaceName</span></span>
<span data-ttu-id="09c67-126">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="09c67-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="09c67-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09c67-127">-WorkspaceObject</span></span>
<span data-ttu-id="09c67-128">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="09c67-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="09c67-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09c67-129">-Confirm</span></span>
<span data-ttu-id="09c67-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09c67-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c67-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c67-131">-WhatIf</span></span>
<span data-ttu-id="09c67-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09c67-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09c67-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09c67-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c67-134">CommonParameters</span></span>
<span data-ttu-id="09c67-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09c67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c67-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="09c67-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c67-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09c67-137">INPUTS</span></span>

### <span data-ttu-id="09c67-138">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="09c67-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="09c67-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="09c67-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="09c67-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09c67-140">OUTPUTS</span></span>

### <span data-ttu-id="09c67-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09c67-141">System.Boolean</span></span>

## <span data-ttu-id="09c67-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09c67-142">NOTES</span></span>

## <span data-ttu-id="09c67-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09c67-143">RELATED LINKS</span></span>
