---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490928"
---
# <span data-ttu-id="286de-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="286de-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="286de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="286de-102">SYNOPSIS</span></span>
<span data-ttu-id="286de-103">A szolgáltatás topológiájának és erőforrásainak törlése.</span><span class="sxs-lookup"><span data-stu-id="286de-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="286de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="286de-104">SYNTAX</span></span>

### <span data-ttu-id="286de-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="286de-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286de-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="286de-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286de-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="286de-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286de-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="286de-108">DESCRIPTION</span></span>
<span data-ttu-id="286de-109">A **Remove-AzureRmDeploymentManagerServiceTopology** parancsmag egy szolgáltatási topológiát töröl.</span><span class="sxs-lookup"><span data-stu-id="286de-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="286de-110">Adja meg a szolgáltatás topológiáját a nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="286de-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="286de-111">Másik lehetőségként megadhatja a ServiceTopology objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="286de-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="286de-112">Példák</span><span class="sxs-lookup"><span data-stu-id="286de-112">EXAMPLES</span></span>

### <span data-ttu-id="286de-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="286de-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="286de-114">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatási topológiát a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="286de-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="286de-115">2. példa: a szolgáltatás topológiájának törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="286de-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="286de-116">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatási topológiát a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="286de-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="286de-117">3. példa: a szolgáltatás topológiájának törlése a szolgáltatás topológiája objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="286de-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="286de-118">Ez a parancs törli azt a szolgáltatási topológiát, amelynek a neve és a ResourceGroup meg kell egyeznie az $serviceTopologyObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="286de-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="286de-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="286de-119">PARAMETERS</span></span>

### <span data-ttu-id="286de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286de-120">-DefaultProfile</span></span>
<span data-ttu-id="286de-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="286de-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286de-122">-Force</span><span class="sxs-lookup"><span data-stu-id="286de-122">-Force</span></span>
<span data-ttu-id="286de-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="286de-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="286de-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="286de-124">-Name</span></span>
<span data-ttu-id="286de-125">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="286de-125">The name of the service topology.</span></span>

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

### <span data-ttu-id="286de-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="286de-126">-PassThru</span></span>
<span data-ttu-id="286de-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="286de-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="286de-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286de-128">-ResourceGroupName</span></span>
<span data-ttu-id="286de-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="286de-129">The resource group.</span></span>

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

### <span data-ttu-id="286de-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="286de-130">-ResourceId</span></span>
<span data-ttu-id="286de-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="286de-131">The resource identifier.</span></span>

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

### <span data-ttu-id="286de-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="286de-132">-ServiceTopology</span></span>
<span data-ttu-id="286de-133">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="286de-133">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="286de-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="286de-134">-Confirm</span></span>
<span data-ttu-id="286de-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="286de-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286de-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286de-136">-WhatIf</span></span>
<span data-ttu-id="286de-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="286de-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286de-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="286de-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286de-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286de-139">CommonParameters</span></span>
<span data-ttu-id="286de-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="286de-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286de-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286de-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286de-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="286de-142">INPUTS</span></span>

### <span data-ttu-id="286de-143">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="286de-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="286de-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="286de-144">OUTPUTS</span></span>

### <span data-ttu-id="286de-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="286de-145">System.Boolean</span></span>

## <span data-ttu-id="286de-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="286de-146">NOTES</span></span>

## <span data-ttu-id="286de-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="286de-147">RELATED LINKS</span></span>

[<span data-ttu-id="286de-148">Új – AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="286de-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="286de-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="286de-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="286de-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="286de-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)