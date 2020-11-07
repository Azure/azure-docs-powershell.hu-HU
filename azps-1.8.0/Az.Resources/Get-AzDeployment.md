---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: cde9c4f8827840047e7fa4a1c597ed6338ed8e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669447"
---
# <span data-ttu-id="18f6e-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="18f6e-101">Get-AzDeployment</span></span>

## <span data-ttu-id="18f6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="18f6e-103">A központi telepítő beszerzése</span><span class="sxs-lookup"><span data-stu-id="18f6e-103">Get deployment</span></span>

## <span data-ttu-id="18f6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18f6e-104">SYNTAX</span></span>

### <span data-ttu-id="18f6e-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18f6e-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18f6e-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="18f6e-106">GetByDeploymentId</span></span>
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18f6e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="18f6e-107">DESCRIPTION</span></span>
<span data-ttu-id="18f6e-108">A **Get-AzDeployment** parancsmag a telepített példányokat az aktuális előfizetéses tartományban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="18f6e-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="18f6e-109">Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="18f6e-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="18f6e-110">A **Get-AzDeployment** alapértelmezés szerint az aktuális előfizetési tartomány minden telepített példányát bekapja.</span><span class="sxs-lookup"><span data-stu-id="18f6e-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="18f6e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="18f6e-111">EXAMPLES</span></span>

### <span data-ttu-id="18f6e-112">Példa 1: a bevezetések beszerzése az előfizetések hatókörében</span><span class="sxs-lookup"><span data-stu-id="18f6e-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="18f6e-113">Ez a parancs a jelenlegi előfizetési tartomány minden telepített példányát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="18f6e-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="18f6e-114">2. példa: a központi felügyelet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="18f6e-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="18f6e-115">Ez a parancs a DeployRoles01 telepítését az aktuális előfizetési tartományon keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="18f6e-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="18f6e-116">A **AzDeployment-** parancsmagok használatával létrehozhatja a kívánt nevet a telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="18f6e-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="18f6e-117">Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.</span><span class="sxs-lookup"><span data-stu-id="18f6e-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="18f6e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18f6e-118">PARAMETERS</span></span>

### <span data-ttu-id="18f6e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18f6e-119">-ApiVersion</span></span>
<span data-ttu-id="18f6e-120">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18f6e-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="18f6e-121">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="18f6e-121">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f6e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f6e-122">-DefaultProfile</span></span>
<span data-ttu-id="18f6e-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18f6e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18f6e-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="18f6e-124">-Id</span></span>
<span data-ttu-id="18f6e-125">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="18f6e-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="18f6e-126">Példa:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="18f6e-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f6e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18f6e-127">-Name</span></span>
<span data-ttu-id="18f6e-128">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="18f6e-128">The name of deployment.</span></span>

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

### <span data-ttu-id="18f6e-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="18f6e-129">-Pre</span></span>
<span data-ttu-id="18f6e-130">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="18f6e-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="18f6e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f6e-131">CommonParameters</span></span>
<span data-ttu-id="18f6e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18f6e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f6e-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f6e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f6e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18f6e-134">INPUTS</span></span>

### <span data-ttu-id="18f6e-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="18f6e-135">None</span></span>

## <span data-ttu-id="18f6e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18f6e-136">OUTPUTS</span></span>

### <span data-ttu-id="18f6e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="18f6e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="18f6e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18f6e-138">NOTES</span></span>

## <span data-ttu-id="18f6e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18f6e-139">RELATED LINKS</span></span>
