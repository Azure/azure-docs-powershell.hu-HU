---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c02a88cdb550e1ec9cb343b286d3211045873820
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932978"
---
# <span data-ttu-id="7d3fc-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="7d3fc-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="7d3fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3fc-103">Beszerzi a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-103">Gets the service topology.</span></span>

## <span data-ttu-id="7d3fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7d3fc-104">SYNTAX</span></span>

### <span data-ttu-id="7d3fc-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d3fc-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d3fc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3fc-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d3fc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7d3fc-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d3fc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7d3fc-108">DESCRIPTION</span></span>
<span data-ttu-id="7d3fc-109">A **Get-AzDeploymentManagerServiceTopology** parancsmag szolgáltatás topológiát kap.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="7d3fc-110">Ezt az objektumot helyileg módosíthatja, majd a topológia módosításait a Set-AzDeploymentManagerServiceTopology parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="7d3fc-111">Adja meg a szolgáltatás topológiáját a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="7d3fc-112">Másik módon meg is használhatja a ServiceTopology objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="7d3fc-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7d3fc-113">EXAMPLES</span></span>

### <span data-ttu-id="7d3fc-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="7d3fc-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="7d3fc-115">Ez a parancs egy ContosoServiceTopology nevű szolgáltatás-topológiát kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7d3fc-116">2. példa: Szolgáltatás topológiájának lekérte az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="7d3fc-117">Ez a parancs egy ContosoServiceTopology nevű szolgáltatás-topológiát kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7d3fc-118">3. példa: Szolgáltatás-topológia lekérte a szolgáltatás topológiaobjektumát.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="7d3fc-119">Ez a parancs egy olyan szolgáltatás-topológiát kap, amelynek neve és ResourceGroup tulajdonsága megegyezik a $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="7d3fc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d3fc-120">PARAMETERS</span></span>

### <span data-ttu-id="7d3fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3fc-121">-DefaultProfile</span></span>
<span data-ttu-id="7d3fc-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d3fc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d3fc-123">-InputObject</span></span>
<span data-ttu-id="7d3fc-124">Szolgáltatás topológia erőforrásobjektuma.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="7d3fc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7d3fc-125">-Name</span></span>
<span data-ttu-id="7d3fc-126">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="7d3fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d3fc-128">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-128">The resource group.</span></span>

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

### <span data-ttu-id="7d3fc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3fc-129">-ResourceId</span></span>
<span data-ttu-id="7d3fc-130">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-130">The resource identifier.</span></span>

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

### <span data-ttu-id="7d3fc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3fc-131">CommonParameters</span></span>
<span data-ttu-id="7d3fc-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3fc-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d3fc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3fc-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d3fc-134">INPUTS</span></span>

### <span data-ttu-id="7d3fc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7d3fc-135">System.String</span></span>

### <span data-ttu-id="7d3fc-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="7d3fc-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="7d3fc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d3fc-137">OUTPUTS</span></span>

### <span data-ttu-id="7d3fc-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="7d3fc-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="7d3fc-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7d3fc-139">NOTES</span></span>

## <span data-ttu-id="7d3fc-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d3fc-140">RELATED LINKS</span></span>
