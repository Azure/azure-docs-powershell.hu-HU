---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466546"
---
# <span data-ttu-id="a8ca6-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a8ca6-101">Get-AzDeployment</span></span>

## <span data-ttu-id="a8ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ca6-103">Üzembe helyezés</span><span class="sxs-lookup"><span data-stu-id="a8ca6-103">Get deployment</span></span>

## <span data-ttu-id="a8ca6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8ca6-104">SYNTAX</span></span>

### <span data-ttu-id="a8ca6-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8ca6-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8ca6-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a8ca6-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8ca6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8ca6-107">DESCRIPTION</span></span>
<span data-ttu-id="a8ca6-108">A **Get-AzDeployment** parancsmag az aktuális előfizetési hatókörű telepítéseket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="a8ca6-109">Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="a8ca6-110">Alapértelmezés szerint a **Get-AzDeployment** az összes telepítést az aktuális előfizetési hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="a8ca6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8ca6-111">EXAMPLES</span></span>

### <span data-ttu-id="a8ca6-112">1. példa: Az összes telepítés lekérte az előfizetés hatókörét</span><span class="sxs-lookup"><span data-stu-id="a8ca6-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="a8ca6-113">Ez a parancs az összes telepítést az aktuális előfizetési hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="a8ca6-114">2. példa: Telepítés lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="a8ca6-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="a8ca6-115">Ez a parancs a DeployRoles01 telepítést az aktuális előfizetési hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="a8ca6-116">A **New-AzDeployment parancsmagok** használatával nevet rendelhet a telepítéshez, amikor létrehozza.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="a8ca6-117">Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="a8ca6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8ca6-118">PARAMETERS</span></span>

### <span data-ttu-id="a8ca6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ca6-119">-DefaultProfile</span></span>
<span data-ttu-id="a8ca6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ca6-121">-Id</span><span class="sxs-lookup"><span data-stu-id="a8ca6-121">-Id</span></span>
<span data-ttu-id="a8ca6-122">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a8ca6-123">példa: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a8ca6-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="a8ca6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a8ca6-124">-Name</span></span>
<span data-ttu-id="a8ca6-125">Az üzembe helyezés neve.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-125">The name of deployment.</span></span>

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

### <span data-ttu-id="a8ca6-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="a8ca6-126">-Pre</span></span>
<span data-ttu-id="a8ca6-127">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a8ca6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ca6-128">CommonParameters</span></span>
<span data-ttu-id="a8ca6-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ca6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ca6-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8ca6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ca6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8ca6-131">INPUTS</span></span>

### <span data-ttu-id="a8ca6-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="a8ca6-132">None</span></span>

## <span data-ttu-id="a8ca6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8ca6-133">OUTPUTS</span></span>

### <span data-ttu-id="a8ca6-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a8ca6-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a8ca6-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8ca6-135">NOTES</span></span>

## <span data-ttu-id="a8ca6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8ca6-136">RELATED LINKS</span></span>
