---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 54a48a025dff2bba2c1ad620237d0a84aacf7d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666666"
---
# <span data-ttu-id="1f75b-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1f75b-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="1f75b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f75b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f75b-103">Megkapja a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="1f75b-103">Gets the service topology.</span></span>

## <span data-ttu-id="1f75b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f75b-104">SYNTAX</span></span>

### <span data-ttu-id="1f75b-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f75b-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f75b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f75b-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f75b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1f75b-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f75b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f75b-108">DESCRIPTION</span></span>
<span data-ttu-id="1f75b-109">A **Get-AzDeploymentManagerServiceTopology** parancsmag szolgáltatási topológiát kap.</span><span class="sxs-lookup"><span data-stu-id="1f75b-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="1f75b-110">Ezt az objektumot helyileg módosíthatja, majd az Set-AzDeploymentManagerServiceTopology parancsmag használatával alkalmazhatja a módosításokat a topológiára.</span><span class="sxs-lookup"><span data-stu-id="1f75b-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="1f75b-111">Adja meg a szolgáltatás topológiáját a nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="1f75b-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="1f75b-112">Másik lehetőségként megadhatja a ServiceTopology objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1f75b-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="1f75b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="1f75b-113">EXAMPLES</span></span>

### <span data-ttu-id="1f75b-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1f75b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="1f75b-115">Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f75b-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1f75b-116">2. példa: a szolgáltatás topológiájának beszerzése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="1f75b-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="1f75b-117">Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f75b-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1f75b-118">3. példa: a szolgáltatás topológiájának beszerzése a Service topológia objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="1f75b-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="1f75b-119">Ez a parancs olyan szolgáltatási topológiát kap, amelynek a neve és a ResourceGroup megegyezik a $serviceTopologyObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="1f75b-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="1f75b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f75b-120">PARAMETERS</span></span>

### <span data-ttu-id="1f75b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f75b-121">-DefaultProfile</span></span>
<span data-ttu-id="1f75b-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f75b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f75b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f75b-123">-InputObject</span></span>
<span data-ttu-id="1f75b-124">Szolgáltatási topológia erőforrás-objektuma.</span><span class="sxs-lookup"><span data-stu-id="1f75b-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="1f75b-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f75b-125">-Name</span></span>
<span data-ttu-id="1f75b-126">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="1f75b-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="1f75b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f75b-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f75b-128">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="1f75b-128">The resource group.</span></span>

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

### <span data-ttu-id="1f75b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f75b-129">-ResourceId</span></span>
<span data-ttu-id="1f75b-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1f75b-130">The resource identifier.</span></span>

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

### <span data-ttu-id="1f75b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f75b-131">CommonParameters</span></span>
<span data-ttu-id="1f75b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f75b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f75b-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f75b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f75b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f75b-134">INPUTS</span></span>

### <span data-ttu-id="1f75b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1f75b-135">System.String</span></span>

### <span data-ttu-id="1f75b-136">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="1f75b-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="1f75b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f75b-137">OUTPUTS</span></span>

### <span data-ttu-id="1f75b-138">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="1f75b-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="1f75b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f75b-139">NOTES</span></span>

## <span data-ttu-id="1f75b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f75b-140">RELATED LINKS</span></span>
