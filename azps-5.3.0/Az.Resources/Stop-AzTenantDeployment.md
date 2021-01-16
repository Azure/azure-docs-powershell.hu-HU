---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466391"
---
# <span data-ttu-id="30a74-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="30a74-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="30a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a74-102">SYNOPSIS</span></span>
<span data-ttu-id="30a74-103">Futó telepítés megszakítása bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="30a74-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="30a74-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30a74-104">SYNTAX</span></span>

### <span data-ttu-id="30a74-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30a74-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a74-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="30a74-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a74-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="30a74-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a74-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30a74-108">DESCRIPTION</span></span>
<span data-ttu-id="30a74-109">A **Stop-AzTenantDeployment** parancsmag megszakít egy olyan telepítést, amely elkezdődött, de nem fejeződött be az aktuális bérlői webhelyen.</span><span class="sxs-lookup"><span data-stu-id="30a74-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="30a74-110">Az üzembe helyezés befejezéséhez a központi telepítésnek hiányos kiépítési állapotnak (például Provisioning) kell lennie, nem pedig befejezettnek (például Kiépítve vagy Sikertelen).</span><span class="sxs-lookup"><span data-stu-id="30a74-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="30a74-111">Ha bérlői hatókörben létre kell hoznia egy központi telepítést, használja a New-AzTenantDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="30a74-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="30a74-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30a74-112">EXAMPLES</span></span>

### <span data-ttu-id="30a74-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="30a74-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="30a74-114">Ez a parancs megszakítja a futó telepítés "deployment01" futását az aktuális bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="30a74-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="30a74-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="30a74-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="30a74-116">Ez a parancs lekérte a központi telepítést01 a bérlő aktuális hatókörében, és megszakítja azt.</span><span class="sxs-lookup"><span data-stu-id="30a74-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="30a74-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30a74-117">PARAMETERS</span></span>

### <span data-ttu-id="30a74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a74-118">-DefaultProfile</span></span>
<span data-ttu-id="30a74-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30a74-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a74-120">-Id</span><span class="sxs-lookup"><span data-stu-id="30a74-120">-Id</span></span>
<span data-ttu-id="30a74-121">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="30a74-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="30a74-122">példa: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="30a74-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="30a74-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30a74-123">-InputObject</span></span>
<span data-ttu-id="30a74-124">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="30a74-124">The deployment object.</span></span>

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

### <span data-ttu-id="30a74-125">-Name</span><span class="sxs-lookup"><span data-stu-id="30a74-125">-Name</span></span>
<span data-ttu-id="30a74-126">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="30a74-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a74-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30a74-127">-PassThru</span></span>
<span data-ttu-id="30a74-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="30a74-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="30a74-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="30a74-129">-Pre</span></span>
<span data-ttu-id="30a74-130">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="30a74-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="30a74-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30a74-131">-Confirm</span></span>
<span data-ttu-id="30a74-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="30a74-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a74-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a74-133">-WhatIf</span></span>
<span data-ttu-id="30a74-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="30a74-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a74-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30a74-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a74-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a74-136">CommonParameters</span></span>
<span data-ttu-id="30a74-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a74-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a74-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30a74-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a74-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30a74-139">INPUTS</span></span>

### <span data-ttu-id="30a74-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="30a74-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="30a74-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30a74-141">OUTPUTS</span></span>

### <span data-ttu-id="30a74-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30a74-142">System.Boolean</span></span>

## <span data-ttu-id="30a74-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30a74-143">NOTES</span></span>

## <span data-ttu-id="30a74-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30a74-144">RELATED LINKS</span></span>
