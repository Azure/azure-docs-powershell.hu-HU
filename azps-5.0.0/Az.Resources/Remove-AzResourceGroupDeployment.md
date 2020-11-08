---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195539"
---
# <span data-ttu-id="5d15d-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d15d-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="5d15d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d15d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d15d-103">Egy erőforráscsoport-telepítő és az ahhoz kapcsolódó műveletek eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5d15d-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="5d15d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d15d-104">SYNTAX</span></span>

### <span data-ttu-id="5d15d-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d15d-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d15d-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5d15d-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d15d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d15d-107">DESCRIPTION</span></span>

<span data-ttu-id="5d15d-108">A **Remove-AzResourceGroupDeployment** parancsmag eltávolít egy Azure erőforráscsoport-telepítőt és bármely kapcsolódó műveletet.</span><span class="sxs-lookup"><span data-stu-id="5d15d-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="5d15d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5d15d-109">EXAMPLES</span></span>

### <span data-ttu-id="5d15d-110">1. példa: egy erőforráscsoport-telepítő eltávolítása a ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d15d-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="5d15d-111">Ez a parancs eltávolítja az erőforráscsoport-bevezetést a bevezetésben a teljes értékű erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="5d15d-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5d15d-112">A sikeres eltávolítás eredménye igaz.</span><span class="sxs-lookup"><span data-stu-id="5d15d-112">Successful removal returns true.</span></span>

### <span data-ttu-id="5d15d-113">2. példa: az erőforráscsoport-telepítő eltávolítása a ResourceGroupName és a ResourceName</span><span class="sxs-lookup"><span data-stu-id="5d15d-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="5d15d-114">Ez a parancs eltávolítja az erőforráscsoport-telepítőt a megadott ResourceGroupName és ResourceName.</span><span class="sxs-lookup"><span data-stu-id="5d15d-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="5d15d-115">A sikeres eltávolítás eredménye igaz.</span><span class="sxs-lookup"><span data-stu-id="5d15d-115">Successful removal returns true.</span></span>

## <span data-ttu-id="5d15d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d15d-116">PARAMETERS</span></span>

### <span data-ttu-id="5d15d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d15d-117">-DefaultProfile</span></span>
<span data-ttu-id="5d15d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5d15d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d15d-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5d15d-119">-Id</span></span>
<span data-ttu-id="5d15d-120">Az eltávolítandó erőforráscsoport-példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d15d-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="5d15d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d15d-121">-Name</span></span>
<span data-ttu-id="5d15d-122">Az eltávolítandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d15d-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="5d15d-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="5d15d-123">-Pre</span></span>
<span data-ttu-id="5d15d-124">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="5d15d-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5d15d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d15d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d15d-126">Az eltávolítandó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d15d-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="5d15d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d15d-127">-Confirm</span></span>
<span data-ttu-id="5d15d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d15d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d15d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d15d-129">-WhatIf</span></span>
<span data-ttu-id="5d15d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d15d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d15d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d15d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d15d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d15d-132">CommonParameters</span></span>
<span data-ttu-id="5d15d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d15d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d15d-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d15d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d15d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d15d-135">INPUTS</span></span>

### <span data-ttu-id="5d15d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5d15d-136">System.String</span></span>

## <span data-ttu-id="5d15d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d15d-137">OUTPUTS</span></span>

### <span data-ttu-id="5d15d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d15d-138">System.Boolean</span></span>

## <span data-ttu-id="5d15d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d15d-139">NOTES</span></span>

## <span data-ttu-id="5d15d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d15d-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d15d-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d15d-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="5d15d-142">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d15d-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="5d15d-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d15d-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="5d15d-144">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5d15d-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


