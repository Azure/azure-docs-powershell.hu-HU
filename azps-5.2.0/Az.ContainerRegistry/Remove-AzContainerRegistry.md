---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356261"
---
# <span data-ttu-id="fea8e-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fea8e-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="fea8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea8e-102">SYNOPSIS</span></span>
<span data-ttu-id="fea8e-103">Eltávolítja a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="fea8e-103">Removes a container registry.</span></span>

## <span data-ttu-id="fea8e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fea8e-104">SYNTAX</span></span>

### <span data-ttu-id="fea8e-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fea8e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea8e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea8e-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea8e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea8e-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea8e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fea8e-108">DESCRIPTION</span></span>
<span data-ttu-id="fea8e-109">A Remove-AzContainerRegistry parancsmag eltávolítja a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="fea8e-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="fea8e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fea8e-110">EXAMPLES</span></span>

### <span data-ttu-id="fea8e-111">1. példa: Egy megadott tároló beállításjegyzékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fea8e-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="fea8e-112">Ez a parancs eltávolítja a megadott tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="fea8e-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="fea8e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fea8e-113">PARAMETERS</span></span>

### <span data-ttu-id="fea8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea8e-114">-DefaultProfile</span></span>
<span data-ttu-id="fea8e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fea8e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fea8e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fea8e-116">-Name</span></span>
<span data-ttu-id="fea8e-117">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="fea8e-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="fea8e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fea8e-118">-PassThru</span></span>
<span data-ttu-id="fea8e-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad vissza, ha az eltávolítás sikerült.</span><span class="sxs-lookup"><span data-stu-id="fea8e-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="fea8e-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="fea8e-120">-Registry</span></span>
<span data-ttu-id="fea8e-121">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="fea8e-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="fea8e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea8e-122">-ResourceGroupName</span></span>
<span data-ttu-id="fea8e-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fea8e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="fea8e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea8e-124">-ResourceId</span></span>
<span data-ttu-id="fea8e-125">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fea8e-125">The container registry resource id</span></span>

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

### <span data-ttu-id="fea8e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fea8e-126">-Confirm</span></span>
<span data-ttu-id="fea8e-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fea8e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea8e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea8e-128">-WhatIf</span></span>
<span data-ttu-id="fea8e-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fea8e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea8e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fea8e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea8e-131">CommonParameters</span></span>
<span data-ttu-id="fea8e-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea8e-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fea8e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea8e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fea8e-134">INPUTS</span></span>

### <span data-ttu-id="fea8e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fea8e-135">System.String</span></span>

## <span data-ttu-id="fea8e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea8e-136">OUTPUTS</span></span>

### <span data-ttu-id="fea8e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fea8e-137">System.Boolean</span></span>

## <span data-ttu-id="fea8e-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fea8e-138">NOTES</span></span>

## <span data-ttu-id="fea8e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fea8e-139">RELATED LINKS</span></span>

[<span data-ttu-id="fea8e-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fea8e-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="fea8e-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fea8e-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="fea8e-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fea8e-142">Update-AzContainerRegistry</span></span>]()

