---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187026"
---
# <span data-ttu-id="bfda1-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bfda1-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="bfda1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfda1-102">SYNOPSIS</span></span>
<span data-ttu-id="bfda1-103">Futó telepített példány lemondása a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="bfda1-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="bfda1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfda1-104">SYNTAX</span></span>

### <span data-ttu-id="bfda1-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfda1-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfda1-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="bfda1-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfda1-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="bfda1-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfda1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfda1-108">DESCRIPTION</span></span>
<span data-ttu-id="bfda1-109">A **stop-AzTenantDeployment** parancsmag lemondja azokat a telepített példányokat, amelyek a jelenlegi bérlői hatókörben nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="bfda1-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="bfda1-110">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="bfda1-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="bfda1-111">Ha a bérlői hatókörben szeretne bevezetést létrehozni, használja az New-AzTenantDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bfda1-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="bfda1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="bfda1-112">EXAMPLES</span></span>

### <span data-ttu-id="bfda1-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bfda1-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="bfda1-114">A parancs a jelenlegi bérlői hatókörben lemondja a "deployment01" futó központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="bfda1-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="bfda1-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="bfda1-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="bfda1-116">Ez a parancs beilleszti a "deployment01" üzembe állítást az aktuális bérlői tartományba, és lemondja azt.</span><span class="sxs-lookup"><span data-stu-id="bfda1-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="bfda1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfda1-117">PARAMETERS</span></span>

### <span data-ttu-id="bfda1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfda1-118">-DefaultProfile</span></span>
<span data-ttu-id="bfda1-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfda1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfda1-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bfda1-120">-Id</span></span>
<span data-ttu-id="bfda1-121">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bfda1-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="bfda1-122">Példa:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="bfda1-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="bfda1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfda1-123">-InputObject</span></span>
<span data-ttu-id="bfda1-124">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="bfda1-124">The deployment object.</span></span>

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

### <span data-ttu-id="bfda1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bfda1-125">-Name</span></span>
<span data-ttu-id="bfda1-126">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="bfda1-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="bfda1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfda1-127">-PassThru</span></span>
<span data-ttu-id="bfda1-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bfda1-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="bfda1-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="bfda1-129">-Pre</span></span>
<span data-ttu-id="bfda1-130">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bfda1-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bfda1-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bfda1-131">-Confirm</span></span>
<span data-ttu-id="bfda1-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bfda1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfda1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfda1-133">-WhatIf</span></span>
<span data-ttu-id="bfda1-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bfda1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfda1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfda1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfda1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfda1-136">CommonParameters</span></span>
<span data-ttu-id="bfda1-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfda1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfda1-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bfda1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfda1-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfda1-139">INPUTS</span></span>

### <span data-ttu-id="bfda1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="bfda1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="bfda1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfda1-141">OUTPUTS</span></span>

### <span data-ttu-id="bfda1-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfda1-142">System.Boolean</span></span>

## <span data-ttu-id="bfda1-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfda1-143">NOTES</span></span>

## <span data-ttu-id="bfda1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfda1-144">RELATED LINKS</span></span>
