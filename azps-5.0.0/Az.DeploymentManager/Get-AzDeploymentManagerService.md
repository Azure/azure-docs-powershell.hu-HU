---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297245"
---
# <span data-ttu-id="d56cc-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d56cc-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="d56cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d56cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d56cc-103">Megkapja a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d56cc-103">Gets the service.</span></span>

## <span data-ttu-id="d56cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d56cc-104">SYNTAX</span></span>

### <span data-ttu-id="d56cc-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d56cc-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d56cc-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d56cc-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d56cc-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d56cc-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d56cc-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d56cc-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d56cc-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="d56cc-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d56cc-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="d56cc-110">DESCRIPTION</span></span>
<span data-ttu-id="d56cc-111">A **Get-AzDeploymentManagerService** parancsmag szolgáltatás-topológiában kap egy szolgáltatást, és egy olyan objektumot ad eredményül, amely az adott szolgáltatást jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d56cc-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="d56cc-112">Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="d56cc-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="d56cc-113">Másik lehetőségként megadhatja a szolgáltatás objektumát vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d56cc-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="d56cc-114">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="d56cc-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="d56cc-115">Példák</span><span class="sxs-lookup"><span data-stu-id="d56cc-115">EXAMPLES</span></span>

### <span data-ttu-id="d56cc-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d56cc-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="d56cc-117">Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.</span><span class="sxs-lookup"><span data-stu-id="d56cc-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d56cc-118">2. példa: szolgáltatás kérése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="d56cc-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="d56cc-119">Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.</span><span class="sxs-lookup"><span data-stu-id="d56cc-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d56cc-120">3. példa: szolgáltatás beszerzése a Service objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="d56cc-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="d56cc-121">Ez a parancs olyan szolgáltatást kap, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="d56cc-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="d56cc-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d56cc-122">PARAMETERS</span></span>

### <span data-ttu-id="d56cc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56cc-123">-DefaultProfile</span></span>
<span data-ttu-id="d56cc-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d56cc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d56cc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d56cc-125">-InputObject</span></span>
<span data-ttu-id="d56cc-126">Service objektum.</span><span class="sxs-lookup"><span data-stu-id="d56cc-126">Service object.</span></span>

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

### <span data-ttu-id="d56cc-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d56cc-127">-Name</span></span>
<span data-ttu-id="d56cc-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d56cc-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56cc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56cc-129">-ResourceGroupName</span></span>
<span data-ttu-id="d56cc-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="d56cc-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56cc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d56cc-131">-ResourceId</span></span>
<span data-ttu-id="d56cc-132">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d56cc-132">The resource identifier.</span></span>

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

### <span data-ttu-id="d56cc-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="d56cc-133">-ServiceTopologyName</span></span>
<span data-ttu-id="d56cc-134">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="d56cc-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="d56cc-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d56cc-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="d56cc-136">A szolgáltatás topológiájának objektuma, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="d56cc-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56cc-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d56cc-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="d56cc-138">A szolgáltatás topológiája erőforrás-azonosító, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="d56cc-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56cc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56cc-139">CommonParameters</span></span>
<span data-ttu-id="d56cc-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d56cc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56cc-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d56cc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56cc-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d56cc-142">INPUTS</span></span>

### <span data-ttu-id="d56cc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d56cc-143">System.String</span></span>

### <span data-ttu-id="d56cc-144">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d56cc-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d56cc-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d56cc-145">OUTPUTS</span></span>

### <span data-ttu-id="d56cc-146">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d56cc-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d56cc-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d56cc-147">NOTES</span></span>

## <span data-ttu-id="d56cc-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d56cc-148">RELATED LINKS</span></span>
