---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467929"
---
# <span data-ttu-id="4363e-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="4363e-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="4363e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4363e-102">SYNOPSIS</span></span>
<span data-ttu-id="4363e-103">A bevezetés törlése.</span><span class="sxs-lookup"><span data-stu-id="4363e-103">Deletes the rollout.</span></span>

## <span data-ttu-id="4363e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4363e-104">SYNTAX</span></span>

### <span data-ttu-id="4363e-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4363e-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4363e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4363e-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4363e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4363e-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4363e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4363e-108">DESCRIPTION</span></span>
<span data-ttu-id="4363e-109">A **Remove-AzDeploymentManagerRollout** parancsmag egy bevezetést töröl egy terminálállapotban.</span><span class="sxs-lookup"><span data-stu-id="4363e-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="4363e-110">Adja meg a bevezetést a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="4363e-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="4363e-111">Másik módon meg is használhatja a bevezetési objektumot vagy az Erőforrásazonosítót.</span><span class="sxs-lookup"><span data-stu-id="4363e-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="4363e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4363e-112">EXAMPLES</span></span>

### <span data-ttu-id="4363e-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="4363e-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="4363e-114">Ez a parancs törli a ContosoRollout nevű bevezetést a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="4363e-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4363e-115">2. példa: Bevezetés törlése az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="4363e-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="4363e-116">Ez a parancs törli a ContosoRollout nevű bevezetést a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="4363e-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4363e-117">3. példa: Bevezetés törlése a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="4363e-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="4363e-118">Ez a parancs törli a névvel és erőforráscsoporttal egyező névvel és erőforráscsoportnévvel $rolloutObject nevét.</span><span class="sxs-lookup"><span data-stu-id="4363e-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="4363e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4363e-119">PARAMETERS</span></span>

### <span data-ttu-id="4363e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4363e-120">-DefaultProfile</span></span>
<span data-ttu-id="4363e-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4363e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4363e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4363e-122">-InputObject</span></span>
<span data-ttu-id="4363e-123">Az eltávolítható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="4363e-123">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4363e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4363e-124">-Name</span></span>
<span data-ttu-id="4363e-125">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="4363e-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="4363e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4363e-126">-PassThru</span></span>
<span data-ttu-id="4363e-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4363e-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4363e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4363e-128">-ResourceGroupName</span></span>
<span data-ttu-id="4363e-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="4363e-129">The resource group.</span></span>

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

### <span data-ttu-id="4363e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4363e-130">-ResourceId</span></span>
<span data-ttu-id="4363e-131">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4363e-131">The resource identifier.</span></span>

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

### <span data-ttu-id="4363e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4363e-132">-Confirm</span></span>
<span data-ttu-id="4363e-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4363e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4363e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4363e-134">-WhatIf</span></span>
<span data-ttu-id="4363e-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4363e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4363e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4363e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4363e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4363e-137">CommonParameters</span></span>
<span data-ttu-id="4363e-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4363e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4363e-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4363e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4363e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4363e-140">INPUTS</span></span>

### <span data-ttu-id="4363e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4363e-141">System.String</span></span>

### <span data-ttu-id="4363e-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="4363e-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="4363e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4363e-143">OUTPUTS</span></span>

### <span data-ttu-id="4363e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4363e-144">System.Boolean</span></span>

## <span data-ttu-id="4363e-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4363e-145">NOTES</span></span>

## <span data-ttu-id="4363e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4363e-146">RELATED LINKS</span></span>
