---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480627"
---
# <span data-ttu-id="8c3bf-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c3bf-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="8c3bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3bf-103">Eltávolítja a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-103">Removes a container registry.</span></span>

## <span data-ttu-id="8c3bf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c3bf-104">SYNTAX</span></span>

### <span data-ttu-id="8c3bf-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c3bf-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3bf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c3bf-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3bf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c3bf-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c3bf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c3bf-108">DESCRIPTION</span></span>
<span data-ttu-id="8c3bf-109">A Remove-AzContainerRegistry parancsmag eltávolítja a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="8c3bf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c3bf-110">EXAMPLES</span></span>

### <span data-ttu-id="8c3bf-111">1. példa: Egy megadott tároló beállításjegyzékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8c3bf-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="8c3bf-112">Ez a parancs eltávolítja a megadott tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="8c3bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c3bf-113">PARAMETERS</span></span>

### <span data-ttu-id="8c3bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3bf-114">-DefaultProfile</span></span>
<span data-ttu-id="8c3bf-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c3bf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c3bf-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8c3bf-116">-Name</span></span>
<span data-ttu-id="8c3bf-117">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="8c3bf-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c3bf-118">-PassThru</span></span>
<span data-ttu-id="8c3bf-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad vissza, ha az eltávolítás sikerült.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="8c3bf-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="8c3bf-120">-Registry</span></span>
<span data-ttu-id="8c3bf-121">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="8c3bf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3bf-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c3bf-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c3bf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c3bf-124">-ResourceId</span></span>
<span data-ttu-id="8c3bf-125">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8c3bf-125">The container registry resource id</span></span>

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

### <span data-ttu-id="8c3bf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c3bf-126">-Confirm</span></span>
<span data-ttu-id="8c3bf-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c3bf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c3bf-128">-WhatIf</span></span>
<span data-ttu-id="8c3bf-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c3bf-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c3bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3bf-131">CommonParameters</span></span>
<span data-ttu-id="8c3bf-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3bf-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c3bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3bf-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c3bf-134">INPUTS</span></span>

### <span data-ttu-id="8c3bf-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8c3bf-135">System.String</span></span>

## <span data-ttu-id="8c3bf-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c3bf-136">OUTPUTS</span></span>

### <span data-ttu-id="8c3bf-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c3bf-137">System.Boolean</span></span>

## <span data-ttu-id="8c3bf-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c3bf-138">NOTES</span></span>

## <span data-ttu-id="8c3bf-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c3bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="8c3bf-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c3bf-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="8c3bf-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c3bf-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="8c3bf-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c3bf-142">Update-AzContainerRegistry</span></span>]()

