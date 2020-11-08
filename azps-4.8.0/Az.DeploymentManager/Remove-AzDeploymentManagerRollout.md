---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017797"
---
# <span data-ttu-id="0fdbb-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="0fdbb-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="0fdbb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fdbb-102">SYNOPSIS</span></span>
<span data-ttu-id="0fdbb-103">Törli a kiépítést.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-103">Deletes the rollout.</span></span>

## <span data-ttu-id="0fdbb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fdbb-104">SYNTAX</span></span>

### <span data-ttu-id="0fdbb-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fdbb-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fdbb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fdbb-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fdbb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0fdbb-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fdbb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fdbb-108">DESCRIPTION</span></span>
<span data-ttu-id="0fdbb-109">A **Remove-AzDeploymentManagerRollout** parancsmag kivezetést töröl egy terminál-állapotban.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="0fdbb-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="0fdbb-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="0fdbb-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0fdbb-112">EXAMPLES</span></span>

### <span data-ttu-id="0fdbb-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fdbb-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="0fdbb-114">Ez a parancs törli a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0fdbb-115">2. példa: az erőforrás-azonosítóval történő bevezetés törlése</span><span class="sxs-lookup"><span data-stu-id="0fdbb-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="0fdbb-116">Ez a parancs törli a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0fdbb-117">3. példa: a bevezetési objektumon keresztüli bevezetés törlése</span><span class="sxs-lookup"><span data-stu-id="0fdbb-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="0fdbb-118">Ez a parancs törli azt a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="0fdbb-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fdbb-119">PARAMETERS</span></span>

### <span data-ttu-id="0fdbb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fdbb-120">-DefaultProfile</span></span>
<span data-ttu-id="0fdbb-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fdbb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fdbb-122">-InputObject</span></span>
<span data-ttu-id="0fdbb-123">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="0fdbb-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fdbb-124">-Name</span></span>
<span data-ttu-id="0fdbb-125">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="0fdbb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fdbb-126">-PassThru</span></span>
<span data-ttu-id="0fdbb-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0fdbb-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0fdbb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fdbb-128">-ResourceGroupName</span></span>
<span data-ttu-id="0fdbb-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-129">The resource group.</span></span>

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

### <span data-ttu-id="0fdbb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fdbb-130">-ResourceId</span></span>
<span data-ttu-id="0fdbb-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-131">The resource identifier.</span></span>

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

### <span data-ttu-id="0fdbb-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fdbb-132">-Confirm</span></span>
<span data-ttu-id="0fdbb-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fdbb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fdbb-134">-WhatIf</span></span>
<span data-ttu-id="0fdbb-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fdbb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fdbb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fdbb-137">CommonParameters</span></span>
<span data-ttu-id="0fdbb-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fdbb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fdbb-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fdbb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fdbb-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fdbb-140">INPUTS</span></span>

### <span data-ttu-id="0fdbb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0fdbb-141">System.String</span></span>

### <span data-ttu-id="0fdbb-142">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="0fdbb-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="0fdbb-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fdbb-143">OUTPUTS</span></span>

### <span data-ttu-id="0fdbb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fdbb-144">System.Boolean</span></span>

## <span data-ttu-id="0fdbb-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fdbb-145">NOTES</span></span>

## <span data-ttu-id="0fdbb-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fdbb-146">RELATED LINKS</span></span>
