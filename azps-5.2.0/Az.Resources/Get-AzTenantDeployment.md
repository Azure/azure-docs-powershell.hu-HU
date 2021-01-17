---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365258"
---
# <span data-ttu-id="ab145-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ab145-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="ab145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab145-102">SYNOPSIS</span></span>
<span data-ttu-id="ab145-103">Üzembe helyezés bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="ab145-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="ab145-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab145-104">SYNTAX</span></span>

### <span data-ttu-id="ab145-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab145-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab145-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ab145-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab145-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab145-107">DESCRIPTION</span></span>
<span data-ttu-id="ab145-108">A **Get-AztenantDeployment** parancsmag a telepítéseket a bérlő hatókörében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab145-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="ab145-109">Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="ab145-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ab145-110">Alapértelmezés szerint a **Get-AzTenantDeployment** az összes telepítést a bérlői webhelyen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab145-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="ab145-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab145-111">EXAMPLES</span></span>

### <span data-ttu-id="ab145-112">1. példa: Az összes telepítés lekérte a bérlői webhely hatókörét</span><span class="sxs-lookup"><span data-stu-id="ab145-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="ab145-113">Ez a parancs az összes központi telepítést a bérlő aktuális hatókörében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab145-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="ab145-114">2. példa: Telepítés lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="ab145-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="ab145-115">Ez a parancs a "Deploy01" telepítést az aktuális bérlői hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab145-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="ab145-116">A **New-AztenantDeployment** parancsmagok használatával nevet rendelhet a telepítéshez, amikor létrehozza.</span><span class="sxs-lookup"><span data-stu-id="ab145-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="ab145-117">Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.</span><span class="sxs-lookup"><span data-stu-id="ab145-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ab145-118">3. példa: Telepítés lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="ab145-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="ab145-119">Ez a parancs a bérlő hatókörében kapja meg a "Deploy01" telepítést.</span><span class="sxs-lookup"><span data-stu-id="ab145-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="ab145-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab145-120">PARAMETERS</span></span>

### <span data-ttu-id="ab145-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab145-121">-DefaultProfile</span></span>
<span data-ttu-id="ab145-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab145-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab145-123">-Id</span><span class="sxs-lookup"><span data-stu-id="ab145-123">-Id</span></span>
<span data-ttu-id="ab145-124">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ab145-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ab145-125">példa: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ab145-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="ab145-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ab145-126">-Name</span></span>
<span data-ttu-id="ab145-127">Az üzembe helyezés neve.</span><span class="sxs-lookup"><span data-stu-id="ab145-127">The name of deployment.</span></span>

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

### <span data-ttu-id="ab145-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="ab145-128">-Pre</span></span>
<span data-ttu-id="ab145-129">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ab145-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ab145-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab145-130">CommonParameters</span></span>
<span data-ttu-id="ab145-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab145-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab145-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab145-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab145-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab145-133">INPUTS</span></span>

### <span data-ttu-id="ab145-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab145-134">None</span></span>

## <span data-ttu-id="ab145-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab145-135">OUTPUTS</span></span>

### <span data-ttu-id="ab145-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ab145-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ab145-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab145-137">NOTES</span></span>

## <span data-ttu-id="ab145-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab145-138">RELATED LINKS</span></span>
