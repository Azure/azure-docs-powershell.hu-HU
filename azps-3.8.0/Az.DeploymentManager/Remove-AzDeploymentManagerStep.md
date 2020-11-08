---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014377"
---
# <span data-ttu-id="8a201-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="8a201-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="8a201-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a201-102">SYNOPSIS</span></span>
<span data-ttu-id="8a201-103">Törli a lépést.</span><span class="sxs-lookup"><span data-stu-id="8a201-103">Deletes the step.</span></span>

## <span data-ttu-id="8a201-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a201-104">SYNTAX</span></span>

### <span data-ttu-id="8a201-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a201-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a201-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a201-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a201-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8a201-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a201-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a201-108">DESCRIPTION</span></span>
<span data-ttu-id="8a201-109">A **Remove-AzDeploymentManagerStep** parancsmag egy lépést töröl.</span><span class="sxs-lookup"><span data-stu-id="8a201-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="8a201-110">Adja meg a kívánt lépést a nevével és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="8a201-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="8a201-111">Másik lehetőségként a Step objektum vagy a ResourceId is megadható.</span><span class="sxs-lookup"><span data-stu-id="8a201-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="8a201-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8a201-112">EXAMPLES</span></span>

### <span data-ttu-id="8a201-113">1. példa: lépés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8a201-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="8a201-114">Ez a parancs törli a ContosoService1WaitStep nevű lépést a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8a201-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="8a201-115">2. példa: lépés eltávolítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="8a201-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="8a201-116">Ez a parancs törli a ContosoService1WaitStep nevű lépést a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8a201-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="8a201-117">3. példa: lépés eltávolítása New-AzDeploymentManagerStep által visszaadott objektum használatával</span><span class="sxs-lookup"><span data-stu-id="8a201-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="8a201-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8a201-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="8a201-119">Ez a parancs törli azt a lépést, amelynek a neve és a ResourceGroup meg kell egyeznie az $stepObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="8a201-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="8a201-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a201-120">PARAMETERS</span></span>

### <span data-ttu-id="8a201-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a201-121">-DefaultProfile</span></span>
<span data-ttu-id="8a201-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a201-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a201-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a201-123">-InputObject</span></span>
<span data-ttu-id="8a201-124">Az eltávolítandó lépés.</span><span class="sxs-lookup"><span data-stu-id="8a201-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a201-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a201-125">-Name</span></span>
<span data-ttu-id="8a201-126">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8a201-126">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a201-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a201-127">-PassThru</span></span>
<span data-ttu-id="8a201-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8a201-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8a201-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a201-129">-ResourceGroupName</span></span>
<span data-ttu-id="8a201-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="8a201-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a201-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a201-131">-ResourceId</span></span>
<span data-ttu-id="8a201-132">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8a201-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a201-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a201-133">-Confirm</span></span>
<span data-ttu-id="8a201-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a201-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a201-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a201-135">-WhatIf</span></span>
<span data-ttu-id="8a201-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8a201-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a201-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a201-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a201-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a201-138">CommonParameters</span></span>
<span data-ttu-id="8a201-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a201-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a201-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8a201-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a201-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a201-141">INPUTS</span></span>

### <span data-ttu-id="8a201-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8a201-142">System.String</span></span>

### <span data-ttu-id="8a201-143">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="8a201-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="8a201-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a201-144">OUTPUTS</span></span>

### <span data-ttu-id="8a201-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a201-145">System.Boolean</span></span>

## <span data-ttu-id="8a201-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a201-146">NOTES</span></span>

## <span data-ttu-id="8a201-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a201-147">RELATED LINKS</span></span>
