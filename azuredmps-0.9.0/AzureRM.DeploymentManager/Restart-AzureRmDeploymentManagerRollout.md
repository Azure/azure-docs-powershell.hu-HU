---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491620"
---
# <span data-ttu-id="aaf75-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="aaf75-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="aaf75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aaf75-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf75-103">Sikertelen bevezetés újraindítása.</span><span class="sxs-lookup"><span data-stu-id="aaf75-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="aaf75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aaf75-104">SYNTAX</span></span>

### <span data-ttu-id="aaf75-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aaf75-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf75-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaf75-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf75-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="aaf75-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaf75-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aaf75-108">DESCRIPTION</span></span>
<span data-ttu-id="aaf75-109">Az **Újraindítás – AzureRmDeploymentManagerRollout** parancsmag újraindítja a sikertelen bevezetést, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="aaf75-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="aaf75-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="aaf75-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="aaf75-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="aaf75-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="aaf75-112">Opcionális paraméter: a SkipSucceeded lehetővé teszi, hogy a bevezetés előző futása során minden követett lépést kiugorjon.</span><span class="sxs-lookup"><span data-stu-id="aaf75-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="aaf75-113">Példák</span><span class="sxs-lookup"><span data-stu-id="aaf75-113">EXAMPLES</span></span>

### <span data-ttu-id="aaf75-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aaf75-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="aaf75-115">Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="aaf75-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="aaf75-116">A SkipSucceeded jelző azt jelzi, hogy a már sikeresen futtatott összes lépést ki kell hagynia, és a kivezetésnek továbbra is az utolsó sikertelen végrehajtástól kell lépnie.</span><span class="sxs-lookup"><span data-stu-id="aaf75-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="aaf75-117">2. példa: a bevezetés újraindítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="aaf75-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="aaf75-118">Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="aaf75-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="aaf75-119">3. példa: a bevezetés újraindítása a kivezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="aaf75-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="aaf75-120">Ez a parancs elindítja a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject név-és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="aaf75-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="aaf75-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aaf75-121">PARAMETERS</span></span>

### <span data-ttu-id="aaf75-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf75-122">-DefaultProfile</span></span>
<span data-ttu-id="aaf75-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaf75-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf75-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aaf75-124">-Name</span></span>
<span data-ttu-id="aaf75-125">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="aaf75-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf75-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf75-126">-ResourceGroupName</span></span>
<span data-ttu-id="aaf75-127">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="aaf75-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf75-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaf75-128">-ResourceId</span></span>
<span data-ttu-id="aaf75-129">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="aaf75-129">The resource identifier.</span></span>

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

### <span data-ttu-id="aaf75-130">-Bevezetés</span><span class="sxs-lookup"><span data-stu-id="aaf75-130">-Rollout</span></span>
<span data-ttu-id="aaf75-131">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="aaf75-131">The resource to be removed.</span></span>

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

### <span data-ttu-id="aaf75-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="aaf75-132">-SkipSucceeded</span></span>
<span data-ttu-id="aaf75-133">A bevezetési folyamat előző futásában sikeres lépések elhagyása.</span><span class="sxs-lookup"><span data-stu-id="aaf75-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="aaf75-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aaf75-134">-Confirm</span></span>
<span data-ttu-id="aaf75-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aaf75-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaf75-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf75-136">-WhatIf</span></span>
<span data-ttu-id="aaf75-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aaf75-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaf75-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aaf75-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaf75-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf75-139">CommonParameters</span></span>
<span data-ttu-id="aaf75-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aaf75-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf75-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf75-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf75-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaf75-142">INPUTS</span></span>

### <span data-ttu-id="aaf75-143">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="aaf75-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="aaf75-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaf75-144">OUTPUTS</span></span>

### <span data-ttu-id="aaf75-145">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="aaf75-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="aaf75-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aaf75-146">NOTES</span></span>

## <span data-ttu-id="aaf75-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaf75-147">RELATED LINKS</span></span>

[<span data-ttu-id="aaf75-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="aaf75-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="aaf75-149">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="aaf75-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="aaf75-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="aaf75-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)