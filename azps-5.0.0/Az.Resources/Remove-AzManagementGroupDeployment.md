---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300542"
---
# <span data-ttu-id="7b060-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7b060-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="7b060-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b060-102">SYNOPSIS</span></span>
<span data-ttu-id="7b060-103">A központi felügyelet eltávolítása a felügyeleti csoportokban és a hozzájuk kapcsolódó műveletekben</span><span class="sxs-lookup"><span data-stu-id="7b060-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="7b060-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b060-104">SYNTAX</span></span>

### <span data-ttu-id="7b060-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b060-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b060-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7b060-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b060-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b060-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b060-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b060-108">DESCRIPTION</span></span>
<span data-ttu-id="7b060-109">A **Remove-AzManagementGroupDeployment** parancsmag egy olyan Azure-bevezetést távolít el egy felügyeleti csoportban és bármely kapcsolódó műveletben.</span><span class="sxs-lookup"><span data-stu-id="7b060-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="7b060-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7b060-110">EXAMPLES</span></span>

### <span data-ttu-id="7b060-111">1. példa: a példány eltávolítása adott névvel</span><span class="sxs-lookup"><span data-stu-id="7b060-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="7b060-112">Ez a parancs eltávolítja a "RolesDeployment" központi telepítőt a "myMG" felügyeleti csoportnál.</span><span class="sxs-lookup"><span data-stu-id="7b060-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="7b060-113">2. példa: központi üzembe állítás és eltávolítás</span><span class="sxs-lookup"><span data-stu-id="7b060-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="7b060-114">Ez a parancs a "RolesDeployment" ("myMG") felügyeleti csoport "" üzembe állítását és eltávolítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b060-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="7b060-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b060-115">PARAMETERS</span></span>

### <span data-ttu-id="7b060-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b060-116">-AsJob</span></span>
<span data-ttu-id="7b060-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7b060-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b060-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b060-118">-DefaultProfile</span></span>
<span data-ttu-id="7b060-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b060-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b060-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7b060-120">-Id</span></span>
<span data-ttu-id="7b060-121">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b060-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7b060-122">Példa:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7b060-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b060-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b060-123">-InputObject</span></span>
<span data-ttu-id="7b060-124">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="7b060-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b060-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7b060-125">-ManagementGroupId</span></span>
<span data-ttu-id="7b060-126">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b060-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b060-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b060-127">-Name</span></span>
<span data-ttu-id="7b060-128">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="7b060-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b060-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b060-129">-PassThru</span></span>
<span data-ttu-id="7b060-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7b060-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7b060-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="7b060-131">-Pre</span></span>
<span data-ttu-id="7b060-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7b060-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7b060-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b060-133">-Confirm</span></span>
<span data-ttu-id="7b060-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b060-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b060-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b060-135">-WhatIf</span></span>
<span data-ttu-id="7b060-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b060-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b060-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b060-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b060-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b060-138">CommonParameters</span></span>
<span data-ttu-id="7b060-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b060-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b060-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7b060-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b060-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b060-141">INPUTS</span></span>

### <span data-ttu-id="7b060-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7b060-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7b060-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b060-143">OUTPUTS</span></span>

### <span data-ttu-id="7b060-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b060-144">System.Boolean</span></span>

## <span data-ttu-id="7b060-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b060-145">NOTES</span></span>

## <span data-ttu-id="7b060-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b060-146">RELATED LINKS</span></span>
