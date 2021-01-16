---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387434"
---
# <span data-ttu-id="32063-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="32063-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="32063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32063-102">SYNOPSIS</span></span>
<span data-ttu-id="32063-103">A szervizegységet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="32063-103">Gets the service unit.</span></span>

## <span data-ttu-id="32063-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32063-104">SYNTAX</span></span>

### <span data-ttu-id="32063-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32063-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32063-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="32063-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32063-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="32063-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32063-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="32063-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32063-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="32063-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32063-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="32063-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32063-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="32063-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32063-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32063-112">DESCRIPTION</span></span>
<span data-ttu-id="32063-113">A **Get-AzDeploymentManagerServiceUnit** parancsmag szolgáltatásegységet kap egy szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="32063-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="32063-114">Adja meg a szolgáltatási egységet a neve, az a szolgáltatás, amely alatt definiálta, a szolgáltatás topológiája és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="32063-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="32063-115">Másik módon meg is használhatja a ServiceUnit objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="32063-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="32063-116">Ezt az objektumot helyben módosíthatja, majd a helyi parancsmag használatával módosíthatja a szolgáltatási Set-AzDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="32063-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="32063-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32063-117">EXAMPLES</span></span>

### <span data-ttu-id="32063-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="32063-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="32063-119">Ez a parancs egy ContosoService1Storage nevű szolgáltatási egységet kap a ContosoService1 szolgáltatás egy ContosoServiceTopology nevű szolgáltatás topológiája alatt a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="32063-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="32063-120">2. példa: Szolgáltatási egység lekérte az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="32063-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="32063-121">Ez a parancs egy ContosoService1Storage nevű szolgáltatási egységet kap a ContosoService1 szolgáltatás egy ContosoServiceTopology nevű szolgáltatás topológiája alatt a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="32063-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="32063-122">3. példa: Szervizegység behozása a szolgáltatásegység-objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="32063-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="32063-123">Ez a parancs egy olyan szolgáltatásegységet kap, amelynek neve, szolgáltatásneve, szolgáltatás topológiája neve és Erőforráscsoportja megegyezik a $serviceUnitObject, ServiceName, ServiceTopologyName és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="32063-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="32063-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32063-124">PARAMETERS</span></span>

### <span data-ttu-id="32063-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32063-125">-DefaultProfile</span></span>
<span data-ttu-id="32063-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32063-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32063-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32063-127">-InputObject</span></span>
<span data-ttu-id="32063-128">Service unit resource object.</span><span class="sxs-lookup"><span data-stu-id="32063-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="32063-129">-Name</span><span class="sxs-lookup"><span data-stu-id="32063-129">-Name</span></span>
<span data-ttu-id="32063-130">A szolgáltatási egység neve.</span><span class="sxs-lookup"><span data-stu-id="32063-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32063-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32063-131">-ResourceGroupName</span></span>
<span data-ttu-id="32063-132">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="32063-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32063-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32063-133">-ResourceId</span></span>
<span data-ttu-id="32063-134">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="32063-134">The resource identifier.</span></span>

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

### <span data-ttu-id="32063-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="32063-135">-ServiceName</span></span>
<span data-ttu-id="32063-136">Annak a szolgáltatásnak a neve, amelyben a szolgáltatási egység található.</span><span class="sxs-lookup"><span data-stu-id="32063-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="32063-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="32063-137">-ServiceObject</span></span>
<span data-ttu-id="32063-138">Az a szolgáltatásobjektum, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="32063-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="32063-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="32063-139">-ServiceResourceId</span></span>
<span data-ttu-id="32063-140">Az a szolgáltatáserőforrás-azonosító, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="32063-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="32063-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="32063-141">-ServiceTopologyName</span></span>
<span data-ttu-id="32063-142">Annak a szolgáltatás-topológiának a neve, amely részét képezi a szolgáltatási egységnek.</span><span class="sxs-lookup"><span data-stu-id="32063-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="32063-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="32063-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="32063-144">Az a szolgáltatás topológia objektum, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="32063-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="32063-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="32063-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="32063-146">Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="32063-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="32063-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32063-147">CommonParameters</span></span>
<span data-ttu-id="32063-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32063-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32063-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32063-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32063-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32063-150">INPUTS</span></span>

### <span data-ttu-id="32063-151">System.String</span><span class="sxs-lookup"><span data-stu-id="32063-151">System.String</span></span>

### <span data-ttu-id="32063-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="32063-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="32063-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32063-153">OUTPUTS</span></span>

### <span data-ttu-id="32063-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="32063-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="32063-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32063-155">NOTES</span></span>

## <span data-ttu-id="32063-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32063-156">RELATED LINKS</span></span>
