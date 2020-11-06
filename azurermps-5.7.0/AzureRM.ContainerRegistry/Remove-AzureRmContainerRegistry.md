---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497664"
---
# <span data-ttu-id="29ffc-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29ffc-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="29ffc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="29ffc-103">Tároló-nyilvántartó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="29ffc-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29ffc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29ffc-104">SYNTAX</span></span>

### <span data-ttu-id="29ffc-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29ffc-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29ffc-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29ffc-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29ffc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29ffc-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ffc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="29ffc-108">DESCRIPTION</span></span>
<span data-ttu-id="29ffc-109">A Remove-AzureRmContainerRegistry parancsmag eltávolítja a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="29ffc-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="29ffc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="29ffc-110">EXAMPLES</span></span>

### <span data-ttu-id="29ffc-111">1. példa: a megadott tároló beállításjegyzékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="29ffc-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="29ffc-112">Ez a parancs eltávolítja a megadott tároló-beállításjegyzéket.</span><span class="sxs-lookup"><span data-stu-id="29ffc-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="29ffc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29ffc-113">PARAMETERS</span></span>

### <span data-ttu-id="29ffc-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29ffc-114">-Name</span></span>
<span data-ttu-id="29ffc-115">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="29ffc-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ffc-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="29ffc-116">-Registry</span></span>
<span data-ttu-id="29ffc-117">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="29ffc-117">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ffc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ffc-118">-ResourceGroupName</span></span>
<span data-ttu-id="29ffc-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="29ffc-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ffc-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29ffc-120">-Confirm</span></span>
<span data-ttu-id="29ffc-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29ffc-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ffc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ffc-122">-WhatIf</span></span>
<span data-ttu-id="29ffc-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29ffc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29ffc-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29ffc-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ffc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ffc-125">-DefaultProfile</span></span>
<span data-ttu-id="29ffc-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29ffc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29ffc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29ffc-127">-ResourceId</span></span>
<span data-ttu-id="29ffc-128">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="29ffc-128">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ffc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29ffc-129">-PassThru</span></span>
<span data-ttu-id="29ffc-130">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="29ffc-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="29ffc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ffc-131">CommonParameters</span></span>
<span data-ttu-id="29ffc-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29ffc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ffc-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ffc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ffc-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29ffc-134">INPUTS</span></span>

### <span data-ttu-id="29ffc-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29ffc-135">PSContainerRegistry</span></span>
<span data-ttu-id="29ffc-136">A "Registry" paraméter elfogadja a "PSContainerRegistry" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="29ffc-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="29ffc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29ffc-137">OUTPUTS</span></span>

### <span data-ttu-id="29ffc-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="29ffc-138">None</span></span>

## <span data-ttu-id="29ffc-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29ffc-139">NOTES</span></span>

## <span data-ttu-id="29ffc-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29ffc-140">RELATED LINKS</span></span>

[<span data-ttu-id="29ffc-141">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29ffc-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="29ffc-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29ffc-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="29ffc-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29ffc-143">Update-AzureRmContainerRegistry</span></span>]()

