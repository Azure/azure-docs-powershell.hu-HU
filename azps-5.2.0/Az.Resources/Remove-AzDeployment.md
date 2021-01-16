---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355577"
---
# <span data-ttu-id="231bd-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="231bd-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="231bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="231bd-102">SYNOPSIS</span></span>
<span data-ttu-id="231bd-103">Eltávolítja a telepítést és a kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="231bd-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="231bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="231bd-104">SYNTAX</span></span>

### <span data-ttu-id="231bd-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="231bd-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="231bd-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="231bd-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="231bd-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="231bd-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="231bd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="231bd-108">DESCRIPTION</span></span>
<span data-ttu-id="231bd-109">A **Remove-AzDeployment** parancsmag eltávolítja az Azure-telepítéseket az előfizetés hatókörében, valamint a kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="231bd-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="231bd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="231bd-110">EXAMPLES</span></span>

### <span data-ttu-id="231bd-111">1. példa: Adott nevű telepítés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="231bd-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="231bd-112">Ez a parancs eltávolítja a "RolesDeployment" telepítést az aktuális előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="231bd-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="231bd-113">2. példa: Telepítés lekérte és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="231bd-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="231bd-114">Ez a parancs a központi telepítés "RolesDeployment" parancsát kapja meg az aktuális előfizetési hatókörben, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="231bd-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="231bd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="231bd-115">PARAMETERS</span></span>

### <span data-ttu-id="231bd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="231bd-116">-AsJob</span></span>
<span data-ttu-id="231bd-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="231bd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="231bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="231bd-118">-DefaultProfile</span></span>
<span data-ttu-id="231bd-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="231bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="231bd-120">-Id</span><span class="sxs-lookup"><span data-stu-id="231bd-120">-Id</span></span>
<span data-ttu-id="231bd-121">A telepítés teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="231bd-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="231bd-122">példa: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="231bd-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="231bd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="231bd-123">-InputObject</span></span>
<span data-ttu-id="231bd-124">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="231bd-124">The deployment object.</span></span>

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

### <span data-ttu-id="231bd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="231bd-125">-Name</span></span>
<span data-ttu-id="231bd-126">A központi telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="231bd-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="231bd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="231bd-127">-PassThru</span></span>
<span data-ttu-id="231bd-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="231bd-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="231bd-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="231bd-129">-Pre</span></span>
<span data-ttu-id="231bd-130">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="231bd-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="231bd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="231bd-131">-Confirm</span></span>
<span data-ttu-id="231bd-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="231bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="231bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="231bd-133">-WhatIf</span></span>
<span data-ttu-id="231bd-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="231bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="231bd-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="231bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="231bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="231bd-136">CommonParameters</span></span>
<span data-ttu-id="231bd-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="231bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="231bd-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="231bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="231bd-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="231bd-139">INPUTS</span></span>

### <span data-ttu-id="231bd-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="231bd-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="231bd-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="231bd-141">OUTPUTS</span></span>

### <span data-ttu-id="231bd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="231bd-142">System.Boolean</span></span>

## <span data-ttu-id="231bd-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="231bd-143">NOTES</span></span>

## <span data-ttu-id="231bd-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="231bd-144">RELATED LINKS</span></span>
