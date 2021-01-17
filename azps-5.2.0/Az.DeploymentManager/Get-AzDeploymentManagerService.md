---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324250"
---
# <span data-ttu-id="dc3d4-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="dc3d4-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="dc3d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3d4-103">A szolgáltatás lekérte.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-103">Gets the service.</span></span>

## <span data-ttu-id="dc3d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dc3d4-104">SYNTAX</span></span>

### <span data-ttu-id="dc3d4-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc3d4-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc3d4-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="dc3d4-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc3d4-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="dc3d4-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc3d4-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc3d4-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc3d4-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc3d4-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc3d4-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dc3d4-110">DESCRIPTION</span></span>
<span data-ttu-id="dc3d4-111">A **Get-AzDeploymentManagerService parancsmag** szolgáltatás-topológia alapján kap egy szolgáltatást, és visszaadja az adott szolgáltatást képviselő objektumot.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="dc3d4-112">Adja meg a szolgáltatást a neve, a szolgáltatás topológiája és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="dc3d4-113">Másik módon meg is használhatja a Service objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="dc3d4-114">Ezt az objektumot helyben módosíthatja, majd a Set-AzDeploymentManagerService alkalmazhatja a szolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="dc3d4-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dc3d4-115">EXAMPLES</span></span>

### <span data-ttu-id="dc3d4-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="dc3d4-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="dc3d4-117">Ez a parancs egy ContosoService1 nevű szolgáltatást kap a ContosoServiceTopology nevű szolgáltatás topológiában a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="dc3d4-118">2. példa: Szolgáltatás lekérte az erőforrás-azonosítót használva.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="dc3d4-119">Ez a parancs egy ContosoService1 nevű szolgáltatást kap a ContosoServiceTopology nevű szolgáltatás topológiában a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="dc3d4-120">3. példa: Szolgáltatás lekérte a szolgáltatásobjektumot.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="dc3d4-121">Ez a parancs egy olyan szolgáltatást kap, amelynek a neve, a szolgáltatás topológiája és az Erőforráscsoport neve megegyezik a $serviceObject, ServiceTopologyName és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="dc3d4-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc3d4-122">PARAMETERS</span></span>

### <span data-ttu-id="dc3d4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3d4-123">-DefaultProfile</span></span>
<span data-ttu-id="dc3d4-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc3d4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc3d4-125">-InputObject</span></span>
<span data-ttu-id="dc3d4-126">Szolgáltatásobjektum.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-126">Service object.</span></span>

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

### <span data-ttu-id="dc3d4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="dc3d4-127">-Name</span></span>
<span data-ttu-id="dc3d4-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-128">The name of the service.</span></span>

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

### <span data-ttu-id="dc3d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc3d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc3d4-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-130">The resource group.</span></span>

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

### <span data-ttu-id="dc3d4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc3d4-131">-ResourceId</span></span>
<span data-ttu-id="dc3d4-132">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-132">The resource identifier.</span></span>

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

### <span data-ttu-id="dc3d4-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="dc3d4-133">-ServiceTopologyName</span></span>
<span data-ttu-id="dc3d4-134">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="dc3d4-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="dc3d4-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="dc3d4-136">Az a szolgáltatás topológia objektum, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="dc3d4-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="dc3d4-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="dc3d4-138">Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="dc3d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3d4-139">CommonParameters</span></span>
<span data-ttu-id="dc3d4-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3d4-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc3d4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3d4-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc3d4-142">INPUTS</span></span>

### <span data-ttu-id="dc3d4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="dc3d4-143">System.String</span></span>

### <span data-ttu-id="dc3d4-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="dc3d4-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="dc3d4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc3d4-145">OUTPUTS</span></span>

### <span data-ttu-id="dc3d4-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="dc3d4-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="dc3d4-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dc3d4-147">NOTES</span></span>

## <span data-ttu-id="dc3d4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc3d4-148">RELATED LINKS</span></span>
