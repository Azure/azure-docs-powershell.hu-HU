---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490847"
---
# <span data-ttu-id="015f2-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="015f2-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="015f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="015f2-102">SYNOPSIS</span></span>
<span data-ttu-id="015f2-103">Törli a kivezetést.</span><span class="sxs-lookup"><span data-stu-id="015f2-103">Deletes a rollout.</span></span>

## <span data-ttu-id="015f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="015f2-104">SYNTAX</span></span>

### <span data-ttu-id="015f2-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="015f2-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="015f2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="015f2-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="015f2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="015f2-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="015f2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="015f2-108">DESCRIPTION</span></span>
<span data-ttu-id="015f2-109">A **Remove-AzureRmDeploymentManagerRollout** parancsmag kivezetést töröl egy terminál-állapotban.</span><span class="sxs-lookup"><span data-stu-id="015f2-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="015f2-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="015f2-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="015f2-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="015f2-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="015f2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="015f2-112">EXAMPLES</span></span>

### <span data-ttu-id="015f2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="015f2-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="015f2-114">Ez a parancs törli a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="015f2-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="015f2-115">2. példa: az erőforrás-azonosítóval történő bevezetés törlése</span><span class="sxs-lookup"><span data-stu-id="015f2-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="015f2-116">Ez a parancs törli a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="015f2-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="015f2-117">3. példa: a bevezetési objektumon keresztüli bevezetés törlése</span><span class="sxs-lookup"><span data-stu-id="015f2-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="015f2-118">Ez a parancs törli azt a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="015f2-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="015f2-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="015f2-119">PARAMETERS</span></span>

### <span data-ttu-id="015f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015f2-120">-DefaultProfile</span></span>
<span data-ttu-id="015f2-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="015f2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="015f2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="015f2-122">-Force</span></span>
<span data-ttu-id="015f2-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="015f2-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="015f2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="015f2-124">-Name</span></span>
<span data-ttu-id="015f2-125">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="015f2-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="015f2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="015f2-126">-PassThru</span></span>
<span data-ttu-id="015f2-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="015f2-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="015f2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="015f2-128">-ResourceGroupName</span></span>
<span data-ttu-id="015f2-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="015f2-129">The resource group.</span></span>

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

### <span data-ttu-id="015f2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="015f2-130">-ResourceId</span></span>
<span data-ttu-id="015f2-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="015f2-131">The resource identifier.</span></span>

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

### <span data-ttu-id="015f2-132">-Bevezetés</span><span class="sxs-lookup"><span data-stu-id="015f2-132">-Rollout</span></span>
<span data-ttu-id="015f2-133">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="015f2-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="015f2-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="015f2-134">-Confirm</span></span>
<span data-ttu-id="015f2-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="015f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="015f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="015f2-136">-WhatIf</span></span>
<span data-ttu-id="015f2-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="015f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="015f2-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="015f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="015f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015f2-139">CommonParameters</span></span>
<span data-ttu-id="015f2-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="015f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015f2-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="015f2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015f2-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="015f2-142">INPUTS</span></span>

### <span data-ttu-id="015f2-143">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="015f2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="015f2-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="015f2-144">OUTPUTS</span></span>

### <span data-ttu-id="015f2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="015f2-145">System.Boolean</span></span>

## <span data-ttu-id="015f2-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="015f2-146">NOTES</span></span>

## <span data-ttu-id="015f2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="015f2-147">RELATED LINKS</span></span>

[<span data-ttu-id="015f2-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="015f2-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="015f2-149">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="015f2-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="015f2-150">Újraindítás – AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="015f2-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)