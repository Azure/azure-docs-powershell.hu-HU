---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572105"
---
# <span data-ttu-id="5bdc4-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5bdc4-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="5bdc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdc4-103">Szolgáltatás topológiát kap.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="5bdc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bdc4-104">SYNTAX</span></span>

### <span data-ttu-id="5bdc4-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bdc4-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bdc4-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="5bdc4-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bdc4-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="5bdc4-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bdc4-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bdc4-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bdc4-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="5bdc4-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bdc4-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bdc4-110">DESCRIPTION</span></span>
<span data-ttu-id="5bdc4-111">A **Get-AzureRmDeploymentManagerService parancsmag** szolgáltatás-topológia alapján kap egy szolgáltatást, és az adott szolgáltatást képviselő objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="5bdc4-112">Adja meg a szolgáltatást a neve, a szolgáltatás topológiája és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="5bdc4-113">Másik módon meg is használhatja a Service objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="5bdc4-114">Ezt az objektumot helyben módosíthatja, majd a Set-AzureRmDeploymentManagerService alkalmazhatja a szolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="5bdc4-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bdc4-115">EXAMPLES</span></span>

### <span data-ttu-id="5bdc4-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="5bdc4-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="5bdc4-117">Ez a parancs egy ContosoService1 nevű szolgáltatást kap a ContosoServiceTopology nevű szolgáltatás topológiában a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5bdc4-118">2. példa: Szolgáltatás lekérte az erőforrás-azonosítót használva.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="5bdc4-119">Ez a parancs egy ContosoService1 nevű szolgáltatást kap a ContosoServiceTopology nevű szolgáltatás topológiában a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5bdc4-120">3. példa: Szolgáltatás lekérte a szolgáltatásobjektumot használva.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="5bdc4-121">Ez a parancs egy olyan szolgáltatást kap, amelynek a neve, a szolgáltatás topológiája és az Erőforráscsoport neve megegyezik a $serviceObject, ServiceTopologyName és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="5bdc4-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bdc4-122">PARAMETERS</span></span>

### <span data-ttu-id="5bdc4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdc4-123">-DefaultProfile</span></span>
<span data-ttu-id="5bdc4-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bdc4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5bdc4-125">-Name</span></span>
<span data-ttu-id="5bdc4-126">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-126">The name of the service.</span></span>

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

### <span data-ttu-id="5bdc4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bdc4-127">-ResourceGroupName</span></span>
<span data-ttu-id="5bdc4-128">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-128">The resource group.</span></span>

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

### <span data-ttu-id="5bdc4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bdc4-129">-ResourceId</span></span>
<span data-ttu-id="5bdc4-130">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-130">The resource identifier.</span></span>

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

### <span data-ttu-id="5bdc4-131">-Service</span><span class="sxs-lookup"><span data-stu-id="5bdc4-131">-Service</span></span>
<span data-ttu-id="5bdc4-132">Szolgáltatásobjektum.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-132">Service object.</span></span>

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

### <span data-ttu-id="5bdc4-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5bdc4-133">-ServiceTopology</span></span>
<span data-ttu-id="5bdc4-134">Az a szolgáltatás topológia objektum, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="5bdc4-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="5bdc4-135">-ServiceTopologyName</span></span>
<span data-ttu-id="5bdc4-136">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="5bdc4-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="5bdc4-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="5bdc4-138">Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="5bdc4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdc4-139">CommonParameters</span></span>
<span data-ttu-id="5bdc4-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bdc4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdc4-141">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bdc4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdc4-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bdc4-142">INPUTS</span></span>

### <span data-ttu-id="5bdc4-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="5bdc4-143">None</span></span>

## <span data-ttu-id="5bdc4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bdc4-144">OUTPUTS</span></span>

### <span data-ttu-id="5bdc4-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="5bdc4-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="5bdc4-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bdc4-146">NOTES</span></span>

## <span data-ttu-id="5bdc4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bdc4-147">RELATED LINKS</span></span>

[<span data-ttu-id="5bdc4-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5bdc4-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="5bdc4-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5bdc4-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="5bdc4-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5bdc4-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
