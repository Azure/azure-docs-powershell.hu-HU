---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014389"
---
# <span data-ttu-id="c1320-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="c1320-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="c1320-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1320-102">SYNOPSIS</span></span>
<span data-ttu-id="c1320-103">Megkapja a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c1320-103">Gets the service unit.</span></span>

## <span data-ttu-id="c1320-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1320-104">SYNTAX</span></span>

### <span data-ttu-id="c1320-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1320-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1320-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="c1320-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1320-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c1320-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1320-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c1320-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1320-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c1320-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1320-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1320-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1320-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1320-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1320-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1320-112">DESCRIPTION</span></span>
<span data-ttu-id="c1320-113">A **Get-AzDeploymentManagerServiceUnit** parancsmag egy szolgáltatási egységet kap a szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="c1320-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="c1320-114">Adja meg a szolgáltatás mértékegységét az annak nevével, az azt tartalmazó szolgáltatással, a szolgáltatás topológiájának nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="c1320-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="c1320-115">Másik lehetőségként megadhatja a ServiceUnit objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c1320-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="c1320-116">Ezt az objektumot helyileg módosíthatja, majd a Set-AzDeploymentManagerServiceUnit parancsmag használatával alkalmazhatja a megfelelő módosításokat.</span><span class="sxs-lookup"><span data-stu-id="c1320-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="c1320-117">Példák</span><span class="sxs-lookup"><span data-stu-id="c1320-117">EXAMPLES</span></span>

### <span data-ttu-id="c1320-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1320-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="c1320-119">Ez a parancs egy ContosoService1Storage nevű ContosoService1 kap a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="c1320-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c1320-120">2. példa: szolgáltatási egység beszerzése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="c1320-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="c1320-121">Ez a parancs egy ContosoService1Storage nevű ContosoService1 kap a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="c1320-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c1320-122">3. példa: szolgáltatás-egység beszerzése a Service Unit objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="c1320-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="c1320-123">Ez a parancs egy olyan szolgáltatási egységet kap, amelynek a neve, a szolgáltatás neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceUnitObject, a szolgáltatásnév, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="c1320-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="c1320-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1320-124">PARAMETERS</span></span>

### <span data-ttu-id="c1320-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1320-125">-DefaultProfile</span></span>
<span data-ttu-id="c1320-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1320-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1320-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1320-127">-InputObject</span></span>
<span data-ttu-id="c1320-128">A Service Unit Resource objektum.</span><span class="sxs-lookup"><span data-stu-id="c1320-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="c1320-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1320-129">-Name</span></span>
<span data-ttu-id="c1320-130">A szolgáltatás egységének neve.</span><span class="sxs-lookup"><span data-stu-id="c1320-130">The name of the service unit.</span></span>

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

### <span data-ttu-id="c1320-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1320-131">-ResourceGroupName</span></span>
<span data-ttu-id="c1320-132">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="c1320-132">The resource group.</span></span>

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

### <span data-ttu-id="c1320-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1320-133">-ResourceId</span></span>
<span data-ttu-id="c1320-134">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c1320-134">The resource identifier.</span></span>

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

### <span data-ttu-id="c1320-135">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="c1320-135">-ServiceName</span></span>
<span data-ttu-id="c1320-136">Annak a szolgáltatásnak a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="c1320-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="c1320-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="c1320-137">-ServiceObject</span></span>
<span data-ttu-id="c1320-138">Az a szolgáltatási objektum, amelyben a szolgáltatási egységet létre kívánja venni.</span><span class="sxs-lookup"><span data-stu-id="c1320-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c1320-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c1320-139">-ServiceResourceId</span></span>
<span data-ttu-id="c1320-140">Annak a szolgáltatásnak az erőforrás-azonosítóját, amelyben létre kell hozva a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c1320-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c1320-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="c1320-141">-ServiceTopologyName</span></span>
<span data-ttu-id="c1320-142">Annak a szolgáltatási topológiának a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="c1320-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="c1320-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c1320-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="c1320-144">Annak a szolgáltatásnak a topológiai objektuma, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c1320-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c1320-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c1320-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="c1320-146">Annak a szolgáltatásnak a topológia-erőforrás-azonosítója, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c1320-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c1320-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1320-147">CommonParameters</span></span>
<span data-ttu-id="c1320-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1320-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1320-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1320-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1320-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1320-150">INPUTS</span></span>

### <span data-ttu-id="c1320-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c1320-151">System.String</span></span>

### <span data-ttu-id="c1320-152">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c1320-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c1320-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1320-153">OUTPUTS</span></span>

### <span data-ttu-id="c1320-154">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c1320-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c1320-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1320-155">NOTES</span></span>

## <span data-ttu-id="c1320-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1320-156">RELATED LINKS</span></span>
