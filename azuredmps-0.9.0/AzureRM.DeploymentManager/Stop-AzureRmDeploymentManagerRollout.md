---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671704"
---
# <span data-ttu-id="f6b78-101">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="f6b78-101">Stop-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="f6b78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6b78-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b78-103">Befejezi a kiépítést.</span><span class="sxs-lookup"><span data-stu-id="f6b78-103">Stops a rollout in progress.</span></span>

## <span data-ttu-id="f6b78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6b78-104">SYNTAX</span></span>

### <span data-ttu-id="f6b78-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6b78-105">Interactive (Default)</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b78-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6b78-106">ResourceId</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b78-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f6b78-107">InputObject</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6b78-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6b78-108">DESCRIPTION</span></span>
<span data-ttu-id="f6b78-109">A **stop-AzureRmDeploymentManagerRollout** parancsmag leállítja a folyamatban lévő kivezetést, és egy olyan objektumot ad eredményül, amely a bevezetés aktuális állapotát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f6b78-109">The **Stop-AzureRmDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="f6b78-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="f6b78-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="f6b78-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f6b78-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="f6b78-112">Fontos tudni, hogy miután leállította a kivezetést, az nem indítható el vagy indítható újra.</span><span class="sxs-lookup"><span data-stu-id="f6b78-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="f6b78-113">Csak új kiépítést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="f6b78-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="f6b78-114">Példák</span><span class="sxs-lookup"><span data-stu-id="f6b78-114">EXAMPLES</span></span>

### <span data-ttu-id="f6b78-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6b78-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="f6b78-116">Ez a parancs leállítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="f6b78-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="f6b78-117">2. példa: a bevezetés leállítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="f6b78-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="f6b78-118">Ez a parancs leállítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="f6b78-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f6b78-119">3. példa: a bevezetés befejezése a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="f6b78-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="f6b78-120">Ez a parancs megszünteti azt a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="f6b78-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="f6b78-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6b78-121">PARAMETERS</span></span>

### <span data-ttu-id="f6b78-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b78-122">-DefaultProfile</span></span>
<span data-ttu-id="f6b78-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6b78-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6b78-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f6b78-124">-Force</span></span>
<span data-ttu-id="f6b78-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6b78-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f6b78-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6b78-126">-Name</span></span>
<span data-ttu-id="f6b78-127">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="f6b78-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="f6b78-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b78-128">-ResourceGroupName</span></span>
<span data-ttu-id="f6b78-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="f6b78-129">The resource group.</span></span>

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

### <span data-ttu-id="f6b78-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6b78-130">-ResourceId</span></span>
<span data-ttu-id="f6b78-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f6b78-131">The resource identifier.</span></span>

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

### <span data-ttu-id="f6b78-132">-Bevezetés</span><span class="sxs-lookup"><span data-stu-id="f6b78-132">-Rollout</span></span>
<span data-ttu-id="f6b78-133">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f6b78-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="f6b78-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6b78-134">-Confirm</span></span>
<span data-ttu-id="f6b78-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6b78-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6b78-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b78-136">-WhatIf</span></span>
<span data-ttu-id="f6b78-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6b78-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6b78-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6b78-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6b78-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b78-139">CommonParameters</span></span>
<span data-ttu-id="f6b78-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6b78-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b78-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b78-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b78-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6b78-142">INPUTS</span></span>

### <span data-ttu-id="f6b78-143">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="f6b78-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="f6b78-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6b78-144">OUTPUTS</span></span>

### <span data-ttu-id="f6b78-145">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="f6b78-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="f6b78-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6b78-146">NOTES</span></span>

## <span data-ttu-id="f6b78-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6b78-147">RELATED LINKS</span></span>

[<span data-ttu-id="f6b78-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="f6b78-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="f6b78-149">Újraindítás – AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="f6b78-149">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="f6b78-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="f6b78-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)