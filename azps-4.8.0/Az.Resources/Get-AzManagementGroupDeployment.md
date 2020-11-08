---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184227"
---
# <span data-ttu-id="ee99e-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ee99e-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ee99e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee99e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee99e-103">Bevezetés beszerzése felügyeleti csoporttal</span><span class="sxs-lookup"><span data-stu-id="ee99e-103">Get deployment at a management group</span></span>

## <span data-ttu-id="ee99e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee99e-104">SYNTAX</span></span>

### <span data-ttu-id="ee99e-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee99e-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee99e-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ee99e-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee99e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee99e-107">DESCRIPTION</span></span>
<span data-ttu-id="ee99e-108">A **Get-AzManagementGroupDeployment** parancsmag a központi telepítőket kapja meg a felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="ee99e-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="ee99e-109">Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="ee99e-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ee99e-110">A **Get-AzManagementGroupDeployment** alapértelmezés szerint a felügyeleti csoport minden telepített példányát bekapja.</span><span class="sxs-lookup"><span data-stu-id="ee99e-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="ee99e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ee99e-111">EXAMPLES</span></span>

### <span data-ttu-id="ee99e-112">Példa 1: az összes telepített példány beszerzése egy felügyeleti csoportba</span><span class="sxs-lookup"><span data-stu-id="ee99e-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="ee99e-113">Ez a parancs a "myMG" felügyeleti csoport minden telepített példányát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="ee99e-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="ee99e-114">2. példa: a központi felügyelet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="ee99e-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="ee99e-115">Ez a parancs a "Deploy01" bevezetést kapja a "myMG" felügyeleti csoportnál.</span><span class="sxs-lookup"><span data-stu-id="ee99e-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="ee99e-116">A **AzManagementGroupDeployment-** parancsmagok használatával létrehozhatja a kívánt nevet a telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="ee99e-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="ee99e-117">Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.</span><span class="sxs-lookup"><span data-stu-id="ee99e-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ee99e-118">3. példa: bevezetési azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="ee99e-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="ee99e-119">Ez a parancs a "Deploy01" bevezetést kapja a "myMG" felügyeleti csoportnál.</span><span class="sxs-lookup"><span data-stu-id="ee99e-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="ee99e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee99e-120">PARAMETERS</span></span>

### <span data-ttu-id="ee99e-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ee99e-121">-ApiVersion</span></span>
<span data-ttu-id="ee99e-122">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee99e-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ee99e-123">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ee99e-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee99e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee99e-124">-DefaultProfile</span></span>
<span data-ttu-id="ee99e-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee99e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee99e-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ee99e-126">-Id</span></span>
<span data-ttu-id="ee99e-127">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee99e-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ee99e-128">Példa:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ee99e-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee99e-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ee99e-129">-ManagementGroupId</span></span>
<span data-ttu-id="ee99e-130">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee99e-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee99e-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee99e-131">-Name</span></span>
<span data-ttu-id="ee99e-132">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="ee99e-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee99e-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="ee99e-133">-Pre</span></span>
<span data-ttu-id="ee99e-134">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ee99e-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee99e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee99e-135">CommonParameters</span></span>
<span data-ttu-id="ee99e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee99e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee99e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee99e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee99e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee99e-138">INPUTS</span></span>

### <span data-ttu-id="ee99e-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee99e-139">None</span></span>

## <span data-ttu-id="ee99e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee99e-140">OUTPUTS</span></span>

### <span data-ttu-id="ee99e-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ee99e-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ee99e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee99e-142">NOTES</span></span>

## <span data-ttu-id="ee99e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee99e-143">RELATED LINKS</span></span>
