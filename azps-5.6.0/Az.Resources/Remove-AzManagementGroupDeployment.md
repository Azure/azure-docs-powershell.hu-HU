---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: 06f3dec483c2c8b5e1730cb1046f927d6d38a7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926458"
---
# <span data-ttu-id="48ac7-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="48ac7-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="48ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="48ac7-103">Egy központi telepítés eltávolítása egy felügyeleti csoportnál és a kapcsolódó műveleteknél</span><span class="sxs-lookup"><span data-stu-id="48ac7-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="48ac7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48ac7-104">SYNTAX</span></span>

### <span data-ttu-id="48ac7-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48ac7-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ac7-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="48ac7-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ac7-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="48ac7-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48ac7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48ac7-108">DESCRIPTION</span></span>
<span data-ttu-id="48ac7-109">A **Remove-AzManagementGroupDeployment** parancsmag eltávolít egy Azure-telepítést egy felügyeleti csoportban és a kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="48ac7-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="48ac7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48ac7-110">EXAMPLES</span></span>

### <span data-ttu-id="48ac7-111">1. példa: Adott nevű telepítés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="48ac7-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="48ac7-112">Ez a parancs eltávolítja a "RolesDeployment" központi telepítést a "myMG" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="48ac7-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="48ac7-113">2. példa: Telepítés lekérte és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="48ac7-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="48ac7-114">Ez a parancs a "RolesDeployment" központi telepítést a "myMG" felügyeleti csoportban kapja meg, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="48ac7-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="48ac7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48ac7-115">PARAMETERS</span></span>

### <span data-ttu-id="48ac7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48ac7-116">-AsJob</span></span>
<span data-ttu-id="48ac7-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="48ac7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48ac7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ac7-118">-DefaultProfile</span></span>
<span data-ttu-id="48ac7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48ac7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ac7-120">-Id</span><span class="sxs-lookup"><span data-stu-id="48ac7-120">-Id</span></span>
<span data-ttu-id="48ac7-121">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="48ac7-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="48ac7-122">példa: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="48ac7-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="48ac7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48ac7-123">-InputObject</span></span>
<span data-ttu-id="48ac7-124">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="48ac7-124">The deployment object.</span></span>

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

### <span data-ttu-id="48ac7-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="48ac7-125">-ManagementGroupId</span></span>
<span data-ttu-id="48ac7-126">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="48ac7-126">The management group id.</span></span>

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

### <span data-ttu-id="48ac7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="48ac7-127">-Name</span></span>
<span data-ttu-id="48ac7-128">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="48ac7-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="48ac7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48ac7-129">-PassThru</span></span>
<span data-ttu-id="48ac7-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="48ac7-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="48ac7-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="48ac7-131">-Pre</span></span>
<span data-ttu-id="48ac7-132">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="48ac7-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="48ac7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48ac7-133">-Confirm</span></span>
<span data-ttu-id="48ac7-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="48ac7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48ac7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ac7-135">-WhatIf</span></span>
<span data-ttu-id="48ac7-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="48ac7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48ac7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48ac7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48ac7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ac7-138">CommonParameters</span></span>
<span data-ttu-id="48ac7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ac7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ac7-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48ac7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ac7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48ac7-141">INPUTS</span></span>

### <span data-ttu-id="48ac7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="48ac7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="48ac7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48ac7-143">OUTPUTS</span></span>

### <span data-ttu-id="48ac7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48ac7-144">System.Boolean</span></span>

## <span data-ttu-id="48ac7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48ac7-145">NOTES</span></span>

## <span data-ttu-id="48ac7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48ac7-146">RELATED LINKS</span></span>
