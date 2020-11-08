---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014394"
---
# <span data-ttu-id="ac960-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ac960-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="ac960-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac960-102">SYNOPSIS</span></span>
<span data-ttu-id="ac960-103">Megkapja a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="ac960-103">Gets the service topology.</span></span>

## <span data-ttu-id="ac960-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac960-104">SYNTAX</span></span>

### <span data-ttu-id="ac960-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac960-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac960-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac960-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac960-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ac960-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac960-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac960-108">DESCRIPTION</span></span>
<span data-ttu-id="ac960-109">A **Get-AzDeploymentManagerServiceTopology** parancsmag szolgáltatási topológiát kap.</span><span class="sxs-lookup"><span data-stu-id="ac960-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="ac960-110">Ezt az objektumot helyileg módosíthatja, majd az Set-AzDeploymentManagerServiceTopology parancsmag használatával alkalmazhatja a módosításokat a topológiára.</span><span class="sxs-lookup"><span data-stu-id="ac960-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="ac960-111">Adja meg a szolgáltatás topológiáját a nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="ac960-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="ac960-112">Másik lehetőségként megadhatja a ServiceTopology objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ac960-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="ac960-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ac960-113">EXAMPLES</span></span>

### <span data-ttu-id="ac960-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac960-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="ac960-115">Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ac960-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ac960-116">2. példa: a szolgáltatás topológiájának beszerzése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="ac960-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="ac960-117">Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ac960-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ac960-118">3. példa: a szolgáltatás topológiájának beszerzése a Service topológia objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="ac960-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="ac960-119">Ez a parancs olyan szolgáltatási topológiát kap, amelynek a neve és a ResourceGroup megegyezik a $serviceTopologyObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="ac960-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="ac960-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac960-120">PARAMETERS</span></span>

### <span data-ttu-id="ac960-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac960-121">-DefaultProfile</span></span>
<span data-ttu-id="ac960-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac960-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac960-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac960-123">-InputObject</span></span>
<span data-ttu-id="ac960-124">Szolgáltatási topológia erőforrás-objektuma.</span><span class="sxs-lookup"><span data-stu-id="ac960-124">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac960-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac960-125">-Name</span></span>
<span data-ttu-id="ac960-126">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="ac960-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac960-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac960-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac960-128">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="ac960-128">The resource group.</span></span>

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

### <span data-ttu-id="ac960-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac960-129">-ResourceId</span></span>
<span data-ttu-id="ac960-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ac960-130">The resource identifier.</span></span>

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

### <span data-ttu-id="ac960-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac960-131">CommonParameters</span></span>
<span data-ttu-id="ac960-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac960-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac960-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac960-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac960-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac960-134">INPUTS</span></span>

### <span data-ttu-id="ac960-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ac960-135">System.String</span></span>

### <span data-ttu-id="ac960-136">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="ac960-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ac960-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac960-137">OUTPUTS</span></span>

### <span data-ttu-id="ac960-138">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="ac960-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ac960-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac960-139">NOTES</span></span>

## <span data-ttu-id="ac960-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac960-140">RELATED LINKS</span></span>
