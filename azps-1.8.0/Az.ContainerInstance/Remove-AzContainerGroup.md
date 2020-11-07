---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: fb9b2c23618d731f6f107f755ca6ef41dfe439ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671188"
---
# <span data-ttu-id="e2018-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e2018-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="e2018-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2018-102">SYNOPSIS</span></span>
<span data-ttu-id="e2018-103">Tároló csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e2018-103">Removes a container group.</span></span>

## <span data-ttu-id="e2018-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2018-104">SYNTAX</span></span>

### <span data-ttu-id="e2018-105">RemoveContainerGroupByResourceGroupAndNameParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2018-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2018-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="e2018-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2018-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="e2018-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2018-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2018-108">DESCRIPTION</span></span>
<span data-ttu-id="e2018-109">A **Remove-AzContainerGroup** parancsmag eltávolítja a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="e2018-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="e2018-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e2018-110">EXAMPLES</span></span>

### <span data-ttu-id="e2018-111">1. példa: a tároló csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e2018-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="e2018-112">Ez a parancs eltávolítja a megadott tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="e2018-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="e2018-113">2. példa: a tárolók csoportjának eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e2018-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="e2018-114">Ez a parancs a tárolók csoportját csövekkel távolítja el.</span><span class="sxs-lookup"><span data-stu-id="e2018-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="e2018-115">3. példa: erőforrás-azonosítóval távolítja el a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="e2018-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="e2018-116">Ez a parancs erőforrás-azonosítóval távolítja el a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="e2018-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="e2018-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2018-117">PARAMETERS</span></span>

### <span data-ttu-id="e2018-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2018-118">-DefaultProfile</span></span>
<span data-ttu-id="e2018-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2018-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2018-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2018-120">-InputObject</span></span>
<span data-ttu-id="e2018-121">Az eltávolítandó tároló csoport.</span><span class="sxs-lookup"><span data-stu-id="e2018-121">The container group to remove.</span></span>

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

### <span data-ttu-id="e2018-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2018-122">-Name</span></span>
<span data-ttu-id="e2018-123">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2018-123">The container group name.</span></span>

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

### <span data-ttu-id="e2018-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2018-124">-PassThru</span></span>
<span data-ttu-id="e2018-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e2018-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e2018-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2018-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2018-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2018-127">The resource group name.</span></span>

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

### <span data-ttu-id="e2018-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2018-128">-ResourceId</span></span>
<span data-ttu-id="e2018-129">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e2018-129">The resource id.</span></span>

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

### <span data-ttu-id="e2018-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2018-130">-Confirm</span></span>
<span data-ttu-id="e2018-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2018-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2018-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2018-132">-WhatIf</span></span>
<span data-ttu-id="e2018-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2018-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2018-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2018-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2018-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2018-135">CommonParameters</span></span>
<span data-ttu-id="e2018-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2018-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2018-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2018-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2018-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2018-138">INPUTS</span></span>

### <span data-ttu-id="e2018-139">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e2018-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="e2018-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e2018-140">System.String</span></span>

## <span data-ttu-id="e2018-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2018-141">OUTPUTS</span></span>

### <span data-ttu-id="e2018-142">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e2018-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="e2018-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2018-143">NOTES</span></span>

## <span data-ttu-id="e2018-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2018-144">RELATED LINKS</span></span>
