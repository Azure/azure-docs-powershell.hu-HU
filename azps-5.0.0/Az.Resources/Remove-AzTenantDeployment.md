---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195531"
---
# <span data-ttu-id="99734-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="99734-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="99734-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99734-102">SYNOPSIS</span></span>
<span data-ttu-id="99734-103">A bevezetést eltávolítja a bérlői hatókörben és az esetleges kapcsolódó műveletekben</span><span class="sxs-lookup"><span data-stu-id="99734-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="99734-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99734-104">SYNTAX</span></span>

### <span data-ttu-id="99734-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99734-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99734-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="99734-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99734-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="99734-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99734-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="99734-108">DESCRIPTION</span></span>
<span data-ttu-id="99734-109">A **Remove-AzTenantDeployment** parancsmag a jelenlegi bérlői hatókör és az ahhoz kapcsolódó műveletek Azure-telepítését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="99734-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="99734-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99734-110">EXAMPLES</span></span>

### <span data-ttu-id="99734-111">1. példa: a példány eltávolítása adott névvel</span><span class="sxs-lookup"><span data-stu-id="99734-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="99734-112">Ez a parancs eltávolítja a "RolesDeployment" telepítőt az aktuális bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="99734-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="99734-113">2. példa: központi üzembe állítás és eltávolítás</span><span class="sxs-lookup"><span data-stu-id="99734-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="99734-114">Ez a parancs a "RolesDeployment" üzembe helyezi az aktuális bérlői hatókört, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="99734-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="99734-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99734-115">PARAMETERS</span></span>

### <span data-ttu-id="99734-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99734-116">-AsJob</span></span>
<span data-ttu-id="99734-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99734-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99734-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99734-118">-DefaultProfile</span></span>
<span data-ttu-id="99734-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99734-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99734-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="99734-120">-Id</span></span>
<span data-ttu-id="99734-121">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="99734-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="99734-122">Példa:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="99734-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="99734-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99734-123">-InputObject</span></span>
<span data-ttu-id="99734-124">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="99734-124">The deployment object.</span></span>

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

### <span data-ttu-id="99734-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99734-125">-Name</span></span>
<span data-ttu-id="99734-126">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="99734-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99734-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99734-127">-PassThru</span></span>
<span data-ttu-id="99734-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="99734-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="99734-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="99734-129">-Pre</span></span>
<span data-ttu-id="99734-130">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="99734-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="99734-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99734-131">-Confirm</span></span>
<span data-ttu-id="99734-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99734-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99734-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99734-133">-WhatIf</span></span>
<span data-ttu-id="99734-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99734-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99734-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99734-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99734-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99734-136">CommonParameters</span></span>
<span data-ttu-id="99734-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99734-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99734-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99734-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99734-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99734-139">INPUTS</span></span>

### <span data-ttu-id="99734-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="99734-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="99734-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99734-141">OUTPUTS</span></span>

### <span data-ttu-id="99734-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99734-142">System.Boolean</span></span>

## <span data-ttu-id="99734-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99734-143">NOTES</span></span>

## <span data-ttu-id="99734-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99734-144">RELATED LINKS</span></span>
