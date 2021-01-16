---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387349"
---
# <span data-ttu-id="78d5a-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="78d5a-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="78d5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="78d5a-103">A szolgáltatásegység törlése.</span><span class="sxs-lookup"><span data-stu-id="78d5a-103">Deletes the service unit.</span></span>

## <span data-ttu-id="78d5a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78d5a-104">SYNTAX</span></span>

### <span data-ttu-id="78d5a-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78d5a-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d5a-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="78d5a-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d5a-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="78d5a-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d5a-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="78d5a-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d5a-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="78d5a-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d5a-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d5a-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d5a-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="78d5a-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d5a-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78d5a-112">DESCRIPTION</span></span>
<span data-ttu-id="78d5a-113">A **Remove-AzDeploymentManagerServiceUnit** parancsmag töröl egy szolgáltatási egységet egy szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="78d5a-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="78d5a-114">Adja meg a szolgáltatási egységet a neve, az a szolgáltatás, amely alatt definiálta, a szolgáltatás topológiája és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="78d5a-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="78d5a-115">Másik módon meg is használhatja a ServiceUnit objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="78d5a-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="78d5a-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78d5a-116">EXAMPLES</span></span>

### <span data-ttu-id="78d5a-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="78d5a-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="78d5a-118">Ez a parancs törli a ContosoService1Storage nevű szolgáltatási egységet a ContosoService1 szolgáltatásban a ContosoServiceTopology nevű szolgáltatás topológiában a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="78d5a-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="78d5a-119">2. példa: Szolgáltatásegység törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="78d5a-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="78d5a-120">Ez a parancs egy ContosoService1Storage nevű szolgáltatási egységet kap a ContosoService1 szolgáltatás egy ContosoServiceTopology nevű szolgáltatás topológiája alatt a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="78d5a-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="78d5a-121">3. példa: Szervizegység törlése a szolgáltatásegység-objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="78d5a-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="78d5a-122">Ez a parancs törli azokat a szolgáltatásiegységeket, amelyeknek a neve, a szolgáltatás neve, a szolgáltatás topológiája és az Erőforráscsoport neve megegyezik a $serviceUnitObject, ServiceName, ServiceTopologyName és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="78d5a-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="78d5a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78d5a-123">PARAMETERS</span></span>

### <span data-ttu-id="78d5a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d5a-124">-DefaultProfile</span></span>
<span data-ttu-id="78d5a-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78d5a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d5a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78d5a-126">-InputObject</span></span>
<span data-ttu-id="78d5a-127">Service unit resource object.</span><span class="sxs-lookup"><span data-stu-id="78d5a-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="78d5a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="78d5a-128">-Name</span></span>
<span data-ttu-id="78d5a-129">A szolgáltatási egység neve.</span><span class="sxs-lookup"><span data-stu-id="78d5a-129">The name of the service unit.</span></span>

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

### <span data-ttu-id="78d5a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78d5a-130">-PassThru</span></span>
<span data-ttu-id="78d5a-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="78d5a-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="78d5a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d5a-132">-ResourceGroupName</span></span>
<span data-ttu-id="78d5a-133">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="78d5a-133">The resource group.</span></span>

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

### <span data-ttu-id="78d5a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d5a-134">-ResourceId</span></span>
<span data-ttu-id="78d5a-135">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="78d5a-135">The resource identifier.</span></span>

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

### <span data-ttu-id="78d5a-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="78d5a-136">-ServiceName</span></span>
<span data-ttu-id="78d5a-137">Annak a szolgáltatásnak a neve, amelyben a szolgáltatási egység található.</span><span class="sxs-lookup"><span data-stu-id="78d5a-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="78d5a-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="78d5a-138">-ServiceObject</span></span>
<span data-ttu-id="78d5a-139">Az a szolgáltatásobjektum, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="78d5a-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="78d5a-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="78d5a-140">-ServiceResourceId</span></span>
<span data-ttu-id="78d5a-141">Az a szolgáltatáserőforrás-azonosító, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="78d5a-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="78d5a-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="78d5a-142">-ServiceTopologyName</span></span>
<span data-ttu-id="78d5a-143">Annak a szolgáltatás-topológiának a neve, amely részét képezi a szolgáltatási egységnek.</span><span class="sxs-lookup"><span data-stu-id="78d5a-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="78d5a-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="78d5a-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="78d5a-145">Az a szolgáltatás topológia objektum, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="78d5a-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="78d5a-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="78d5a-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="78d5a-147">Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="78d5a-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="78d5a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78d5a-148">-Confirm</span></span>
<span data-ttu-id="78d5a-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="78d5a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d5a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d5a-150">-WhatIf</span></span>
<span data-ttu-id="78d5a-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="78d5a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d5a-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78d5a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d5a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d5a-153">CommonParameters</span></span>
<span data-ttu-id="78d5a-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d5a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d5a-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78d5a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d5a-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78d5a-156">INPUTS</span></span>

### <span data-ttu-id="78d5a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="78d5a-157">System.String</span></span>

### <span data-ttu-id="78d5a-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="78d5a-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="78d5a-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78d5a-159">OUTPUTS</span></span>

### <span data-ttu-id="78d5a-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78d5a-160">System.Boolean</span></span>

## <span data-ttu-id="78d5a-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78d5a-161">NOTES</span></span>

## <span data-ttu-id="78d5a-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78d5a-162">RELATED LINKS</span></span>
