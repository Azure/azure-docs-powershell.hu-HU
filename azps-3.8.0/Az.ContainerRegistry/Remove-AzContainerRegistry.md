---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845682"
---
# <span data-ttu-id="213e6-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="213e6-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="213e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="213e6-102">SYNOPSIS</span></span>
<span data-ttu-id="213e6-103">Tároló-nyilvántartó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="213e6-103">Removes a container registry.</span></span>

## <span data-ttu-id="213e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="213e6-104">SYNTAX</span></span>

### <span data-ttu-id="213e6-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="213e6-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="213e6-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="213e6-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="213e6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="213e6-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="213e6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="213e6-108">DESCRIPTION</span></span>
<span data-ttu-id="213e6-109">A Remove-AzContainerRegistry parancsmag eltávolítja a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="213e6-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="213e6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="213e6-110">EXAMPLES</span></span>

### <span data-ttu-id="213e6-111">1. példa: a megadott tároló beállításjegyzékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="213e6-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="213e6-112">Ez a parancs eltávolítja a megadott tároló-beállításjegyzéket.</span><span class="sxs-lookup"><span data-stu-id="213e6-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="213e6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="213e6-113">PARAMETERS</span></span>

### <span data-ttu-id="213e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213e6-114">-DefaultProfile</span></span>
<span data-ttu-id="213e6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="213e6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="213e6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="213e6-116">-Name</span></span>
<span data-ttu-id="213e6-117">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="213e6-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="213e6-118">-PassThru</span></span>
<span data-ttu-id="213e6-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="213e6-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="213e6-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="213e6-120">-Registry</span></span>
<span data-ttu-id="213e6-121">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="213e6-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="213e6-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="213e6-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="213e6-124">-ResourceId</span></span>
<span data-ttu-id="213e6-125">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="213e6-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213e6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="213e6-126">-Confirm</span></span>
<span data-ttu-id="213e6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="213e6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="213e6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="213e6-128">-WhatIf</span></span>
<span data-ttu-id="213e6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="213e6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="213e6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="213e6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="213e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213e6-131">CommonParameters</span></span>
<span data-ttu-id="213e6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="213e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213e6-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="213e6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213e6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="213e6-134">INPUTS</span></span>

### <span data-ttu-id="213e6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="213e6-135">System.String</span></span>

## <span data-ttu-id="213e6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="213e6-136">OUTPUTS</span></span>

### <span data-ttu-id="213e6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="213e6-137">System.Boolean</span></span>

## <span data-ttu-id="213e6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="213e6-138">NOTES</span></span>

## <span data-ttu-id="213e6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="213e6-139">RELATED LINKS</span></span>

[<span data-ttu-id="213e6-140">Új – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="213e6-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="213e6-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="213e6-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="213e6-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="213e6-142">Update-AzContainerRegistry</span></span>]()

