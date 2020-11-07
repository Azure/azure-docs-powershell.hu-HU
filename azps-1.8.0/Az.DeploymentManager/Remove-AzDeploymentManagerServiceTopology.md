---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 695a10eb71cc2c4bd1a6bc7eef6cba265d524fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670987"
---
# <span data-ttu-id="fffdc-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="fffdc-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="fffdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fffdc-102">SYNOPSIS</span></span>
<span data-ttu-id="fffdc-103">Törli a szolgáltatási topológiát.</span><span class="sxs-lookup"><span data-stu-id="fffdc-103">Deletes the service topology.</span></span> <span data-ttu-id="fffdc-104">A szolgáltatás topológiájának törlése előtt a szolgáltatás topológiájában létrehozott összes szolgáltatást törölni kell.</span><span class="sxs-lookup"><span data-stu-id="fffdc-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="fffdc-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fffdc-105">SYNTAX</span></span>

### <span data-ttu-id="fffdc-106">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fffdc-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffdc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fffdc-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffdc-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="fffdc-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fffdc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="fffdc-109">DESCRIPTION</span></span>
<span data-ttu-id="fffdc-110">A **Remove-AzDeploymentManagerServiceTopology** parancsmag egy szolgáltatási topológiát töröl.</span><span class="sxs-lookup"><span data-stu-id="fffdc-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="fffdc-111">Adja meg a szolgáltatás topológiáját a nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="fffdc-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="fffdc-112">Másik lehetőségként megadhatja a ServiceTopology objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fffdc-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="fffdc-113">Példák</span><span class="sxs-lookup"><span data-stu-id="fffdc-113">EXAMPLES</span></span>

### <span data-ttu-id="fffdc-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fffdc-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="fffdc-115">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatási topológiát a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fffdc-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fffdc-116">2. példa: a szolgáltatás topológiájának törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="fffdc-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="fffdc-117">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatási topológiát a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fffdc-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fffdc-118">3. példa: a szolgáltatás topológiájának törlése a szolgáltatás topológiája objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="fffdc-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="fffdc-119">Ez a parancs törli azt a szolgáltatási topológiát, amelynek a neve és a ResourceGroup meg kell egyeznie az $serviceTopologyObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="fffdc-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="fffdc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fffdc-120">PARAMETERS</span></span>

### <span data-ttu-id="fffdc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffdc-121">-DefaultProfile</span></span>
<span data-ttu-id="fffdc-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fffdc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fffdc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fffdc-123">-InputObject</span></span>
<span data-ttu-id="fffdc-124">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="fffdc-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="fffdc-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fffdc-125">-Name</span></span>
<span data-ttu-id="fffdc-126">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="fffdc-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="fffdc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fffdc-127">-PassThru</span></span>
<span data-ttu-id="fffdc-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fffdc-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fffdc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffdc-129">-ResourceGroupName</span></span>
<span data-ttu-id="fffdc-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="fffdc-130">The resource group.</span></span>

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

### <span data-ttu-id="fffdc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fffdc-131">-ResourceId</span></span>
<span data-ttu-id="fffdc-132">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fffdc-132">The resource identifier.</span></span>

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

### <span data-ttu-id="fffdc-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fffdc-133">-Confirm</span></span>
<span data-ttu-id="fffdc-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fffdc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fffdc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fffdc-135">-WhatIf</span></span>
<span data-ttu-id="fffdc-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fffdc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fffdc-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fffdc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fffdc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffdc-138">CommonParameters</span></span>
<span data-ttu-id="fffdc-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fffdc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffdc-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fffdc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffdc-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fffdc-141">INPUTS</span></span>

### <span data-ttu-id="fffdc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fffdc-142">System.String</span></span>

### <span data-ttu-id="fffdc-143">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fffdc-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fffdc-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fffdc-144">OUTPUTS</span></span>

### <span data-ttu-id="fffdc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fffdc-145">System.Boolean</span></span>

## <span data-ttu-id="fffdc-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fffdc-146">NOTES</span></span>

## <span data-ttu-id="fffdc-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fffdc-147">RELATED LINKS</span></span>
