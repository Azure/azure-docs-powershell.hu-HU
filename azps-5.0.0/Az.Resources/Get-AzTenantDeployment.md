---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301058"
---
# <span data-ttu-id="5806d-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="5806d-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="5806d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5806d-102">SYNOPSIS</span></span>
<span data-ttu-id="5806d-103">A központi bevezetés a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="5806d-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="5806d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5806d-104">SYNTAX</span></span>

### <span data-ttu-id="5806d-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5806d-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5806d-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5806d-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5806d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5806d-107">DESCRIPTION</span></span>
<span data-ttu-id="5806d-108">A **Get-AzTenantDeployment** parancsmag a bevezetéseket a bérlői hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5806d-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="5806d-109">Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="5806d-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="5806d-110">Alapértelmezés szerint a **Get-AzTenantDeployment** minden telepített példányát bekapja a bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="5806d-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="5806d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5806d-111">EXAMPLES</span></span>

### <span data-ttu-id="5806d-112">1. példa: a bevezetések beszerzése a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="5806d-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="5806d-113">Ez a parancs a jelenlegi bérlői tartomány minden telepített példányát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="5806d-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="5806d-114">2. példa: a központi felügyelet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="5806d-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="5806d-115">A parancs a jelenlegi bérlői hatókörben a "Deploy01" bevezetést kapja.</span><span class="sxs-lookup"><span data-stu-id="5806d-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="5806d-116">A **AzTenantDeployment-** parancsmagok használatával létrehozhatja a kívánt nevet a telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="5806d-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="5806d-117">Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.</span><span class="sxs-lookup"><span data-stu-id="5806d-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="5806d-118">3. példa: bevezetési azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="5806d-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="5806d-119">Ez a parancs a "Deploy01" bevezetését a bérlői hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5806d-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="5806d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5806d-120">PARAMETERS</span></span>

### <span data-ttu-id="5806d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5806d-121">-DefaultProfile</span></span>
<span data-ttu-id="5806d-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5806d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5806d-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5806d-123">-Id</span></span>
<span data-ttu-id="5806d-124">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5806d-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5806d-125">Példa:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="5806d-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="5806d-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5806d-126">-Name</span></span>
<span data-ttu-id="5806d-127">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="5806d-127">The name of deployment.</span></span>

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

### <span data-ttu-id="5806d-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="5806d-128">-Pre</span></span>
<span data-ttu-id="5806d-129">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="5806d-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5806d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5806d-130">CommonParameters</span></span>
<span data-ttu-id="5806d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5806d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5806d-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5806d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5806d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5806d-133">INPUTS</span></span>

### <span data-ttu-id="5806d-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="5806d-134">None</span></span>

## <span data-ttu-id="5806d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5806d-135">OUTPUTS</span></span>

### <span data-ttu-id="5806d-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5806d-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5806d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5806d-137">NOTES</span></span>

## <span data-ttu-id="5806d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5806d-138">RELATED LINKS</span></span>
