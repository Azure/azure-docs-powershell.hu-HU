---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011754"
---
# <span data-ttu-id="d4003-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4003-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="d4003-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4003-102">SYNOPSIS</span></span>
<span data-ttu-id="d4003-103">Egy erőforráscsoport-telepítő és az ahhoz kapcsolódó műveletek eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d4003-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="d4003-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4003-104">SYNTAX</span></span>

### <span data-ttu-id="d4003-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4003-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4003-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d4003-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4003-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4003-107">DESCRIPTION</span></span>

<span data-ttu-id="d4003-108">A **Remove-AzResourceGroupDeployment** parancsmag eltávolít egy Azure erőforráscsoport-telepítőt és bármely kapcsolódó műveletet.</span><span class="sxs-lookup"><span data-stu-id="d4003-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="d4003-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d4003-109">EXAMPLES</span></span>

### <span data-ttu-id="d4003-110">1. példa: egy erőforráscsoport-telepítő eltávolítása a ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4003-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="d4003-111">Ez a parancs eltávolítja az erőforráscsoport-bevezetést a bevezetésben a teljes értékű erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="d4003-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d4003-112">A sikeres eltávolítás eredménye igaz.</span><span class="sxs-lookup"><span data-stu-id="d4003-112">Successful removal returns true.</span></span>

### <span data-ttu-id="d4003-113">2. példa: az erőforráscsoport-telepítő eltávolítása a ResourceGroupName és a ResourceName</span><span class="sxs-lookup"><span data-stu-id="d4003-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="d4003-114">Ez a parancs eltávolítja az erőforráscsoport-telepítőt a megadott ResourceGroupName és ResourceName.</span><span class="sxs-lookup"><span data-stu-id="d4003-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="d4003-115">A sikeres eltávolítás eredménye igaz.</span><span class="sxs-lookup"><span data-stu-id="d4003-115">Successful removal returns true.</span></span>

## <span data-ttu-id="d4003-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4003-116">PARAMETERS</span></span>

### <span data-ttu-id="d4003-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4003-117">-ApiVersion</span></span>
<span data-ttu-id="d4003-118">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4003-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d4003-119">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="d4003-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4003-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4003-120">-DefaultProfile</span></span>
<span data-ttu-id="d4003-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4003-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4003-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d4003-122">-Id</span></span>
<span data-ttu-id="d4003-123">Az eltávolítandó erőforráscsoport-példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4003-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="d4003-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4003-124">-Name</span></span>
<span data-ttu-id="d4003-125">Az eltávolítandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4003-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="d4003-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4003-126">-Pre</span></span>
<span data-ttu-id="d4003-127">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="d4003-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d4003-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4003-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4003-129">Az eltávolítandó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4003-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="d4003-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4003-130">-Confirm</span></span>
<span data-ttu-id="d4003-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4003-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4003-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4003-132">-WhatIf</span></span>
<span data-ttu-id="d4003-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4003-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4003-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4003-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4003-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4003-135">CommonParameters</span></span>
<span data-ttu-id="d4003-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4003-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4003-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4003-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4003-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4003-138">INPUTS</span></span>

### <span data-ttu-id="d4003-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d4003-139">System.String</span></span>

## <span data-ttu-id="d4003-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4003-140">OUTPUTS</span></span>

### <span data-ttu-id="d4003-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4003-141">System.Boolean</span></span>

## <span data-ttu-id="d4003-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4003-142">NOTES</span></span>

## <span data-ttu-id="d4003-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4003-143">RELATED LINKS</span></span>

[<span data-ttu-id="d4003-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4003-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="d4003-145">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4003-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="d4003-146">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4003-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="d4003-147">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4003-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


