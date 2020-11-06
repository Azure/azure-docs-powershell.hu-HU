---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
content_git_url: ''
ms.openlocfilehash: 655cfeeae35d1b48bbfe2149fd4262dffe72ae09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491764"
---
# <span data-ttu-id="db38f-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="db38f-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="db38f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db38f-102">SYNOPSIS</span></span>
<span data-ttu-id="db38f-103">Szolgáltatási topológiában kapja meg a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="db38f-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="db38f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db38f-104">SYNTAX</span></span>

### <span data-ttu-id="db38f-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db38f-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db38f-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="db38f-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db38f-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="db38f-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db38f-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="db38f-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db38f-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="db38f-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db38f-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="db38f-110">DESCRIPTION</span></span>
<span data-ttu-id="db38f-111">A **Get-AzureRmDeploymentManagerService** parancsmag szolgáltatás-topológiában kap egy szolgáltatást, és egy olyan objektumot ad eredményül, amely az adott szolgáltatást jelképezi.</span><span class="sxs-lookup"><span data-stu-id="db38f-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="db38f-112">Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="db38f-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="db38f-113">Másik lehetőségként megadhatja a szolgáltatás objektumát vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="db38f-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="db38f-114">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="db38f-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="db38f-115">Példák</span><span class="sxs-lookup"><span data-stu-id="db38f-115">EXAMPLES</span></span>

### <span data-ttu-id="db38f-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db38f-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="db38f-117">Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.</span><span class="sxs-lookup"><span data-stu-id="db38f-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="db38f-118">2. példa: szolgáltatás kérése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="db38f-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="db38f-119">Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.</span><span class="sxs-lookup"><span data-stu-id="db38f-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="db38f-120">3. példa: szolgáltatás beszerzése a Service objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="db38f-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="db38f-121">Ez a parancs olyan szolgáltatást kap, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="db38f-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="db38f-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db38f-122">PARAMETERS</span></span>

### <span data-ttu-id="db38f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db38f-123">-DefaultProfile</span></span>
<span data-ttu-id="db38f-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db38f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db38f-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db38f-125">-Name</span></span>
<span data-ttu-id="db38f-126">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="db38f-126">The name of the service.</span></span>

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

### <span data-ttu-id="db38f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db38f-127">-ResourceGroupName</span></span>
<span data-ttu-id="db38f-128">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="db38f-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db38f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db38f-129">-ResourceId</span></span>
<span data-ttu-id="db38f-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="db38f-130">The resource identifier.</span></span>

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

### <span data-ttu-id="db38f-131">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="db38f-131">-Service</span></span>
<span data-ttu-id="db38f-132">Service objektum.</span><span class="sxs-lookup"><span data-stu-id="db38f-132">Service object.</span></span>

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

### <span data-ttu-id="db38f-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="db38f-133">-ServiceTopology</span></span>
<span data-ttu-id="db38f-134">A szolgáltatás topológiájának objektuma, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="db38f-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="db38f-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="db38f-135">-ServiceTopologyName</span></span>
<span data-ttu-id="db38f-136">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="db38f-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="db38f-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="db38f-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="db38f-138">A szolgáltatás topológiája erőforrás-azonosító, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="db38f-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="db38f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db38f-139">CommonParameters</span></span>
<span data-ttu-id="db38f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db38f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db38f-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db38f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db38f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db38f-142">INPUTS</span></span>

### <span data-ttu-id="db38f-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="db38f-143">None</span></span>

## <span data-ttu-id="db38f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db38f-144">OUTPUTS</span></span>

### <span data-ttu-id="db38f-145">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="db38f-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="db38f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db38f-146">NOTES</span></span>

## <span data-ttu-id="db38f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db38f-147">RELATED LINKS</span></span>

[<span data-ttu-id="db38f-148">Új – AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="db38f-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="db38f-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="db38f-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="db38f-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="db38f-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)