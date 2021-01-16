---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355541"
---
# <span data-ttu-id="0f632-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0f632-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="0f632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f632-102">SYNOPSIS</span></span>
<span data-ttu-id="0f632-103">Egy központi telepítés eltávolítása egy felügyeleti csoportnál és a kapcsolódó műveleteknél</span><span class="sxs-lookup"><span data-stu-id="0f632-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="0f632-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f632-104">SYNTAX</span></span>

### <span data-ttu-id="0f632-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f632-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f632-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0f632-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f632-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f632-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f632-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f632-108">DESCRIPTION</span></span>
<span data-ttu-id="0f632-109">A **Remove-AzManagementGroupDeployment** parancsmag eltávolítja az Azure-telepítéseket egy felügyeleti csoportban, valamint a hozzájuk kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="0f632-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="0f632-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f632-110">EXAMPLES</span></span>

### <span data-ttu-id="0f632-111">1. példa: Adott nevű telepítés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f632-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="0f632-112">Ez a parancs eltávolítja a "RolesDeployment" központi telepítést a "myMG" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="0f632-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="0f632-113">2. példa: Telepítés lekérte és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f632-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="0f632-114">Ez a parancs a "RolesDeployment" központi telepítést a "myMG" felügyeleti csoportban kapja meg, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="0f632-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="0f632-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f632-115">PARAMETERS</span></span>

### <span data-ttu-id="0f632-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f632-116">-AsJob</span></span>
<span data-ttu-id="0f632-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f632-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f632-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f632-118">-DefaultProfile</span></span>
<span data-ttu-id="0f632-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f632-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f632-120">-Id</span><span class="sxs-lookup"><span data-stu-id="0f632-120">-Id</span></span>
<span data-ttu-id="0f632-121">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0f632-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0f632-122">példa: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0f632-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0f632-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f632-123">-InputObject</span></span>
<span data-ttu-id="0f632-124">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="0f632-124">The deployment object.</span></span>

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

### <span data-ttu-id="0f632-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0f632-125">-ManagementGroupId</span></span>
<span data-ttu-id="0f632-126">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0f632-126">The management group id.</span></span>

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

### <span data-ttu-id="0f632-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0f632-127">-Name</span></span>
<span data-ttu-id="0f632-128">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="0f632-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="0f632-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f632-129">-PassThru</span></span>
<span data-ttu-id="0f632-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0f632-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0f632-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="0f632-131">-Pre</span></span>
<span data-ttu-id="0f632-132">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0f632-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0f632-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f632-133">-Confirm</span></span>
<span data-ttu-id="0f632-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f632-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f632-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f632-135">-WhatIf</span></span>
<span data-ttu-id="0f632-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0f632-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f632-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f632-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f632-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f632-138">CommonParameters</span></span>
<span data-ttu-id="0f632-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f632-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f632-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f632-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f632-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f632-141">INPUTS</span></span>

### <span data-ttu-id="0f632-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0f632-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0f632-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f632-143">OUTPUTS</span></span>

### <span data-ttu-id="0f632-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f632-144">System.Boolean</span></span>

## <span data-ttu-id="0f632-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f632-145">NOTES</span></span>

## <span data-ttu-id="0f632-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f632-146">RELATED LINKS</span></span>
