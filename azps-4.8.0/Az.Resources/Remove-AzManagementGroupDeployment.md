---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017650"
---
# <span data-ttu-id="7abaf-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7abaf-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="7abaf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7abaf-102">SYNOPSIS</span></span>
<span data-ttu-id="7abaf-103">A központi felügyelet eltávolítása a felügyeleti csoportokban és a hozzájuk kapcsolódó műveletekben</span><span class="sxs-lookup"><span data-stu-id="7abaf-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="7abaf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7abaf-104">SYNTAX</span></span>

### <span data-ttu-id="7abaf-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7abaf-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7abaf-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7abaf-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7abaf-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7abaf-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7abaf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7abaf-108">DESCRIPTION</span></span>
<span data-ttu-id="7abaf-109">A **Remove-AzManagementGroupDeployment** parancsmag egy olyan Azure-bevezetést távolít el egy felügyeleti csoportban és bármely kapcsolódó műveletben.</span><span class="sxs-lookup"><span data-stu-id="7abaf-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="7abaf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7abaf-110">EXAMPLES</span></span>

### <span data-ttu-id="7abaf-111">1. példa: a példány eltávolítása adott névvel</span><span class="sxs-lookup"><span data-stu-id="7abaf-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="7abaf-112">Ez a parancs eltávolítja a "RolesDeployment" központi telepítőt a "myMG" felügyeleti csoportnál.</span><span class="sxs-lookup"><span data-stu-id="7abaf-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="7abaf-113">2. példa: központi üzembe állítás és eltávolítás</span><span class="sxs-lookup"><span data-stu-id="7abaf-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="7abaf-114">Ez a parancs a "RolesDeployment" ("myMG") felügyeleti csoport "" üzembe állítását és eltávolítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7abaf-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="7abaf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7abaf-115">PARAMETERS</span></span>

### <span data-ttu-id="7abaf-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7abaf-116">-ApiVersion</span></span>
<span data-ttu-id="7abaf-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7abaf-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7abaf-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7abaf-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7abaf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7abaf-119">-AsJob</span></span>
<span data-ttu-id="7abaf-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7abaf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7abaf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abaf-121">-DefaultProfile</span></span>
<span data-ttu-id="7abaf-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7abaf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7abaf-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7abaf-123">-Id</span></span>
<span data-ttu-id="7abaf-124">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7abaf-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7abaf-125">Példa:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7abaf-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7abaf-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7abaf-126">-InputObject</span></span>
<span data-ttu-id="7abaf-127">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="7abaf-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7abaf-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7abaf-128">-ManagementGroupId</span></span>
<span data-ttu-id="7abaf-129">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7abaf-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7abaf-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7abaf-130">-Name</span></span>
<span data-ttu-id="7abaf-131">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="7abaf-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7abaf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7abaf-132">-PassThru</span></span>
<span data-ttu-id="7abaf-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7abaf-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7abaf-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="7abaf-134">-Pre</span></span>
<span data-ttu-id="7abaf-135">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7abaf-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7abaf-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7abaf-136">-Confirm</span></span>
<span data-ttu-id="7abaf-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7abaf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7abaf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abaf-138">-WhatIf</span></span>
<span data-ttu-id="7abaf-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7abaf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7abaf-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7abaf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7abaf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abaf-141">CommonParameters</span></span>
<span data-ttu-id="7abaf-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7abaf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abaf-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7abaf-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abaf-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7abaf-144">INPUTS</span></span>

### <span data-ttu-id="7abaf-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7abaf-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7abaf-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7abaf-146">OUTPUTS</span></span>

### <span data-ttu-id="7abaf-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7abaf-147">System.Boolean</span></span>

## <span data-ttu-id="7abaf-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7abaf-148">NOTES</span></span>

## <span data-ttu-id="7abaf-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7abaf-149">RELATED LINKS</span></span>
