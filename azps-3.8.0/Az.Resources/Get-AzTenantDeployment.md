---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013778"
---
# <span data-ttu-id="d4596-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d4596-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="d4596-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4596-102">SYNOPSIS</span></span>
<span data-ttu-id="d4596-103">A központi bevezetés a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="d4596-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="d4596-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4596-104">SYNTAX</span></span>

### <span data-ttu-id="d4596-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4596-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4596-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d4596-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4596-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4596-107">DESCRIPTION</span></span>
<span data-ttu-id="d4596-108">A **Get-AzTenantDeployment** parancsmag a bevezetéseket a bérlői hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d4596-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="d4596-109">Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="d4596-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d4596-110">Alapértelmezés szerint a **Get-AzTenantDeployment** minden telepített példányát bekapja a bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="d4596-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="d4596-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d4596-111">EXAMPLES</span></span>

### <span data-ttu-id="d4596-112">1. példa: a bevezetések beszerzése a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="d4596-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="d4596-113">Ez a parancs a jelenlegi bérlői tartomány minden telepített példányát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="d4596-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="d4596-114">2. példa: a központi felügyelet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="d4596-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="d4596-115">A parancs a jelenlegi bérlői hatókörben a "Deploy01" bevezetést kapja.</span><span class="sxs-lookup"><span data-stu-id="d4596-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="d4596-116">A **AzTenantDeployment-** parancsmagok használatával létrehozhatja a kívánt nevet a telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="d4596-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="d4596-117">Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.</span><span class="sxs-lookup"><span data-stu-id="d4596-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="d4596-118">3. példa: bevezetési azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="d4596-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="d4596-119">Ez a parancs a "Deploy01" bevezetését a bérlői hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d4596-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="d4596-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4596-120">PARAMETERS</span></span>

### <span data-ttu-id="d4596-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4596-121">-ApiVersion</span></span>
<span data-ttu-id="d4596-122">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4596-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d4596-123">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d4596-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d4596-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4596-124">-DefaultProfile</span></span>
<span data-ttu-id="d4596-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4596-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4596-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d4596-126">-Id</span></span>
<span data-ttu-id="d4596-127">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4596-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d4596-128">Példa:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d4596-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="d4596-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4596-129">-Name</span></span>
<span data-ttu-id="d4596-130">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="d4596-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4596-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4596-131">-Pre</span></span>
<span data-ttu-id="d4596-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="d4596-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d4596-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4596-133">CommonParameters</span></span>
<span data-ttu-id="d4596-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4596-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4596-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4596-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4596-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4596-136">INPUTS</span></span>

### <span data-ttu-id="d4596-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4596-137">None</span></span>

## <span data-ttu-id="d4596-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4596-138">OUTPUTS</span></span>

### <span data-ttu-id="d4596-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d4596-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d4596-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4596-140">NOTES</span></span>

## <span data-ttu-id="d4596-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4596-141">RELATED LINKS</span></span>
