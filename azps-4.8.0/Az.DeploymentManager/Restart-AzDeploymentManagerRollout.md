---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182808"
---
# <span data-ttu-id="fc3ca-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="fc3ca-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="fc3ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3ca-103">Sikertelen bevezetés újraindítása.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="fc3ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc3ca-104">SYNTAX</span></span>

### <span data-ttu-id="fc3ca-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc3ca-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3ca-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc3ca-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3ca-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc3ca-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc3ca-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc3ca-108">DESCRIPTION</span></span>
<span data-ttu-id="fc3ca-109">Az **Újraindítás – AzDeploymentManagerRollout** parancsmag újraindítja a sikertelen bevezetést, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="fc3ca-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="fc3ca-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="fc3ca-112">Opcionális paraméter: a SkipSucceeded lehetővé teszi, hogy a bevezetés előző futása során minden követett lépést kiugorjon.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="fc3ca-113">Példák</span><span class="sxs-lookup"><span data-stu-id="fc3ca-113">EXAMPLES</span></span>

### <span data-ttu-id="fc3ca-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc3ca-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="fc3ca-115">Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="fc3ca-116">A SkipSucceeded jelző azt jelzi, hogy a már sikeresen futtatott összes lépést ki kell hagynia, és a kivezetésnek továbbra is az utolsó sikertelen végrehajtástól kell lépnie.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="fc3ca-117">2. példa: a bevezetés újraindítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="fc3ca-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="fc3ca-118">Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc3ca-119">3. példa: a bevezetés újraindítása a kivezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="fc3ca-120">Ez a parancs elindítja a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject név-és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="fc3ca-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc3ca-121">PARAMETERS</span></span>

### <span data-ttu-id="fc3ca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc3ca-122">-DefaultProfile</span></span>
<span data-ttu-id="fc3ca-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc3ca-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc3ca-124">-InputObject</span></span>
<span data-ttu-id="fc3ca-125">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="fc3ca-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc3ca-126">-Name</span></span>
<span data-ttu-id="fc3ca-127">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="fc3ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc3ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc3ca-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-129">The resource group.</span></span>

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

### <span data-ttu-id="fc3ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc3ca-130">-ResourceId</span></span>
<span data-ttu-id="fc3ca-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-131">The resource identifier.</span></span>

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

### <span data-ttu-id="fc3ca-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="fc3ca-132">-SkipSucceeded</span></span>
<span data-ttu-id="fc3ca-133">A bevezetési folyamat előző futásában sikeres lépések elhagyása.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="fc3ca-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc3ca-134">-Confirm</span></span>
<span data-ttu-id="fc3ca-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc3ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc3ca-136">-WhatIf</span></span>
<span data-ttu-id="fc3ca-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc3ca-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc3ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3ca-139">CommonParameters</span></span>
<span data-ttu-id="fc3ca-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc3ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3ca-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fc3ca-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3ca-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc3ca-142">INPUTS</span></span>

### <span data-ttu-id="fc3ca-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fc3ca-143">System.String</span></span>

### <span data-ttu-id="fc3ca-144">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="fc3ca-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="fc3ca-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc3ca-145">OUTPUTS</span></span>

### <span data-ttu-id="fc3ca-146">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="fc3ca-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="fc3ca-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc3ca-147">NOTES</span></span>

## <span data-ttu-id="fc3ca-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc3ca-148">RELATED LINKS</span></span>
