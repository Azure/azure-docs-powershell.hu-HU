---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014360"
---
# <span data-ttu-id="c80a1-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c80a1-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="c80a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c80a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c80a1-103">Leállítja a kiépítést.</span><span class="sxs-lookup"><span data-stu-id="c80a1-103">Stops the rollout.</span></span>

## <span data-ttu-id="c80a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c80a1-104">SYNTAX</span></span>

### <span data-ttu-id="c80a1-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c80a1-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c80a1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c80a1-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c80a1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c80a1-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c80a1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c80a1-108">DESCRIPTION</span></span>
<span data-ttu-id="c80a1-109">A **stop-AzDeploymentManagerRollout** parancsmag leállítja a folyamatban lévő kivezetést, és egy olyan objektumot ad eredményül, amely a bevezetés aktuális állapotát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c80a1-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="c80a1-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="c80a1-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="c80a1-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c80a1-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="c80a1-112">Fontos tudni, hogy miután leállította a kivezetést, az nem indítható el vagy indítható újra.</span><span class="sxs-lookup"><span data-stu-id="c80a1-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="c80a1-113">Csak új kiépítést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="c80a1-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="c80a1-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c80a1-114">EXAMPLES</span></span>

### <span data-ttu-id="c80a1-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c80a1-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="c80a1-116">Ez a parancs leállítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="c80a1-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="c80a1-117">2. példa: a bevezetés leállítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="c80a1-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="c80a1-118">Ez a parancs leállítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="c80a1-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c80a1-119">3. példa: a bevezetés befejezése a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="c80a1-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="c80a1-120">Ez a parancs megszünteti azt a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="c80a1-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="c80a1-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c80a1-121">PARAMETERS</span></span>

### <span data-ttu-id="c80a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80a1-122">-DefaultProfile</span></span>
<span data-ttu-id="c80a1-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c80a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c80a1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c80a1-124">-Force</span></span>
<span data-ttu-id="c80a1-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c80a1-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c80a1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c80a1-126">-InputObject</span></span>
<span data-ttu-id="c80a1-127">A kiépítést el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="c80a1-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="c80a1-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c80a1-128">-Name</span></span>
<span data-ttu-id="c80a1-129">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="c80a1-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="c80a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c80a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="c80a1-131">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="c80a1-131">The resource group.</span></span>

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

### <span data-ttu-id="c80a1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c80a1-132">-ResourceId</span></span>
<span data-ttu-id="c80a1-133">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c80a1-133">The resource identifier.</span></span>

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

### <span data-ttu-id="c80a1-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c80a1-134">-Confirm</span></span>
<span data-ttu-id="c80a1-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c80a1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c80a1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c80a1-136">-WhatIf</span></span>
<span data-ttu-id="c80a1-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c80a1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c80a1-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c80a1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c80a1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80a1-139">CommonParameters</span></span>
<span data-ttu-id="c80a1-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c80a1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80a1-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c80a1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80a1-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c80a1-142">INPUTS</span></span>

### <span data-ttu-id="c80a1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c80a1-143">System.String</span></span>

### <span data-ttu-id="c80a1-144">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="c80a1-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c80a1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c80a1-145">OUTPUTS</span></span>

### <span data-ttu-id="c80a1-146">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="c80a1-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c80a1-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c80a1-147">NOTES</span></span>

## <span data-ttu-id="c80a1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c80a1-148">RELATED LINKS</span></span>
