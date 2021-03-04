---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 2af89bac9e748fca0719abf34bd672d2b09c3af5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926433"
---
# <span data-ttu-id="2a8c4-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2a8c4-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2a8c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8c4-103">Futó telepítés megszakítása egy felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="2a8c4-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="2a8c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a8c4-104">SYNTAX</span></span>

### <span data-ttu-id="2a8c4-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a8c4-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8c4-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2a8c4-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8c4-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a8c4-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a8c4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a8c4-108">DESCRIPTION</span></span>
<span data-ttu-id="2a8c4-109">A **Stop-AzManagementGroupDeployment** parancsmag megszakít egy olyan telepítést, amely elkezdődött, de nem fejeződött be egy felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="2a8c4-110">Az üzembe helyezés befejezéséhez a központi telepítésnek hiányos kiépítési állapotnak (például Provisioning) kell lennie, nem pedig befejezettnek (például Kiépítve vagy Sikertelen).</span><span class="sxs-lookup"><span data-stu-id="2a8c4-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="2a8c4-111">Ha egy felügyeleti csoportban létre kell hoznia egy központi telepítést, használja a New-AzManagementGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="2a8c4-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a8c4-112">EXAMPLES</span></span>

### <span data-ttu-id="2a8c4-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="2a8c4-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="2a8c4-114">Ez a parancs megszakítja a futó telepítés "deployment01" futását a "myMG" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="2a8c4-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="2a8c4-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="2a8c4-116">Ez a parancs lekérte a központi telepítést01 a "myMG" felügyeleti csoportban, és megszakítja azt.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="2a8c4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a8c4-117">PARAMETERS</span></span>

### <span data-ttu-id="2a8c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8c4-118">-DefaultProfile</span></span>
<span data-ttu-id="2a8c4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a8c4-120">-Id</span><span class="sxs-lookup"><span data-stu-id="2a8c4-120">-Id</span></span>
<span data-ttu-id="2a8c4-121">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2a8c4-122">példa: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2a8c4-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a8c4-123">-InputObject</span></span>
<span data-ttu-id="2a8c4-124">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c4-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2a8c4-125">-ManagementGroupId</span></span>
<span data-ttu-id="2a8c4-126">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2a8c4-127">-Name</span></span>
<span data-ttu-id="2a8c4-128">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a8c4-129">-PassThru</span></span>
<span data-ttu-id="2a8c4-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2a8c4-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2a8c4-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="2a8c4-131">-Pre</span></span>
<span data-ttu-id="2a8c4-132">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2a8c4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a8c4-133">-Confirm</span></span>
<span data-ttu-id="2a8c4-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a8c4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a8c4-135">-WhatIf</span></span>
<span data-ttu-id="2a8c4-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a8c4-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a8c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8c4-138">CommonParameters</span></span>
<span data-ttu-id="2a8c4-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8c4-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a8c4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8c4-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a8c4-141">INPUTS</span></span>

### <span data-ttu-id="2a8c4-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2a8c4-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2a8c4-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a8c4-143">OUTPUTS</span></span>

### <span data-ttu-id="2a8c4-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a8c4-144">System.Boolean</span></span>

## <span data-ttu-id="2a8c4-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a8c4-145">NOTES</span></span>

## <span data-ttu-id="2a8c4-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a8c4-146">RELATED LINKS</span></span>
