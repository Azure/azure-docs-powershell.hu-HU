---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490844"
---
# <span data-ttu-id="bd836-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="bd836-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="bd836-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd836-102">SYNOPSIS</span></span>
<span data-ttu-id="bd836-103">Szolgáltatást töröl egy szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="bd836-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="bd836-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd836-104">SYNTAX</span></span>

### <span data-ttu-id="bd836-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd836-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd836-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="bd836-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd836-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="bd836-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd836-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd836-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd836-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="bd836-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd836-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd836-110">DESCRIPTION</span></span>
<span data-ttu-id="bd836-111">A **Remove-AzureRmDeploymentManagerService** parancsmag a szolgáltatás topológiája alatt töröl egy szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bd836-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="bd836-112">Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="bd836-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="bd836-113">Másik lehetőségként megadhatja a szolgáltatás objektumát vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="bd836-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="bd836-114">Példák</span><span class="sxs-lookup"><span data-stu-id="bd836-114">EXAMPLES</span></span>

### <span data-ttu-id="bd836-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd836-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="bd836-116">Ez a parancs törli a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="bd836-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="bd836-117">2. példa: szolgáltatás törlése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="bd836-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="bd836-118">Ez a parancs törli a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="bd836-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="bd836-119">Példa 3: szolgáltatás törlése a Service objektummal.</span><span class="sxs-lookup"><span data-stu-id="bd836-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="bd836-120">Ez a parancs törli azt a szolgáltatást, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="bd836-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="bd836-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd836-121">PARAMETERS</span></span>

### <span data-ttu-id="bd836-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd836-122">-DefaultProfile</span></span>
<span data-ttu-id="bd836-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd836-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd836-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bd836-124">-Force</span></span>
<span data-ttu-id="bd836-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd836-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bd836-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd836-126">-Name</span></span>
<span data-ttu-id="bd836-127">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="bd836-127">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd836-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd836-128">-PassThru</span></span>
<span data-ttu-id="bd836-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bd836-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bd836-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd836-130">-ResourceGroupName</span></span>
<span data-ttu-id="bd836-131">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="bd836-131">The resource group.</span></span>

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

### <span data-ttu-id="bd836-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd836-132">-ResourceId</span></span>
<span data-ttu-id="bd836-133">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bd836-133">The resource identifier.</span></span>

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

### <span data-ttu-id="bd836-134">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="bd836-134">-Service</span></span>
<span data-ttu-id="bd836-135">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="bd836-135">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd836-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="bd836-136">-ServiceTopology</span></span>
<span data-ttu-id="bd836-137">A szolgáltatás topológiájának objektuma, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="bd836-137">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd836-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="bd836-138">-ServiceTopologyName</span></span>
<span data-ttu-id="bd836-139">Annak a szolgáltatási topológiának a neve, amelyhez a szolgáltatás tartozik.</span><span class="sxs-lookup"><span data-stu-id="bd836-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="bd836-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="bd836-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="bd836-141">A szolgáltatás topológiája erőforrás-azonosító, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="bd836-141">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd836-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd836-142">-Confirm</span></span>
<span data-ttu-id="bd836-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd836-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd836-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd836-144">-WhatIf</span></span>
<span data-ttu-id="bd836-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd836-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd836-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd836-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd836-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd836-147">CommonParameters</span></span>
<span data-ttu-id="bd836-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd836-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd836-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd836-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd836-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd836-150">INPUTS</span></span>

### <span data-ttu-id="bd836-151">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="bd836-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="bd836-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd836-152">OUTPUTS</span></span>

### <span data-ttu-id="bd836-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd836-153">System.Boolean</span></span>

## <span data-ttu-id="bd836-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd836-154">NOTES</span></span>

## <span data-ttu-id="bd836-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd836-155">RELATED LINKS</span></span>

[<span data-ttu-id="bd836-156">Új – AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="bd836-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="bd836-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="bd836-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="bd836-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="bd836-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)