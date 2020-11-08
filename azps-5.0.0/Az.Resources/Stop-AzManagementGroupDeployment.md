---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187028"
---
# <span data-ttu-id="4dff6-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dff6-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="4dff6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4dff6-102">SYNOPSIS</span></span>
<span data-ttu-id="4dff6-103">Futó telepített példány lemondása felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="4dff6-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="4dff6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4dff6-104">SYNTAX</span></span>

### <span data-ttu-id="4dff6-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4dff6-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dff6-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4dff6-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dff6-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="4dff6-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dff6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4dff6-108">DESCRIPTION</span></span>
<span data-ttu-id="4dff6-109">A **stop-AzManagementGroupDeployment** parancsmag lemondja azokat a telepített példányokat, amelyek egy felügyeleti csoportban elkezdődtek, de nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="4dff6-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="4dff6-110">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="4dff6-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="4dff6-111">Ha egy felügyeleti csoportban szeretne bevezetést létrehozni, használja az New-AzManagementGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4dff6-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="4dff6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4dff6-112">EXAMPLES</span></span>

### <span data-ttu-id="4dff6-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4dff6-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="4dff6-114">Ez a parancs lemondja a "deployment01" futó központi telepítőt a "myMG" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="4dff6-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="4dff6-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="4dff6-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="4dff6-116">Ez a parancs a "deployment01" ("myMG") felügyeleti csoport "" üzembe állítását adja vissza, és lemondja azt.</span><span class="sxs-lookup"><span data-stu-id="4dff6-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="4dff6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4dff6-117">PARAMETERS</span></span>

### <span data-ttu-id="4dff6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dff6-118">-DefaultProfile</span></span>
<span data-ttu-id="4dff6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dff6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dff6-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="4dff6-120">-Id</span></span>
<span data-ttu-id="4dff6-121">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4dff6-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4dff6-122">Példa:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="4dff6-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="4dff6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dff6-123">-InputObject</span></span>
<span data-ttu-id="4dff6-124">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="4dff6-124">The deployment object.</span></span>

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

### <span data-ttu-id="4dff6-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4dff6-125">-ManagementGroupId</span></span>
<span data-ttu-id="4dff6-126">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4dff6-126">The management group id.</span></span>

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

### <span data-ttu-id="4dff6-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4dff6-127">-Name</span></span>
<span data-ttu-id="4dff6-128">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="4dff6-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="4dff6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dff6-129">-PassThru</span></span>
<span data-ttu-id="4dff6-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4dff6-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="4dff6-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="4dff6-131">-Pre</span></span>
<span data-ttu-id="4dff6-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4dff6-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4dff6-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4dff6-133">-Confirm</span></span>
<span data-ttu-id="4dff6-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4dff6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dff6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dff6-135">-WhatIf</span></span>
<span data-ttu-id="4dff6-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4dff6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dff6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4dff6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dff6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dff6-138">CommonParameters</span></span>
<span data-ttu-id="4dff6-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4dff6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dff6-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4dff6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dff6-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dff6-141">INPUTS</span></span>

### <span data-ttu-id="4dff6-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4dff6-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4dff6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dff6-143">OUTPUTS</span></span>

### <span data-ttu-id="4dff6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4dff6-144">System.Boolean</span></span>

## <span data-ttu-id="4dff6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4dff6-145">NOTES</span></span>

## <span data-ttu-id="4dff6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dff6-146">RELATED LINKS</span></span>
