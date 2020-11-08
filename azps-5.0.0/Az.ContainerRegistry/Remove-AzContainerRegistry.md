---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185579"
---
# <span data-ttu-id="c85ed-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c85ed-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="c85ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c85ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c85ed-103">Tároló-nyilvántartó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c85ed-103">Removes a container registry.</span></span>

## <span data-ttu-id="c85ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c85ed-104">SYNTAX</span></span>

### <span data-ttu-id="c85ed-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c85ed-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c85ed-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c85ed-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c85ed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c85ed-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c85ed-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c85ed-108">DESCRIPTION</span></span>
<span data-ttu-id="c85ed-109">A Remove-AzContainerRegistry parancsmag eltávolítja a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="c85ed-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="c85ed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c85ed-110">EXAMPLES</span></span>

### <span data-ttu-id="c85ed-111">1. példa: a megadott tároló beállításjegyzékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c85ed-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="c85ed-112">Ez a parancs eltávolítja a megadott tároló-beállításjegyzéket.</span><span class="sxs-lookup"><span data-stu-id="c85ed-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="c85ed-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c85ed-113">PARAMETERS</span></span>

### <span data-ttu-id="c85ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c85ed-114">-DefaultProfile</span></span>
<span data-ttu-id="c85ed-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c85ed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c85ed-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c85ed-116">-Name</span></span>
<span data-ttu-id="c85ed-117">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="c85ed-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="c85ed-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c85ed-118">-PassThru</span></span>
<span data-ttu-id="c85ed-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="c85ed-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="c85ed-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="c85ed-120">-Registry</span></span>
<span data-ttu-id="c85ed-121">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="c85ed-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="c85ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c85ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="c85ed-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c85ed-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c85ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c85ed-124">-ResourceId</span></span>
<span data-ttu-id="c85ed-125">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="c85ed-125">The container registry resource id</span></span>

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

### <span data-ttu-id="c85ed-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c85ed-126">-Confirm</span></span>
<span data-ttu-id="c85ed-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c85ed-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c85ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c85ed-128">-WhatIf</span></span>
<span data-ttu-id="c85ed-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c85ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c85ed-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c85ed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c85ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c85ed-131">CommonParameters</span></span>
<span data-ttu-id="c85ed-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c85ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c85ed-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c85ed-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c85ed-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c85ed-134">INPUTS</span></span>

### <span data-ttu-id="c85ed-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c85ed-135">System.String</span></span>

## <span data-ttu-id="c85ed-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c85ed-136">OUTPUTS</span></span>

### <span data-ttu-id="c85ed-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c85ed-137">System.Boolean</span></span>

## <span data-ttu-id="c85ed-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c85ed-138">NOTES</span></span>

## <span data-ttu-id="c85ed-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c85ed-139">RELATED LINKS</span></span>

[<span data-ttu-id="c85ed-140">Új – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c85ed-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="c85ed-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c85ed-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="c85ed-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c85ed-142">Update-AzContainerRegistry</span></span>]()

