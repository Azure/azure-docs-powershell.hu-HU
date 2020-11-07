---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: e53f2e72a10befb126bc9cc20dc12bf8990b1553
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670980"
---
# <span data-ttu-id="620e7-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="620e7-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="620e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="620e7-102">SYNOPSIS</span></span>
<span data-ttu-id="620e7-103">Sikertelen bevezetés újraindítása.</span><span class="sxs-lookup"><span data-stu-id="620e7-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="620e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="620e7-104">SYNTAX</span></span>

### <span data-ttu-id="620e7-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="620e7-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="620e7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="620e7-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="620e7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="620e7-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="620e7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="620e7-108">DESCRIPTION</span></span>
<span data-ttu-id="620e7-109">Az **Újraindítás – AzDeploymentManagerRollout** parancsmag újraindítja a sikertelen bevezetést, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="620e7-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="620e7-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="620e7-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="620e7-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="620e7-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="620e7-112">Opcionális paraméter: a SkipSucceeded lehetővé teszi, hogy a bevezetés előző futása során minden követett lépést kiugorjon.</span><span class="sxs-lookup"><span data-stu-id="620e7-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="620e7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="620e7-113">EXAMPLES</span></span>

### <span data-ttu-id="620e7-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="620e7-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="620e7-115">Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="620e7-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="620e7-116">A SkipSucceeded jelző azt jelzi, hogy a már sikeresen futtatott összes lépést ki kell hagynia, és a kivezetésnek továbbra is az utolsó sikertelen végrehajtástól kell lépnie.</span><span class="sxs-lookup"><span data-stu-id="620e7-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="620e7-117">2. példa: a bevezetés újraindítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="620e7-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="620e7-118">Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="620e7-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="620e7-119">3. példa: a bevezetés újraindítása a kivezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="620e7-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="620e7-120">Ez a parancs elindítja a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject név-és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="620e7-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="620e7-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="620e7-121">PARAMETERS</span></span>

### <span data-ttu-id="620e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620e7-122">-DefaultProfile</span></span>
<span data-ttu-id="620e7-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="620e7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="620e7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="620e7-124">-InputObject</span></span>
<span data-ttu-id="620e7-125">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="620e7-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="620e7-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="620e7-126">-Name</span></span>
<span data-ttu-id="620e7-127">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="620e7-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="620e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="620e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="620e7-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="620e7-129">The resource group.</span></span>

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

### <span data-ttu-id="620e7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="620e7-130">-ResourceId</span></span>
<span data-ttu-id="620e7-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="620e7-131">The resource identifier.</span></span>

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

### <span data-ttu-id="620e7-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="620e7-132">-SkipSucceeded</span></span>
<span data-ttu-id="620e7-133">A bevezetési folyamat előző futásában sikeres lépések elhagyása.</span><span class="sxs-lookup"><span data-stu-id="620e7-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="620e7-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="620e7-134">-Confirm</span></span>
<span data-ttu-id="620e7-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="620e7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="620e7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="620e7-136">-WhatIf</span></span>
<span data-ttu-id="620e7-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="620e7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="620e7-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="620e7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="620e7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620e7-139">CommonParameters</span></span>
<span data-ttu-id="620e7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="620e7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620e7-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620e7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620e7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="620e7-142">INPUTS</span></span>

### <span data-ttu-id="620e7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="620e7-143">System.String</span></span>

### <span data-ttu-id="620e7-144">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="620e7-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="620e7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="620e7-145">OUTPUTS</span></span>

### <span data-ttu-id="620e7-146">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="620e7-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="620e7-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="620e7-147">NOTES</span></span>

## <span data-ttu-id="620e7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="620e7-148">RELATED LINKS</span></span>
