---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: be9a289e7d3aca0bc0a4cc4e2ae8e23dbe5b1ae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679486"
---
# <span data-ttu-id="f6cd7-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f6cd7-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="f6cd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="f6cd7-103">Tároló csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f6cd7-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6cd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6cd7-104">SYNTAX</span></span>

### <span data-ttu-id="f6cd7-105">RemoveContainerGroupByResourceGroupAndNameParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6cd7-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6cd7-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f6cd7-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6cd7-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="f6cd7-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6cd7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6cd7-108">DESCRIPTION</span></span>
<span data-ttu-id="f6cd7-109">A **Remove-AzureRmContainerGroup** parancsmag eltávolítja a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="f6cd7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f6cd7-110">EXAMPLES</span></span>

### <span data-ttu-id="f6cd7-111">1. példa: a tároló csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f6cd7-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="f6cd7-112">Ez a parancs eltávolítja a megadott tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="f6cd7-113">2. példa: a tárolók csoportjának eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f6cd7-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="f6cd7-114">Ez a parancs a tárolók csoportját csövekkel távolítja el.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="f6cd7-115">3. példa: erőforrás-azonosítóval távolítja el a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="f6cd7-116">Ez a parancs erőforrás-azonosítóval távolítja el a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="f6cd7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6cd7-117">PARAMETERS</span></span>

### <span data-ttu-id="f6cd7-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6cd7-118">-Confirm</span></span>
<span data-ttu-id="f6cd7-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6cd7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6cd7-120">-InputObject</span></span>
<span data-ttu-id="f6cd7-121">Az eltávolítandó tároló csoport.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-121">The container group to remove.</span></span>

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

### <span data-ttu-id="f6cd7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6cd7-122">-Name</span></span>
<span data-ttu-id="f6cd7-123">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-123">The container group name.</span></span>

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

### <span data-ttu-id="f6cd7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6cd7-124">-PassThru</span></span>
<span data-ttu-id="f6cd7-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f6cd7-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f6cd7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6cd7-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6cd7-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-127">The resource group name.</span></span>

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

### <span data-ttu-id="f6cd7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cd7-128">-ResourceId</span></span>
<span data-ttu-id="f6cd7-129">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-129">The resource id.</span></span>

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

### <span data-ttu-id="f6cd7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6cd7-130">-WhatIf</span></span>
<span data-ttu-id="f6cd7-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6cd7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6cd7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6cd7-133">-DefaultProfile</span></span>
<span data-ttu-id="f6cd7-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cd7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6cd7-135">CommonParameters</span></span>
<span data-ttu-id="f6cd7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6cd7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6cd7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6cd7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6cd7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6cd7-138">INPUTS</span></span>

### <span data-ttu-id="f6cd7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f6cd7-139">System.String</span></span>
<span data-ttu-id="f6cd7-140">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f6cd7-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="f6cd7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6cd7-141">OUTPUTS</span></span>

### <span data-ttu-id="f6cd7-142">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f6cd7-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="f6cd7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6cd7-143">NOTES</span></span>

## <span data-ttu-id="f6cd7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6cd7-144">RELATED LINKS</span></span>

