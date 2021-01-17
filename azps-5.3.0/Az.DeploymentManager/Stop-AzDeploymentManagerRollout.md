---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387336"
---
# <span data-ttu-id="7336e-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7336e-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="7336e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7336e-102">SYNOPSIS</span></span>
<span data-ttu-id="7336e-103">Leállítja a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="7336e-103">Stops the rollout.</span></span>

## <span data-ttu-id="7336e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7336e-104">SYNTAX</span></span>

### <span data-ttu-id="7336e-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7336e-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7336e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7336e-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7336e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7336e-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7336e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7336e-108">DESCRIPTION</span></span>
<span data-ttu-id="7336e-109">A **Stop-AzDeploymentManagerRollout** parancsmag leállítja a folyamatban lévő bevezetést, és visszaad egy objektumot, amely a bevezetés aktuális állapotát képviseli.</span><span class="sxs-lookup"><span data-stu-id="7336e-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="7336e-110">Adja meg a bevezetést a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="7336e-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7336e-111">Másik módon meg is használhatja a bevezetési objektumot vagy az Erőforrásazonosítót.</span><span class="sxs-lookup"><span data-stu-id="7336e-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="7336e-112">Felhívjuk a figyelmét arra, hogy miután leállt a bevezetés, az nem folytatható és nem indítható újra.</span><span class="sxs-lookup"><span data-stu-id="7336e-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="7336e-113">Csak új bevezetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="7336e-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="7336e-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7336e-114">EXAMPLES</span></span>

### <span data-ttu-id="7336e-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="7336e-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="7336e-116">Ez a parancs leállítja a ContosoRollout nevű bevezetést a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="7336e-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="7336e-117">2. példa: Bevezetés leállítása az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="7336e-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7336e-118">Ez a parancs leállítja a ContosoRollout nevű bevezetést a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="7336e-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7336e-119">3. példa: Bevezetés leállítása a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="7336e-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="7336e-120">Ez a parancs leállítja az olyan bevezetést, amelynek neve és ResourceGroup tulajdonsága megegyezik a $rolloutObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="7336e-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7336e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7336e-121">PARAMETERS</span></span>

### <span data-ttu-id="7336e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7336e-122">-DefaultProfile</span></span>
<span data-ttu-id="7336e-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7336e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7336e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7336e-124">-Force</span></span>
<span data-ttu-id="7336e-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7336e-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7336e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7336e-126">-InputObject</span></span>
<span data-ttu-id="7336e-127">Az eltávolítható bevezetés.</span><span class="sxs-lookup"><span data-stu-id="7336e-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="7336e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7336e-128">-Name</span></span>
<span data-ttu-id="7336e-129">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="7336e-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="7336e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7336e-130">-ResourceGroupName</span></span>
<span data-ttu-id="7336e-131">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="7336e-131">The resource group.</span></span>

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

### <span data-ttu-id="7336e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7336e-132">-ResourceId</span></span>
<span data-ttu-id="7336e-133">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7336e-133">The resource identifier.</span></span>

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

### <span data-ttu-id="7336e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7336e-134">-Confirm</span></span>
<span data-ttu-id="7336e-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7336e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7336e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7336e-136">-WhatIf</span></span>
<span data-ttu-id="7336e-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7336e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7336e-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7336e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7336e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7336e-139">CommonParameters</span></span>
<span data-ttu-id="7336e-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7336e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7336e-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7336e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7336e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7336e-142">INPUTS</span></span>

### <span data-ttu-id="7336e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7336e-143">System.String</span></span>

### <span data-ttu-id="7336e-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="7336e-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7336e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7336e-145">OUTPUTS</span></span>

### <span data-ttu-id="7336e-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="7336e-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7336e-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7336e-147">NOTES</span></span>

## <span data-ttu-id="7336e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7336e-148">RELATED LINKS</span></span>
