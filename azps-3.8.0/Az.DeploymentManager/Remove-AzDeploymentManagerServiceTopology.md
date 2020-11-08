---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014399"
---
# <span data-ttu-id="77189-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="77189-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="77189-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77189-102">SYNOPSIS</span></span>
<span data-ttu-id="77189-103">Törli a szolgáltatási topológiát.</span><span class="sxs-lookup"><span data-stu-id="77189-103">Deletes the service topology.</span></span> <span data-ttu-id="77189-104">A szolgáltatás topológiájának törlése előtt a szolgáltatás topológiájában létrehozott összes szolgáltatást törölni kell.</span><span class="sxs-lookup"><span data-stu-id="77189-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="77189-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77189-105">SYNTAX</span></span>

### <span data-ttu-id="77189-106">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77189-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77189-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="77189-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77189-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="77189-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77189-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="77189-109">DESCRIPTION</span></span>
<span data-ttu-id="77189-110">A **Remove-AzDeploymentManagerServiceTopology** parancsmag egy szolgáltatási topológiát töröl.</span><span class="sxs-lookup"><span data-stu-id="77189-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="77189-111">Adja meg a szolgáltatás topológiáját a nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="77189-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="77189-112">Másik lehetőségként megadhatja a ServiceTopology objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="77189-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="77189-113">Példák</span><span class="sxs-lookup"><span data-stu-id="77189-113">EXAMPLES</span></span>

### <span data-ttu-id="77189-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="77189-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="77189-115">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatási topológiát a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77189-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="77189-116">2. példa: a szolgáltatás topológiájának törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="77189-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="77189-117">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatási topológiát a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77189-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="77189-118">3. példa: a szolgáltatás topológiájának törlése a szolgáltatás topológiája objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="77189-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="77189-119">Ez a parancs törli azt a szolgáltatási topológiát, amelynek a neve és a ResourceGroup meg kell egyeznie az $serviceTopologyObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="77189-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="77189-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77189-120">PARAMETERS</span></span>

### <span data-ttu-id="77189-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77189-121">-DefaultProfile</span></span>
<span data-ttu-id="77189-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77189-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77189-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77189-123">-InputObject</span></span>
<span data-ttu-id="77189-124">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="77189-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="77189-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77189-125">-Name</span></span>
<span data-ttu-id="77189-126">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="77189-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="77189-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77189-127">-PassThru</span></span>
<span data-ttu-id="77189-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="77189-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="77189-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77189-129">-ResourceGroupName</span></span>
<span data-ttu-id="77189-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="77189-130">The resource group.</span></span>

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

### <span data-ttu-id="77189-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77189-131">-ResourceId</span></span>
<span data-ttu-id="77189-132">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="77189-132">The resource identifier.</span></span>

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

### <span data-ttu-id="77189-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77189-133">-Confirm</span></span>
<span data-ttu-id="77189-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77189-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77189-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77189-135">-WhatIf</span></span>
<span data-ttu-id="77189-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77189-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77189-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77189-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77189-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77189-138">CommonParameters</span></span>
<span data-ttu-id="77189-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77189-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77189-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="77189-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77189-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77189-141">INPUTS</span></span>

### <span data-ttu-id="77189-142">System. String</span><span class="sxs-lookup"><span data-stu-id="77189-142">System.String</span></span>

### <span data-ttu-id="77189-143">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="77189-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="77189-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77189-144">OUTPUTS</span></span>

### <span data-ttu-id="77189-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77189-145">System.Boolean</span></span>

## <span data-ttu-id="77189-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77189-146">NOTES</span></span>

## <span data-ttu-id="77189-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77189-147">RELATED LINKS</span></span>
