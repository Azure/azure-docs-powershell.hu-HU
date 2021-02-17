---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208383"
---
# <span data-ttu-id="45780-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45780-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="45780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45780-102">SYNOPSIS</span></span>
<span data-ttu-id="45780-103">Futó telepítés megszakítása egy felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="45780-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="45780-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="45780-104">SYNTAX</span></span>

### <span data-ttu-id="45780-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45780-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45780-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="45780-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45780-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="45780-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45780-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="45780-108">DESCRIPTION</span></span>
<span data-ttu-id="45780-109">A **Stop-AzManagementGroupDeployment** parancsmag megszakít egy olyan telepítést, amely elkezdődött, de nem fejeződött be egy felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="45780-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="45780-110">Az üzembe helyezés befejezéséhez a központi telepítésnek hiányos kiépítési állapotnak (például Provisioning) kell lennie, nem pedig befejezettnek (például Kiépítve vagy Sikertelen).</span><span class="sxs-lookup"><span data-stu-id="45780-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="45780-111">Ha egy felügyeleti csoportban létre kell hoznia egy központi telepítést, használja a New-AzManagementGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="45780-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="45780-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="45780-112">EXAMPLES</span></span>

### <span data-ttu-id="45780-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="45780-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="45780-114">Ez a parancs megszakítja a futó telepítés "deployment01" futását a "myMG" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="45780-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="45780-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="45780-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="45780-116">Ez a parancs lekérte a központi telepítést01 a "myMG" felügyeleti csoportban, és megszakítja azt.</span><span class="sxs-lookup"><span data-stu-id="45780-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="45780-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45780-117">PARAMETERS</span></span>

### <span data-ttu-id="45780-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45780-118">-DefaultProfile</span></span>
<span data-ttu-id="45780-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45780-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45780-120">-Id</span><span class="sxs-lookup"><span data-stu-id="45780-120">-Id</span></span>
<span data-ttu-id="45780-121">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="45780-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="45780-122">példa: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="45780-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="45780-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45780-123">-InputObject</span></span>
<span data-ttu-id="45780-124">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="45780-124">The deployment object.</span></span>

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

### <span data-ttu-id="45780-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="45780-125">-ManagementGroupId</span></span>
<span data-ttu-id="45780-126">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="45780-126">The management group id.</span></span>

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

### <span data-ttu-id="45780-127">-Name</span><span class="sxs-lookup"><span data-stu-id="45780-127">-Name</span></span>
<span data-ttu-id="45780-128">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="45780-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="45780-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45780-129">-PassThru</span></span>
<span data-ttu-id="45780-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="45780-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="45780-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="45780-131">-Pre</span></span>
<span data-ttu-id="45780-132">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="45780-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="45780-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45780-133">-Confirm</span></span>
<span data-ttu-id="45780-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="45780-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45780-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45780-135">-WhatIf</span></span>
<span data-ttu-id="45780-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="45780-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45780-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45780-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45780-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45780-138">CommonParameters</span></span>
<span data-ttu-id="45780-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45780-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45780-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45780-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45780-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45780-141">INPUTS</span></span>

### <span data-ttu-id="45780-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="45780-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="45780-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45780-143">OUTPUTS</span></span>

### <span data-ttu-id="45780-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45780-144">System.Boolean</span></span>

## <span data-ttu-id="45780-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="45780-145">NOTES</span></span>

## <span data-ttu-id="45780-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45780-146">RELATED LINKS</span></span>
