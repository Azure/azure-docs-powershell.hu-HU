---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017794"
---
# <span data-ttu-id="f74df-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="f74df-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="f74df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f74df-102">SYNOPSIS</span></span>
<span data-ttu-id="f74df-103">Törli a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="f74df-103">Deletes the service unit.</span></span>

## <span data-ttu-id="f74df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f74df-104">SYNTAX</span></span>

### <span data-ttu-id="f74df-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f74df-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74df-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="f74df-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74df-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="f74df-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74df-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="f74df-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74df-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="f74df-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74df-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f74df-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74df-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="f74df-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74df-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="f74df-112">DESCRIPTION</span></span>
<span data-ttu-id="f74df-113">A **Remove-AzDeploymentManagerServiceUnit** parancsmag egy szolgáltatási egységet töröl a szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f74df-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="f74df-114">Adja meg a szolgáltatás mértékegységét az annak nevével, az azt tartalmazó szolgáltatással, a szolgáltatás topológiájának nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="f74df-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="f74df-115">Másik lehetőségként megadhatja a ServiceUnit objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f74df-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="f74df-116">Példák</span><span class="sxs-lookup"><span data-stu-id="f74df-116">EXAMPLES</span></span>

### <span data-ttu-id="f74df-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f74df-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="f74df-118">Ez a parancs törli a ContosoService1Storage nevű ContosoService1 a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="f74df-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f74df-119">2. példa: a szolgáltatási egység törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="f74df-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="f74df-120">Ez a parancs egy ContosoService1Storage nevű ContosoService1 kap a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="f74df-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f74df-121">3. példa: a szolgáltatási egység törlése a Service Unit objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="f74df-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="f74df-122">Ez a parancs törli azt a szolgáltatási egységet, amelynek a neve, a szolgáltatásnév, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceUnitObject, a szolgáltatásnév, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="f74df-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="f74df-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f74df-123">PARAMETERS</span></span>

### <span data-ttu-id="f74df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74df-124">-DefaultProfile</span></span>
<span data-ttu-id="f74df-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f74df-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f74df-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f74df-126">-InputObject</span></span>
<span data-ttu-id="f74df-127">A Service Unit Resource objektum.</span><span class="sxs-lookup"><span data-stu-id="f74df-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f74df-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f74df-128">-Name</span></span>
<span data-ttu-id="f74df-129">A szolgáltatás egységének neve.</span><span class="sxs-lookup"><span data-stu-id="f74df-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74df-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f74df-130">-PassThru</span></span>
<span data-ttu-id="f74df-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f74df-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f74df-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74df-132">-ResourceGroupName</span></span>
<span data-ttu-id="f74df-133">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="f74df-133">The resource group.</span></span>

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

### <span data-ttu-id="f74df-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f74df-134">-ResourceId</span></span>
<span data-ttu-id="f74df-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f74df-135">The resource identifier.</span></span>

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

### <span data-ttu-id="f74df-136">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="f74df-136">-ServiceName</span></span>
<span data-ttu-id="f74df-137">Annak a szolgáltatásnak a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="f74df-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74df-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="f74df-138">-ServiceObject</span></span>
<span data-ttu-id="f74df-139">Az a szolgáltatási objektum, amelyben a szolgáltatási egységet létre kívánja venni.</span><span class="sxs-lookup"><span data-stu-id="f74df-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74df-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="f74df-140">-ServiceResourceId</span></span>
<span data-ttu-id="f74df-141">Annak a szolgáltatásnak az erőforrás-azonosítóját, amelyben létre kell hozva a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="f74df-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74df-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="f74df-142">-ServiceTopologyName</span></span>
<span data-ttu-id="f74df-143">Annak a szolgáltatási topológiának a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="f74df-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="f74df-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="f74df-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="f74df-145">Annak a szolgáltatásnak a topológiai objektuma, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="f74df-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74df-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="f74df-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="f74df-147">Annak a szolgáltatásnak a topológia-erőforrás-azonosítója, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="f74df-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74df-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f74df-148">-Confirm</span></span>
<span data-ttu-id="f74df-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f74df-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74df-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74df-150">-WhatIf</span></span>
<span data-ttu-id="f74df-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f74df-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f74df-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f74df-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74df-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74df-153">CommonParameters</span></span>
<span data-ttu-id="f74df-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f74df-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74df-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f74df-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74df-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f74df-156">INPUTS</span></span>

### <span data-ttu-id="f74df-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f74df-157">System.String</span></span>

### <span data-ttu-id="f74df-158">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="f74df-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="f74df-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f74df-159">OUTPUTS</span></span>

### <span data-ttu-id="f74df-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f74df-160">System.Boolean</span></span>

## <span data-ttu-id="f74df-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f74df-161">NOTES</span></span>

## <span data-ttu-id="f74df-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f74df-162">RELATED LINKS</span></span>
