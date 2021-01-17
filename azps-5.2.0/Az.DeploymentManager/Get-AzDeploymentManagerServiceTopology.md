---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324235"
---
# <span data-ttu-id="f4d0e-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="f4d0e-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="f4d0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d0e-103">Beszerzi a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-103">Gets the service topology.</span></span>

## <span data-ttu-id="f4d0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4d0e-104">SYNTAX</span></span>

### <span data-ttu-id="f4d0e-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4d0e-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4d0e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d0e-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d0e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4d0e-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d0e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4d0e-108">DESCRIPTION</span></span>
<span data-ttu-id="f4d0e-109">A **Get-AzDeploymentManagerServiceTopology** parancsmag szolgáltatás topológiát kap.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="f4d0e-110">Ezt az objektumot helyileg módosíthatja, majd a topológia módosításait a Set-AzDeploymentManagerServiceTopology parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="f4d0e-111">Adja meg a szolgáltatás topológiáját a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="f4d0e-112">Másik módon meg is használhatja a ServiceTopology objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="f4d0e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4d0e-113">EXAMPLES</span></span>

### <span data-ttu-id="f4d0e-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="f4d0e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="f4d0e-115">Ez a parancs egy ContosoServiceTopology nevű szolgáltatás-topológiát kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4d0e-116">2. példa: Szolgáltatás topológiájának lekérte az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="f4d0e-117">Ez a parancs egy ContosoServiceTopology nevű szolgáltatás-topológiát kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4d0e-118">3. példa: Szolgáltatás-topológia lekérte a szolgáltatás topológia objektumát.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="f4d0e-119">Ez a parancs egy olyan szolgáltatás-topológiát kap, amelynek neve és ResourceGroup tulajdonsága megegyezik a $serviceTopologyObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="f4d0e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4d0e-120">PARAMETERS</span></span>

### <span data-ttu-id="f4d0e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d0e-121">-DefaultProfile</span></span>
<span data-ttu-id="f4d0e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d0e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4d0e-123">-InputObject</span></span>
<span data-ttu-id="f4d0e-124">Szolgáltatás topológia erőforrásobjektuma.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="f4d0e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f4d0e-125">-Name</span></span>
<span data-ttu-id="f4d0e-126">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="f4d0e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d0e-127">-ResourceGroupName</span></span>
<span data-ttu-id="f4d0e-128">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-128">The resource group.</span></span>

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

### <span data-ttu-id="f4d0e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d0e-129">-ResourceId</span></span>
<span data-ttu-id="f4d0e-130">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-130">The resource identifier.</span></span>

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

### <span data-ttu-id="f4d0e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d0e-131">CommonParameters</span></span>
<span data-ttu-id="f4d0e-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d0e-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4d0e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d0e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4d0e-134">INPUTS</span></span>

### <span data-ttu-id="f4d0e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f4d0e-135">System.String</span></span>

### <span data-ttu-id="f4d0e-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="f4d0e-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="f4d0e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4d0e-137">OUTPUTS</span></span>

### <span data-ttu-id="f4d0e-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="f4d0e-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="f4d0e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4d0e-139">NOTES</span></span>

## <span data-ttu-id="f4d0e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4d0e-140">RELATED LINKS</span></span>
