---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: 80343713c9bf7a0e34a1d9a3b3b75825cbb97a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503815"
---
# <span data-ttu-id="98955-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="98955-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="98955-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98955-102">SYNOPSIS</span></span>
<span data-ttu-id="98955-103">Tároló csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="98955-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98955-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98955-104">SYNTAX</span></span>

### <span data-ttu-id="98955-105">RemoveContainerGroupByResourceGroupAndNameParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98955-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98955-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="98955-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98955-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="98955-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98955-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="98955-108">DESCRIPTION</span></span>
<span data-ttu-id="98955-109">A **Remove-AzureRmContainerGroup** parancsmag eltávolítja a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="98955-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="98955-110">Példák</span><span class="sxs-lookup"><span data-stu-id="98955-110">EXAMPLES</span></span>

### <span data-ttu-id="98955-111">1. példa: a tároló csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="98955-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="98955-112">Ez a parancs eltávolítja a megadott tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="98955-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="98955-113">2. példa: a tárolók csoportjának eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="98955-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="98955-114">Ez a parancs a tárolók csoportját csövekkel távolítja el.</span><span class="sxs-lookup"><span data-stu-id="98955-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="98955-115">3. példa: erőforrás-azonosítóval távolítja el a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="98955-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="98955-116">Ez a parancs erőforrás-azonosítóval távolítja el a tároló csoportot.</span><span class="sxs-lookup"><span data-stu-id="98955-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="98955-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98955-117">PARAMETERS</span></span>

### <span data-ttu-id="98955-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98955-118">-DefaultProfile</span></span>
<span data-ttu-id="98955-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98955-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98955-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98955-120">-InputObject</span></span>
<span data-ttu-id="98955-121">Az eltávolítandó tároló csoport.</span><span class="sxs-lookup"><span data-stu-id="98955-121">The container group to remove.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98955-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98955-122">-Name</span></span>
<span data-ttu-id="98955-123">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="98955-123">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98955-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98955-124">-PassThru</span></span>
<span data-ttu-id="98955-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="98955-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98955-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98955-126">-ResourceGroupName</span></span>
<span data-ttu-id="98955-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="98955-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98955-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98955-128">-ResourceId</span></span>
<span data-ttu-id="98955-129">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="98955-129">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98955-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98955-130">-Confirm</span></span>
<span data-ttu-id="98955-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98955-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98955-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98955-132">-WhatIf</span></span>
<span data-ttu-id="98955-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98955-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98955-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98955-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98955-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98955-135">CommonParameters</span></span>
<span data-ttu-id="98955-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98955-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98955-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98955-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98955-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98955-138">INPUTS</span></span>

### <span data-ttu-id="98955-139">System. String</span><span class="sxs-lookup"><span data-stu-id="98955-139">System.String</span></span>
<span data-ttu-id="98955-140">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="98955-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="98955-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98955-141">OUTPUTS</span></span>

### <span data-ttu-id="98955-142">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="98955-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="98955-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98955-143">NOTES</span></span>

## <span data-ttu-id="98955-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98955-144">RELATED LINKS</span></span>
