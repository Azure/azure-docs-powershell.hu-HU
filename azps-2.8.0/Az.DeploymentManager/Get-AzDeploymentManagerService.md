---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666672"
---
# <span data-ttu-id="7ffd0-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="7ffd0-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="7ffd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ffd0-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffd0-103">Megkapja a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-103">Gets the service.</span></span>

## <span data-ttu-id="7ffd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ffd0-104">SYNTAX</span></span>

### <span data-ttu-id="7ffd0-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ffd0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ffd0-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="7ffd0-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ffd0-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="7ffd0-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ffd0-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ffd0-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ffd0-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="7ffd0-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ffd0-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ffd0-110">DESCRIPTION</span></span>
<span data-ttu-id="7ffd0-111">A **Get-AzDeploymentManagerService** parancsmag szolgáltatás-topológiában kap egy szolgáltatást, és egy olyan objektumot ad eredményül, amely az adott szolgáltatást jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="7ffd0-112">Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="7ffd0-113">Másik lehetőségként megadhatja a szolgáltatás objektumát vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="7ffd0-114">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="7ffd0-115">Példák</span><span class="sxs-lookup"><span data-stu-id="7ffd0-115">EXAMPLES</span></span>

### <span data-ttu-id="7ffd0-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ffd0-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="7ffd0-117">Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7ffd0-118">2. példa: szolgáltatás kérése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="7ffd0-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="7ffd0-119">Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7ffd0-120">3. példa: szolgáltatás beszerzése a Service objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="7ffd0-121">Ez a parancs olyan szolgáltatást kap, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="7ffd0-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ffd0-122">PARAMETERS</span></span>

### <span data-ttu-id="7ffd0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffd0-123">-DefaultProfile</span></span>
<span data-ttu-id="7ffd0-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ffd0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ffd0-125">-InputObject</span></span>
<span data-ttu-id="7ffd0-126">Service objektum.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-126">Service object.</span></span>

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

### <span data-ttu-id="7ffd0-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ffd0-127">-Name</span></span>
<span data-ttu-id="7ffd0-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffd0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffd0-129">-ResourceGroupName</span></span>
<span data-ttu-id="7ffd0-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-130">The resource group.</span></span>

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

### <span data-ttu-id="7ffd0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ffd0-131">-ResourceId</span></span>
<span data-ttu-id="7ffd0-132">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-132">The resource identifier.</span></span>

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

### <span data-ttu-id="7ffd0-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="7ffd0-133">-ServiceTopologyName</span></span>
<span data-ttu-id="7ffd0-134">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="7ffd0-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="7ffd0-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="7ffd0-136">A szolgáltatás topológiájának objektuma, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="7ffd0-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="7ffd0-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="7ffd0-138">A szolgáltatás topológiája erőforrás-azonosító, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7ffd0-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="7ffd0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffd0-139">CommonParameters</span></span>
<span data-ttu-id="7ffd0-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ffd0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffd0-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffd0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffd0-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ffd0-142">INPUTS</span></span>

### <span data-ttu-id="7ffd0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7ffd0-143">System.String</span></span>

### <span data-ttu-id="7ffd0-144">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="7ffd0-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="7ffd0-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ffd0-145">OUTPUTS</span></span>

### <span data-ttu-id="7ffd0-146">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="7ffd0-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="7ffd0-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ffd0-147">NOTES</span></span>

## <span data-ttu-id="7ffd0-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ffd0-148">RELATED LINKS</span></span>
