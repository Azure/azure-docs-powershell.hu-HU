---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490932"
---
# <span data-ttu-id="ec2c6-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ec2c6-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="ec2c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2c6-103">Lépés törlése</span><span class="sxs-lookup"><span data-stu-id="ec2c6-103">Deletes a step.</span></span>

## <span data-ttu-id="ec2c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec2c6-104">SYNTAX</span></span>

### <span data-ttu-id="ec2c6-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec2c6-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec2c6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec2c6-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec2c6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ec2c6-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec2c6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec2c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ec2c6-109">A **Remove-AzureRmDeploymentManagerStep** parancsmag egy lépést töröl.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="ec2c6-110">Adja meg a kívánt lépést a nevével és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="ec2c6-111">Másik lehetőségként a Step objektum vagy a ResourceId is megadható.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="ec2c6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ec2c6-112">EXAMPLES</span></span>
### <span data-ttu-id="ec2c6-113">1. példa: lépés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ec2c6-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="ec2c6-114">Ez a parancs törli a ContosoService1WaitStep nevű lépést a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ec2c6-115">2. példa: lépés eltávolítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="ec2c6-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="ec2c6-116">Ez a parancs törli a ContosoService1WaitStep nevű lépést a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ec2c6-117">3. példa: lépés eltávolítása New-AzureRmDeploymentManagerStep által visszaadott objektum használatával</span><span class="sxs-lookup"><span data-stu-id="ec2c6-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="ec2c6-118">Ez a parancs törli azt a lépést, amelynek a neve és a ResourceGroup meg kell egyeznie az $stepObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="ec2c6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec2c6-119">PARAMETERS</span></span>

### <span data-ttu-id="ec2c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2c6-120">-DefaultProfile</span></span>
<span data-ttu-id="ec2c6-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec2c6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ec2c6-122">-Force</span></span>
<span data-ttu-id="ec2c6-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ec2c6-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec2c6-124">-Name</span></span>
<span data-ttu-id="ec2c6-125">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-125">The name of the step.</span></span>

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

### <span data-ttu-id="ec2c6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec2c6-126">-PassThru</span></span>
<span data-ttu-id="ec2c6-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ec2c6-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ec2c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec2c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec2c6-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-129">The resource group.</span></span>

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

### <span data-ttu-id="ec2c6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec2c6-130">-ResourceId</span></span>
<span data-ttu-id="ec2c6-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-131">The resource identifier.</span></span>

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

### <span data-ttu-id="ec2c6-132">Lépés</span><span class="sxs-lookup"><span data-stu-id="ec2c6-132">-Step</span></span>
<span data-ttu-id="ec2c6-133">Az eltávolítandó lépés.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-133">The step to be removed.</span></span>

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

### <span data-ttu-id="ec2c6-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec2c6-134">-Confirm</span></span>
<span data-ttu-id="ec2c6-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec2c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec2c6-136">-WhatIf</span></span>
<span data-ttu-id="ec2c6-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec2c6-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec2c6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec2c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2c6-139">CommonParameters</span></span>
<span data-ttu-id="ec2c6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec2c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ec2c6-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec2c6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2c6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec2c6-142">INPUTS</span></span>

### <span data-ttu-id="ec2c6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ec2c6-143">System.String</span></span>

### <span data-ttu-id="ec2c6-144">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ec2c6-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ec2c6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec2c6-145">OUTPUTS</span></span>

### <span data-ttu-id="ec2c6-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec2c6-146">System.Boolean</span></span>

## <span data-ttu-id="ec2c6-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec2c6-147">NOTES</span></span>

## <span data-ttu-id="ec2c6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec2c6-148">RELATED LINKS</span></span>
