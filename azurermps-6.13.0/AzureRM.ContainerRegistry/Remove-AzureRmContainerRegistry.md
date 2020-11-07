---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679586"
---
# <span data-ttu-id="9155f-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9155f-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="9155f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9155f-102">SYNOPSIS</span></span>
<span data-ttu-id="9155f-103">Tároló-nyilvántartó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9155f-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9155f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9155f-104">SYNTAX</span></span>

### <span data-ttu-id="9155f-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9155f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9155f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9155f-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9155f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9155f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9155f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9155f-108">DESCRIPTION</span></span>
<span data-ttu-id="9155f-109">A Remove-AzureRmContainerRegistry parancsmag eltávolítja a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="9155f-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="9155f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9155f-110">EXAMPLES</span></span>

### <span data-ttu-id="9155f-111">1. példa: a megadott tároló beállításjegyzékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9155f-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="9155f-112">Ez a parancs eltávolítja a megadott tároló-beállításjegyzéket.</span><span class="sxs-lookup"><span data-stu-id="9155f-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="9155f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9155f-113">PARAMETERS</span></span>

### <span data-ttu-id="9155f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9155f-114">-DefaultProfile</span></span>
<span data-ttu-id="9155f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9155f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9155f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9155f-116">-Name</span></span>
<span data-ttu-id="9155f-117">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="9155f-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="9155f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9155f-118">-PassThru</span></span>
<span data-ttu-id="9155f-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="9155f-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="9155f-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="9155f-120">-Registry</span></span>
<span data-ttu-id="9155f-121">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="9155f-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="9155f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9155f-122">-ResourceGroupName</span></span>
<span data-ttu-id="9155f-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9155f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="9155f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9155f-124">-ResourceId</span></span>
<span data-ttu-id="9155f-125">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="9155f-125">The container registry resource id</span></span>

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

### <span data-ttu-id="9155f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9155f-126">-Confirm</span></span>
<span data-ttu-id="9155f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9155f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9155f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9155f-128">-WhatIf</span></span>
<span data-ttu-id="9155f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9155f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9155f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9155f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9155f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9155f-131">CommonParameters</span></span>
<span data-ttu-id="9155f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9155f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9155f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9155f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9155f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9155f-134">INPUTS</span></span>

### <span data-ttu-id="9155f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9155f-135">System.String</span></span>

## <span data-ttu-id="9155f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9155f-136">OUTPUTS</span></span>

### <span data-ttu-id="9155f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9155f-137">System.Boolean</span></span>

## <span data-ttu-id="9155f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9155f-138">NOTES</span></span>

## <span data-ttu-id="9155f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9155f-139">RELATED LINKS</span></span>

[<span data-ttu-id="9155f-140">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9155f-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="9155f-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9155f-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="9155f-142">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9155f-142">Update-AzureRmContainerRegistry</span></span>]()

