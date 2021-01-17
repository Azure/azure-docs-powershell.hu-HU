---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468549"
---
# <span data-ttu-id="a3be3-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3be3-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a3be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3be3-102">SYNOPSIS</span></span>
<span data-ttu-id="a3be3-103">Eltávolítja az erőforráscsoport-telepítést és a kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="a3be3-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="a3be3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3be3-104">SYNTAX</span></span>

### <span data-ttu-id="a3be3-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3be3-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3be3-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a3be3-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3be3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3be3-107">DESCRIPTION</span></span>

<span data-ttu-id="a3be3-108">A **Remove-AzResourceGroupDeployment** parancsmag eltávolítja az Azure-erőforráscsoportok telepítését és a hozzájuk kapcsolódó műveleteket.</span><span class="sxs-lookup"><span data-stu-id="a3be3-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="a3be3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3be3-109">EXAMPLES</span></span>

### <span data-ttu-id="a3be3-110">1. példa: Erőforráscsoport-telepítés eltávolítása az Erőforrásazonosítóval</span><span class="sxs-lookup"><span data-stu-id="a3be3-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="a3be3-111">Ez a parancs eltávolít egy erőforráscsoport-telepítést a telepítés teljes erőforrás-azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="a3be3-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a3be3-112">A sikeres eltávolítás eredménye igaz.</span><span class="sxs-lookup"><span data-stu-id="a3be3-112">Successful removal returns true.</span></span>

### <span data-ttu-id="a3be3-113">2. példa: Erőforráscsoport-telepítés eltávolítása a ResourceGroupName és az ResourceName csoporttal</span><span class="sxs-lookup"><span data-stu-id="a3be3-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="a3be3-114">Ez a parancs eltávolít egy erőforráscsoport-telepítést a megadott ResourceGroupName és ResourceName mezővel.</span><span class="sxs-lookup"><span data-stu-id="a3be3-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="a3be3-115">A sikeres eltávolítás eredménye igaz.</span><span class="sxs-lookup"><span data-stu-id="a3be3-115">Successful removal returns true.</span></span>

## <span data-ttu-id="a3be3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3be3-116">PARAMETERS</span></span>

### <span data-ttu-id="a3be3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3be3-117">-DefaultProfile</span></span>
<span data-ttu-id="a3be3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3be3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3be3-119">-Id</span><span class="sxs-lookup"><span data-stu-id="a3be3-119">-Id</span></span>
<span data-ttu-id="a3be3-120">Az eltávolítható erőforráscsoport-telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3be3-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3be3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3be3-121">-Name</span></span>
<span data-ttu-id="a3be3-122">Az eltávolítható erőforráscsoport-telepítés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3be3-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3be3-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="a3be3-123">-Pre</span></span>
<span data-ttu-id="a3be3-124">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="a3be3-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a3be3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3be3-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3be3-126">Az eltávolítható erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3be3-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3be3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3be3-127">-Confirm</span></span>
<span data-ttu-id="a3be3-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a3be3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3be3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3be3-129">-WhatIf</span></span>
<span data-ttu-id="a3be3-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a3be3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3be3-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3be3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3be3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3be3-132">CommonParameters</span></span>
<span data-ttu-id="a3be3-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3be3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3be3-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3be3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3be3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3be3-135">INPUTS</span></span>

### <span data-ttu-id="a3be3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a3be3-136">System.String</span></span>

## <span data-ttu-id="a3be3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3be3-137">OUTPUTS</span></span>

### <span data-ttu-id="a3be3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3be3-138">System.Boolean</span></span>

## <span data-ttu-id="a3be3-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3be3-139">NOTES</span></span>

## <span data-ttu-id="a3be3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3be3-140">RELATED LINKS</span></span>

[<span data-ttu-id="a3be3-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3be3-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a3be3-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3be3-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="a3be3-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3be3-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="a3be3-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3be3-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


