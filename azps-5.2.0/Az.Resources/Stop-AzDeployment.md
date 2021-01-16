---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354006"
---
# <span data-ttu-id="f0331-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0331-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="f0331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0331-102">SYNOPSIS</span></span>
<span data-ttu-id="f0331-103">Futó telepítés megszakítása</span><span class="sxs-lookup"><span data-stu-id="f0331-103">Cancel a running deployment</span></span>

## <span data-ttu-id="f0331-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f0331-104">SYNTAX</span></span>

### <span data-ttu-id="f0331-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0331-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0331-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f0331-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0331-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0331-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0331-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f0331-108">DESCRIPTION</span></span>
<span data-ttu-id="f0331-109">A **Stop-AzDeployment** parancsmag megszakítja a telepítést az előfizetés hatókörében, amely elkezdődött, de nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="f0331-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="f0331-110">Az üzembe helyezés befejezéséhez a központi telepítésnek hiányos kiépítési állapotnak (például Provisioning) kell lennie, nem pedig befejezettnek (például Kiépítve vagy Sikertelen).</span><span class="sxs-lookup"><span data-stu-id="f0331-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="f0331-111">Ha az előfizetés hatókörében létre kell hoznia egy központi telepítést, használja a New-AzDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f0331-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="f0331-112">Ez a parancsmag csak egy futó telepítést leállít.</span><span class="sxs-lookup"><span data-stu-id="f0331-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="f0331-113">A Name *paraméter* használatával leállíthatja az adott telepítést.</span><span class="sxs-lookup"><span data-stu-id="f0331-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="f0331-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f0331-114">EXAMPLES</span></span>

### <span data-ttu-id="f0331-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="f0331-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="f0331-116">Ez a parancs megszakítja a futó telepítés "deployment01" futását az aktuális előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="f0331-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="f0331-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="f0331-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="f0331-118">Ez a parancs a központi telepítést a jelenlegi előfizetési hatókörben "deployment01" (központi telepítés) kapja meg, és lemondja azt.</span><span class="sxs-lookup"><span data-stu-id="f0331-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="f0331-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0331-119">PARAMETERS</span></span>

### <span data-ttu-id="f0331-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0331-120">-DefaultProfile</span></span>
<span data-ttu-id="f0331-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0331-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0331-122">-Id</span><span class="sxs-lookup"><span data-stu-id="f0331-122">-Id</span></span>
<span data-ttu-id="f0331-123">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f0331-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f0331-124">példa: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f0331-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="f0331-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0331-125">-InputObject</span></span>
<span data-ttu-id="f0331-126">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="f0331-126">The deployment object.</span></span>

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

### <span data-ttu-id="f0331-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f0331-127">-Name</span></span>
<span data-ttu-id="f0331-128">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="f0331-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="f0331-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0331-129">-PassThru</span></span>
<span data-ttu-id="f0331-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f0331-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f0331-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0331-131">-Pre</span></span>
<span data-ttu-id="f0331-132">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f0331-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f0331-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0331-133">-Confirm</span></span>
<span data-ttu-id="f0331-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f0331-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0331-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0331-135">-WhatIf</span></span>
<span data-ttu-id="f0331-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f0331-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0331-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0331-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0331-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0331-138">CommonParameters</span></span>
<span data-ttu-id="f0331-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0331-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0331-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0331-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0331-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0331-141">INPUTS</span></span>

### <span data-ttu-id="f0331-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f0331-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f0331-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0331-143">OUTPUTS</span></span>

### <span data-ttu-id="f0331-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0331-144">System.Boolean</span></span>

## <span data-ttu-id="f0331-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f0331-145">NOTES</span></span>

## <span data-ttu-id="f0331-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0331-146">RELATED LINKS</span></span>
