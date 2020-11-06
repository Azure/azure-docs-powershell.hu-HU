---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491623"
---
# <span data-ttu-id="6df0d-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="6df0d-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="6df0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6df0d-102">SYNOPSIS</span></span>
<span data-ttu-id="6df0d-103">Egy szolgáltatás szolgáltatási egységét törli a szolgáltatás topológiájában.</span><span class="sxs-lookup"><span data-stu-id="6df0d-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="6df0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6df0d-104">SYNTAX</span></span>

### <span data-ttu-id="6df0d-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6df0d-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df0d-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="6df0d-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df0d-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="6df0d-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df0d-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="6df0d-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df0d-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="6df0d-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df0d-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6df0d-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df0d-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="6df0d-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6df0d-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="6df0d-112">DESCRIPTION</span></span>
<span data-ttu-id="6df0d-113">A **Remove-AzureRmDeploymentManagerServiceUnit** parancsmag egy szolgáltatási egységet töröl a szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6df0d-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="6df0d-114">Adja meg a szolgáltatás mértékegységét az annak nevével, az azt tartalmazó szolgáltatással, a szolgáltatás topológiájának nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="6df0d-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="6df0d-115">Másik lehetőségként megadhatja a ServiceUnit objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6df0d-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="6df0d-116">Példák</span><span class="sxs-lookup"><span data-stu-id="6df0d-116">EXAMPLES</span></span>

### <span data-ttu-id="6df0d-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6df0d-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="6df0d-118">Ez a parancs törli a ContosoService1Storage nevű ContosoService1 a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="6df0d-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6df0d-119">2. példa: a szolgáltatási egység törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="6df0d-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="6df0d-120">Ez a parancs egy ContosoService1Storage nevű ContosoService1 kap a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="6df0d-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6df0d-121">3. példa: a szolgáltatási egység törlése a Service Unit objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="6df0d-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="6df0d-122">Ez a parancs törli azt a szolgáltatási egységet, amelynek a neve, a szolgáltatásnév, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceUnitObject, a szolgáltatásnév, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="6df0d-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="6df0d-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6df0d-123">PARAMETERS</span></span>

### <span data-ttu-id="6df0d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df0d-124">-DefaultProfile</span></span>
<span data-ttu-id="6df0d-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6df0d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df0d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6df0d-126">-Force</span></span>
<span data-ttu-id="6df0d-127">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6df0d-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6df0d-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6df0d-128">-Name</span></span>
<span data-ttu-id="6df0d-129">A törlendő szolgáltatási egység neve.</span><span class="sxs-lookup"><span data-stu-id="6df0d-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df0d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6df0d-130">-PassThru</span></span>
<span data-ttu-id="6df0d-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6df0d-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6df0d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df0d-132">-ResourceGroupName</span></span>
<span data-ttu-id="6df0d-133">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="6df0d-133">The resource group.</span></span>

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

### <span data-ttu-id="6df0d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6df0d-134">-ResourceId</span></span>
<span data-ttu-id="6df0d-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6df0d-135">The resource identifier.</span></span>

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

### <span data-ttu-id="6df0d-136">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="6df0d-136">-Service</span></span>
<span data-ttu-id="6df0d-137">Az a szolgáltatási objektum, amelyben a szolgáltatási egységet létre kívánja venni.</span><span class="sxs-lookup"><span data-stu-id="6df0d-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="6df0d-138">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="6df0d-138">-ServiceName</span></span>
<span data-ttu-id="6df0d-139">Annak a szolgáltatásnak a neve, amelyhez a szolgáltatási egység tartozik.</span><span class="sxs-lookup"><span data-stu-id="6df0d-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df0d-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="6df0d-140">-ServiceResourceId</span></span>
<span data-ttu-id="6df0d-141">Annak a szolgáltatásnak az erőforrás-azonosítóját, amelyben létre kell hozva a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="6df0d-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="6df0d-142">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6df0d-142">-ServiceTopology</span></span>
<span data-ttu-id="6df0d-143">Annak a szolgáltatásnak a topológiai objektuma, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="6df0d-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="6df0d-144">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="6df0d-144">-ServiceTopologyName</span></span>
<span data-ttu-id="6df0d-145">Annak a szolgáltatási hálózatnak a neve, amelyhez a szolgáltatási egység tartozik.</span><span class="sxs-lookup"><span data-stu-id="6df0d-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="6df0d-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="6df0d-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="6df0d-147">Annak a szolgáltatásnak a topológia-erőforrás-azonosítója, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="6df0d-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="6df0d-148">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="6df0d-148">-ServiceUnit</span></span>
<span data-ttu-id="6df0d-149">Az eltávolítandó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6df0d-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="6df0d-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6df0d-150">-Confirm</span></span>
<span data-ttu-id="6df0d-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6df0d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df0d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df0d-152">-WhatIf</span></span>
<span data-ttu-id="6df0d-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6df0d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df0d-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6df0d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df0d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df0d-155">CommonParameters</span></span>
<span data-ttu-id="6df0d-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6df0d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df0d-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df0d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df0d-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df0d-158">INPUTS</span></span>

### <span data-ttu-id="6df0d-159">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="6df0d-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="6df0d-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df0d-160">OUTPUTS</span></span>

### <span data-ttu-id="6df0d-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6df0d-161">System.Boolean</span></span>

## <span data-ttu-id="6df0d-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6df0d-162">NOTES</span></span>

## <span data-ttu-id="6df0d-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6df0d-163">RELATED LINKS</span></span>

[<span data-ttu-id="6df0d-164">Új – AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="6df0d-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="6df0d-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="6df0d-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="6df0d-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="6df0d-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)