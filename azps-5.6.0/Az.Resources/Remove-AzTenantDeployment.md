---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: f995050e86189c1b84652895ad0434403c4e86d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932314"
---
# <span data-ttu-id="10091-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="10091-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="10091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10091-102">SYNOPSIS</span></span>
<span data-ttu-id="10091-103">Eltávolítja a telepítést a bérlő hatókörében és a kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="10091-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="10091-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10091-104">SYNTAX</span></span>

### <span data-ttu-id="10091-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10091-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10091-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="10091-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10091-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="10091-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10091-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10091-108">DESCRIPTION</span></span>
<span data-ttu-id="10091-109">A **Remove-AzTenantDeployment** parancsmag eltávolítja az Azure-telepítéseket a bérlő aktuális hatókörében, valamint a kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="10091-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="10091-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10091-110">EXAMPLES</span></span>

### <span data-ttu-id="10091-111">1. példa: Adott nevű telepítés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="10091-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="10091-112">Ez a parancs eltávolítja a "RolesDeployment" központi telepítést a bérlő aktuális hatókörében.</span><span class="sxs-lookup"><span data-stu-id="10091-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="10091-113">2. példa: Telepítés lekérte és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="10091-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="10091-114">Ez a parancs a központi telepítés "RolesDeployment" parancsát kapja meg az aktuális bérlői webhelyen, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="10091-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="10091-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10091-115">PARAMETERS</span></span>

### <span data-ttu-id="10091-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10091-116">-AsJob</span></span>
<span data-ttu-id="10091-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="10091-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10091-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10091-118">-DefaultProfile</span></span>
<span data-ttu-id="10091-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10091-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10091-120">-Id</span><span class="sxs-lookup"><span data-stu-id="10091-120">-Id</span></span>
<span data-ttu-id="10091-121">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="10091-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="10091-122">példa: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="10091-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="10091-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10091-123">-InputObject</span></span>
<span data-ttu-id="10091-124">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="10091-124">The deployment object.</span></span>

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

### <span data-ttu-id="10091-125">-Name</span><span class="sxs-lookup"><span data-stu-id="10091-125">-Name</span></span>
<span data-ttu-id="10091-126">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="10091-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="10091-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10091-127">-PassThru</span></span>
<span data-ttu-id="10091-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="10091-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="10091-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="10091-129">-Pre</span></span>
<span data-ttu-id="10091-130">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="10091-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="10091-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10091-131">-Confirm</span></span>
<span data-ttu-id="10091-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="10091-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10091-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10091-133">-WhatIf</span></span>
<span data-ttu-id="10091-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="10091-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10091-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10091-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10091-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10091-136">CommonParameters</span></span>
<span data-ttu-id="10091-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10091-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10091-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10091-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10091-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10091-139">INPUTS</span></span>

### <span data-ttu-id="10091-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="10091-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="10091-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10091-141">OUTPUTS</span></span>

### <span data-ttu-id="10091-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10091-142">System.Boolean</span></span>

## <span data-ttu-id="10091-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10091-143">NOTES</span></span>

## <span data-ttu-id="10091-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10091-144">RELATED LINKS</span></span>
