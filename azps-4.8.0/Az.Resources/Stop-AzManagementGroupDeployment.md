---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 8604aa58efff7b6fe7ef6dc931fdcb54b313d634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172759"
---
# <span data-ttu-id="c099c-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c099c-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="c099c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c099c-102">SYNOPSIS</span></span>
<span data-ttu-id="c099c-103">Futó telepített példány lemondása felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="c099c-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="c099c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c099c-104">SYNTAX</span></span>

### <span data-ttu-id="c099c-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c099c-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c099c-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c099c-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c099c-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="c099c-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c099c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c099c-108">DESCRIPTION</span></span>
<span data-ttu-id="c099c-109">A **stop-AzManagementGroupDeployment** parancsmag lemondja azokat a telepített példányokat, amelyek egy felügyeleti csoportban elkezdődtek, de nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="c099c-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="c099c-110">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="c099c-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="c099c-111">Ha egy felügyeleti csoportban szeretne bevezetést létrehozni, használja az New-AzManagementGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c099c-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="c099c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c099c-112">EXAMPLES</span></span>

### <span data-ttu-id="c099c-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c099c-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="c099c-114">Ez a parancs lemondja a "deployment01" futó központi telepítőt a "myMG" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="c099c-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="c099c-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="c099c-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="c099c-116">Ez a parancs a "deployment01" ("myMG") felügyeleti csoport "" üzembe állítását adja vissza, és lemondja azt.</span><span class="sxs-lookup"><span data-stu-id="c099c-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="c099c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c099c-117">PARAMETERS</span></span>

### <span data-ttu-id="c099c-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c099c-118">-ApiVersion</span></span>
<span data-ttu-id="c099c-119">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c099c-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c099c-120">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c099c-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c099c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c099c-121">-DefaultProfile</span></span>
<span data-ttu-id="c099c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c099c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c099c-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c099c-123">-Id</span></span>
<span data-ttu-id="c099c-124">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c099c-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c099c-125">Példa:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c099c-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c099c-126">-InputObject</span></span>
<span data-ttu-id="c099c-127">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="c099c-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c099c-128">-ManagementGroupId</span></span>
<span data-ttu-id="c099c-129">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c099c-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c099c-130">-Name</span></span>
<span data-ttu-id="c099c-131">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="c099c-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c099c-132">-PassThru</span></span>
<span data-ttu-id="c099c-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c099c-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c099c-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="c099c-134">-Pre</span></span>
<span data-ttu-id="c099c-135">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c099c-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c099c-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c099c-136">-Confirm</span></span>
<span data-ttu-id="c099c-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c099c-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c099c-138">-WhatIf</span></span>
<span data-ttu-id="c099c-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c099c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c099c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c099c-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c099c-141">CommonParameters</span></span>
<span data-ttu-id="c099c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c099c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c099c-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c099c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c099c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c099c-144">INPUTS</span></span>

### <span data-ttu-id="c099c-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c099c-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c099c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c099c-146">OUTPUTS</span></span>

### <span data-ttu-id="c099c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c099c-147">System.Boolean</span></span>

## <span data-ttu-id="c099c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c099c-148">NOTES</span></span>

## <span data-ttu-id="c099c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c099c-149">RELATED LINKS</span></span>
