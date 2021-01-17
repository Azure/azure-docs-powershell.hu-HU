---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340025"
---
# <span data-ttu-id="6ff6f-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6ff6f-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="6ff6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ff6f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff6f-103">Törli a lépést.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-103">Deletes the step.</span></span>

## <span data-ttu-id="6ff6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ff6f-104">SYNTAX</span></span>

### <span data-ttu-id="6ff6f-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ff6f-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff6f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ff6f-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff6f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ff6f-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff6f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ff6f-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff6f-109">Az **Remove-AzDeploymentManagerStep** parancsmag töröl egy lépést.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="6ff6f-110">Adja meg a lépést a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="6ff6f-111">Másik lépésként meg is használhatja a Lépés objektumot vagy az Erőforrásazonosítót.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="6ff6f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ff6f-112">EXAMPLES</span></span>

### <span data-ttu-id="6ff6f-113">1. példa: Lépés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6ff6f-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="6ff6f-114">Ez a parancs törli a ContosoService1WaitStep nevű lépést a ContosoResourceGroup-ban.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6ff6f-115">2. példa: Lépés eltávolítása az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="6ff6f-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="6ff6f-116">Ez a parancs törli a ContosoService1WaitStep nevű lépést a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6ff6f-117">3. példa: Lépés eltávolítása a következő által visszaadott New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6ff6f-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="6ff6f-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="6ff6f-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="6ff6f-119">Ez a parancs törli azt a lépést, amelynek neve és ResourceGroup tulajdonsága megegyezik a $stepObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="6ff6f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ff6f-120">PARAMETERS</span></span>

### <span data-ttu-id="6ff6f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff6f-121">-DefaultProfile</span></span>
<span data-ttu-id="6ff6f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff6f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ff6f-123">-InputObject</span></span>
<span data-ttu-id="6ff6f-124">Az eltávolítható lépés.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-124">The step to be removed.</span></span>

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

### <span data-ttu-id="6ff6f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6ff6f-125">-Name</span></span>
<span data-ttu-id="6ff6f-126">A lépés neve.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-126">The name of the step.</span></span>

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

### <span data-ttu-id="6ff6f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ff6f-127">-PassThru</span></span>
<span data-ttu-id="6ff6f-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6ff6f-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6ff6f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff6f-129">-ResourceGroupName</span></span>
<span data-ttu-id="6ff6f-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-130">The resource group.</span></span>

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

### <span data-ttu-id="6ff6f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ff6f-131">-ResourceId</span></span>
<span data-ttu-id="6ff6f-132">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-132">The resource identifier.</span></span>

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

### <span data-ttu-id="6ff6f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ff6f-133">-Confirm</span></span>
<span data-ttu-id="6ff6f-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff6f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff6f-135">-WhatIf</span></span>
<span data-ttu-id="6ff6f-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff6f-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff6f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff6f-138">CommonParameters</span></span>
<span data-ttu-id="6ff6f-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff6f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff6f-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ff6f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff6f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ff6f-141">INPUTS</span></span>

### <span data-ttu-id="6ff6f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6ff6f-142">System.String</span></span>

### <span data-ttu-id="6ff6f-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="6ff6f-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6ff6f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff6f-144">OUTPUTS</span></span>

### <span data-ttu-id="6ff6f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ff6f-145">System.Boolean</span></span>

## <span data-ttu-id="6ff6f-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ff6f-146">NOTES</span></span>

## <span data-ttu-id="6ff6f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ff6f-147">RELATED LINKS</span></span>
