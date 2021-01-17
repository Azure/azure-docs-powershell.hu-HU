---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480642"
---
# <span data-ttu-id="61c8a-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="61c8a-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="61c8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="61c8a-103">Eltávolít egy tárolócsoportot.</span><span class="sxs-lookup"><span data-stu-id="61c8a-103">Removes a container group.</span></span>

## <span data-ttu-id="61c8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61c8a-104">SYNTAX</span></span>

### <span data-ttu-id="61c8a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="61c8a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61c8a-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="61c8a-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61c8a-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="61c8a-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61c8a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61c8a-108">DESCRIPTION</span></span>
<span data-ttu-id="61c8a-109">A **Remove-AzContainerGroup** parancsmag eltávolít egy tárolócsoportot.</span><span class="sxs-lookup"><span data-stu-id="61c8a-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="61c8a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61c8a-110">EXAMPLES</span></span>

### <span data-ttu-id="61c8a-111">1. példa: Tárolócsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="61c8a-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="61c8a-112">Ez a parancs eltávolítja a megadott tárolócsoportot.</span><span class="sxs-lookup"><span data-stu-id="61c8a-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="61c8a-113">2. példa: Egy tárolócsoport eltávolítása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="61c8a-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="61c8a-114">Ez a parancs egy tárolócsoportot pipával távolít el.</span><span class="sxs-lookup"><span data-stu-id="61c8a-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="61c8a-115">3. példa: Egy tárolócsoport eltávolítása erőforrás-azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="61c8a-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="61c8a-116">Ez a parancs erőforrás-azonosító szerint eltávolítja a tárolócsoportokat.</span><span class="sxs-lookup"><span data-stu-id="61c8a-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="61c8a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61c8a-117">PARAMETERS</span></span>

### <span data-ttu-id="61c8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c8a-118">-DefaultProfile</span></span>
<span data-ttu-id="61c8a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61c8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61c8a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61c8a-120">-InputObject</span></span>
<span data-ttu-id="61c8a-121">Az eltávolítható tárolócsoport.</span><span class="sxs-lookup"><span data-stu-id="61c8a-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61c8a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="61c8a-122">-Name</span></span>
<span data-ttu-id="61c8a-123">A tárolócsoport neve.</span><span class="sxs-lookup"><span data-stu-id="61c8a-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c8a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61c8a-124">-PassThru</span></span>
<span data-ttu-id="61c8a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="61c8a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="61c8a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c8a-126">-ResourceGroupName</span></span>
<span data-ttu-id="61c8a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="61c8a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c8a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61c8a-128">-ResourceId</span></span>
<span data-ttu-id="61c8a-129">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="61c8a-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61c8a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61c8a-130">-Confirm</span></span>
<span data-ttu-id="61c8a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="61c8a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61c8a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61c8a-132">-WhatIf</span></span>
<span data-ttu-id="61c8a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="61c8a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61c8a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61c8a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61c8a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c8a-135">CommonParameters</span></span>
<span data-ttu-id="61c8a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c8a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c8a-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c8a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c8a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61c8a-138">INPUTS</span></span>

### <span data-ttu-id="61c8a-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="61c8a-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="61c8a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="61c8a-140">System.String</span></span>

## <span data-ttu-id="61c8a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61c8a-141">OUTPUTS</span></span>

### <span data-ttu-id="61c8a-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="61c8a-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="61c8a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61c8a-143">NOTES</span></span>

## <span data-ttu-id="61c8a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61c8a-144">RELATED LINKS</span></span>
