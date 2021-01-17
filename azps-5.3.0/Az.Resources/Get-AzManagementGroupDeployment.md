---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466528"
---
# <span data-ttu-id="bd406-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bd406-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="bd406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd406-102">SYNOPSIS</span></span>
<span data-ttu-id="bd406-103">Központi telepítés egy felügyeleti csoportnál</span><span class="sxs-lookup"><span data-stu-id="bd406-103">Get deployment at a management group</span></span>

## <span data-ttu-id="bd406-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd406-104">SYNTAX</span></span>

### <span data-ttu-id="bd406-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd406-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd406-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="bd406-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd406-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd406-107">DESCRIPTION</span></span>
<span data-ttu-id="bd406-108">A **Get-AzManagementGroupDeployment** parancsmag a telepítéseket a felügyeleti csoportnál kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bd406-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="bd406-109">Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="bd406-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="bd406-110">Alapértelmezés szerint a **Get-AzManagementGroupDeployment** az összes telepítést megkapja a felügyeleti csoportnál.</span><span class="sxs-lookup"><span data-stu-id="bd406-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="bd406-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd406-111">EXAMPLES</span></span>

### <span data-ttu-id="bd406-112">1. példa: Az összes központi telepítés lekérte egy felügyeleti csoportnál</span><span class="sxs-lookup"><span data-stu-id="bd406-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="bd406-113">Ez a parancs az összes központi telepítést a "myMG" felügyeleti csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bd406-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="bd406-114">2. példa: Telepítés lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="bd406-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="bd406-115">Ez a parancs a "Deploy01" telepítést a "myMG" felügyeleti csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bd406-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="bd406-116">A **New-AzManagementGroupDeployment** parancsmagok használatával nevet rendelhet a telepítéshez, amikor létrehozza.</span><span class="sxs-lookup"><span data-stu-id="bd406-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="bd406-117">Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.</span><span class="sxs-lookup"><span data-stu-id="bd406-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="bd406-118">3. példa: Telepítés lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="bd406-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="bd406-119">Ez a parancs a "Deploy01" telepítést a "myMG" felügyeleti csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bd406-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="bd406-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd406-120">PARAMETERS</span></span>

### <span data-ttu-id="bd406-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd406-121">-DefaultProfile</span></span>
<span data-ttu-id="bd406-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd406-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd406-123">-Id</span><span class="sxs-lookup"><span data-stu-id="bd406-123">-Id</span></span>
<span data-ttu-id="bd406-124">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd406-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="bd406-125">példa: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="bd406-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd406-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="bd406-126">-ManagementGroupId</span></span>
<span data-ttu-id="bd406-127">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd406-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd406-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bd406-128">-Name</span></span>
<span data-ttu-id="bd406-129">Az üzembe helyezés neve.</span><span class="sxs-lookup"><span data-stu-id="bd406-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd406-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="bd406-130">-Pre</span></span>
<span data-ttu-id="bd406-131">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bd406-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd406-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd406-132">CommonParameters</span></span>
<span data-ttu-id="bd406-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd406-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd406-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd406-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd406-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd406-135">INPUTS</span></span>

### <span data-ttu-id="bd406-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="bd406-136">None</span></span>

## <span data-ttu-id="bd406-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd406-137">OUTPUTS</span></span>

### <span data-ttu-id="bd406-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="bd406-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="bd406-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd406-139">NOTES</span></span>

## <span data-ttu-id="bd406-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd406-140">RELATED LINKS</span></span>
