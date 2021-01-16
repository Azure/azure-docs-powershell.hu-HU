---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333629"
---
# <span data-ttu-id="156c3-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="156c3-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="156c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156c3-102">SYNOPSIS</span></span>
<span data-ttu-id="156c3-103">Egy sikertelen bevezetést indít újra.</span><span class="sxs-lookup"><span data-stu-id="156c3-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="156c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="156c3-104">SYNTAX</span></span>

### <span data-ttu-id="156c3-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="156c3-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="156c3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="156c3-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="156c3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="156c3-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="156c3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="156c3-108">DESCRIPTION</span></span>
<span data-ttu-id="156c3-109">Az **Restart-AzDeploymentManagerRollout** parancsmag egy sikertelen bevezetést indít újra, és visszaad egy olyan objektumot, amely az adott bevezetést képviseli a bevezetés folyamatának részletes adataival együtt.</span><span class="sxs-lookup"><span data-stu-id="156c3-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="156c3-110">Adja meg a bevezetést a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="156c3-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="156c3-111">Másik módon meg is használhatja a bevezetési objektumot vagy az Erőforrásazonosítót.</span><span class="sxs-lookup"><span data-stu-id="156c3-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="156c3-112">Az opcionális skipSucceed paraméter lehetővé teszi, hogy kihagyja az előző futtatás összes sikeres lépését.</span><span class="sxs-lookup"><span data-stu-id="156c3-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="156c3-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="156c3-113">EXAMPLES</span></span>

### <span data-ttu-id="156c3-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="156c3-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="156c3-115">Ez a parancs újraindítja a ContosoRollout nevű bevezetést a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="156c3-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="156c3-116">A Kihagyott jelölő azt jelzi, hogy a már sikeresen lefutott összes lépést át kell hagyni, és a bevezetésnek onnan kell folytatnia a végrehajtást, ahol legutóbb sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="156c3-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="156c3-117">2. példa: Bevezetés újraindítása az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="156c3-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="156c3-118">Ez a parancs újraindítja a ContosoRollout nevű bevezetést a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="156c3-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="156c3-119">3. példa: Bevezetés újraindítása a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="156c3-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="156c3-120">Ez a parancs egy olyan bevezetést indít újra, amelynek neve és ResourceGroup tulajdonsága megegyezik a név és az erőforráscsoport $rolloutObject tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="156c3-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="156c3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="156c3-121">PARAMETERS</span></span>

### <span data-ttu-id="156c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156c3-122">-DefaultProfile</span></span>
<span data-ttu-id="156c3-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="156c3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="156c3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="156c3-124">-InputObject</span></span>
<span data-ttu-id="156c3-125">Az eltávolítható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="156c3-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="156c3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="156c3-126">-Name</span></span>
<span data-ttu-id="156c3-127">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="156c3-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="156c3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156c3-128">-ResourceGroupName</span></span>
<span data-ttu-id="156c3-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="156c3-129">The resource group.</span></span>

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

### <span data-ttu-id="156c3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="156c3-130">-ResourceId</span></span>
<span data-ttu-id="156c3-131">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="156c3-131">The resource identifier.</span></span>

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

### <span data-ttu-id="156c3-132">-SkipSucceed</span><span class="sxs-lookup"><span data-stu-id="156c3-132">-SkipSucceeded</span></span>
<span data-ttu-id="156c3-133">Kihagyhatja a bevezetés előző futtatása során sikeres lépéseket.</span><span class="sxs-lookup"><span data-stu-id="156c3-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="156c3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="156c3-134">-Confirm</span></span>
<span data-ttu-id="156c3-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="156c3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="156c3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="156c3-136">-WhatIf</span></span>
<span data-ttu-id="156c3-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="156c3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="156c3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="156c3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="156c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156c3-139">CommonParameters</span></span>
<span data-ttu-id="156c3-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156c3-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="156c3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156c3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="156c3-142">INPUTS</span></span>

### <span data-ttu-id="156c3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="156c3-143">System.String</span></span>

### <span data-ttu-id="156c3-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="156c3-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="156c3-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="156c3-145">OUTPUTS</span></span>

### <span data-ttu-id="156c3-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="156c3-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="156c3-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="156c3-147">NOTES</span></span>

## <span data-ttu-id="156c3-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="156c3-148">RELATED LINKS</span></span>
