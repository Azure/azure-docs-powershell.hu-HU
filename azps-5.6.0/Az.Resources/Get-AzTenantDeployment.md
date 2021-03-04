---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: 1755438dfc5bdb9b4eedf46ec364e851a2bca154
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942145"
---
# <span data-ttu-id="2ccd7-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="2ccd7-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="2ccd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ccd7-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccd7-103">Üzembe helyezés bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="2ccd7-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="2ccd7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ccd7-104">SYNTAX</span></span>

### <span data-ttu-id="2ccd7-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ccd7-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ccd7-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2ccd7-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ccd7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ccd7-107">DESCRIPTION</span></span>
<span data-ttu-id="2ccd7-108">A **Get-AztenantDeployment** parancsmag a telepítéseket a bérlő hatókörében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="2ccd7-109">Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="2ccd7-110">Alapértelmezés szerint a **Get-AzTenantDeployment** az összes telepítést a bérlői webhelyen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="2ccd7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ccd7-111">EXAMPLES</span></span>

### <span data-ttu-id="2ccd7-112">1. példa: Az összes telepítés lekérte a bérlői webhely hatókörét</span><span class="sxs-lookup"><span data-stu-id="2ccd7-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="2ccd7-113">Ez a parancs az összes központi telepítést a bérlő aktuális hatókörében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="2ccd7-114">2. példa: Telepítés lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="2ccd7-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="2ccd7-115">Ez a parancs a "Deploy01" telepítést az aktuális bérlői hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="2ccd7-116">A **New-AztenantDeployment** parancsmagok használatával nevet rendelhet a telepítéshez, amikor létrehozza.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="2ccd7-117">Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="2ccd7-118">3. példa: Telepítés lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="2ccd7-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="2ccd7-119">Ez a parancs a bérlő hatókörében kapja meg a "Deploy01" telepítést.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="2ccd7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ccd7-120">PARAMETERS</span></span>

### <span data-ttu-id="2ccd7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ccd7-121">-DefaultProfile</span></span>
<span data-ttu-id="2ccd7-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ccd7-123">-Id</span><span class="sxs-lookup"><span data-stu-id="2ccd7-123">-Id</span></span>
<span data-ttu-id="2ccd7-124">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2ccd7-125">példa: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2ccd7-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="2ccd7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2ccd7-126">-Name</span></span>
<span data-ttu-id="2ccd7-127">Az üzembe helyezés neve.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ccd7-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="2ccd7-128">-Pre</span></span>
<span data-ttu-id="2ccd7-129">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2ccd7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccd7-130">CommonParameters</span></span>
<span data-ttu-id="2ccd7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ccd7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccd7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ccd7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccd7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ccd7-133">INPUTS</span></span>

### <span data-ttu-id="2ccd7-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ccd7-134">None</span></span>

## <span data-ttu-id="2ccd7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ccd7-135">OUTPUTS</span></span>

### <span data-ttu-id="2ccd7-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2ccd7-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2ccd7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ccd7-137">NOTES</span></span>

## <span data-ttu-id="2ccd7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ccd7-138">RELATED LINKS</span></span>
